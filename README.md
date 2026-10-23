# ForzaPort 0.10.16.5

**[Download the app ZIP from Releases](https://github.com/Zenon0707/ForzaPort-Public/releases/latest).** Extract the whole ZIP, then double-click **ForzaPort.exe**. Keep **Dependencies** beside it.

This repository now contains the packaged Windows application, rather than the development tree.

## Setup

1. Install Microsoft .NET 8 x64 Runtime.
2. Open ForzaPort.exe. In Settings, choose your FH2/Azimuth 0.9.10 folder.
3. Supply your own readable source database and source Materials.zip in Dependencies/SourceResources, or select their paths in Settings. This folder deliberately contains no game resources.
4. Click Check setup and follow any runtime-preparation prompts.
5. Choose an original car ZIP, Convert, then Export ZIP or Add to game. Close the game before installing or undoing.

Use Undo / recover import for removal. Keep installation receipts and backups; never overwrite the game database to bypass a guard. Saves are not changed by the importer.

## Status

Development is shelved. This is an experimental evaluation build. Known limitations include catalogue/garage PI disagreement, driver hands and steering placement, partial lights and variable dirt/AO/material fidelity. Some cars have no supported compatible donor.

## Licences and credits

Retain all files under **Dependencies/Notices**, **Dependencies/Runtime** and **Dependencies/ExperimentalRuntime**. These include component licences, attribution and the supplied Extra Options corresponding-source bundles. See [third-party notices](THIRD_PARTY_NOTICES.md). Component terms remain distinct; this repository does not apply a blanket open-source licence to every DLL.
