<p align="center"><a href="https://alexbeavs-ps1-ports.github.io/psxrecomp-ports/"><img src="https://raw.githubusercontent.com/alexbeavs-ps1-ports/psxrecomp-ports/main/docs/assets/alexbeav-ps1-recomps-banner.png" alt="Alexbeav's PS1 Recomps" width="100%"></a></p>

# Metal Gear Solid Recompiled

This release candidate uses PSXRecomp and the shared recomp-ui launcher.
You must supply your own Metal Gear Solid (USA) game discs (SLUS-00594 and SLUS-00776) and SCPH-1001 (USA) BIOS.
The kit is made from the Redump dumps `Metal Gear Solid (USA) (Disc 1) (Rev 1)` and `Metal Gear Solid (USA) (Disc 2) (Rev 1)`.
The package contains no game disc, retail BIOS, generated retail game code, or saved game.

<!-- release-standard:bios -->
**BIOS:** SCPH-1001 (USA) retail BIOS, 524288 bytes, SHA-256 `71af94d1e47a68c11e8fdb9f8368040601514a42a5a399cda48c7d3bff1e99d3`. Supply your own dump; releases do not use OpenBIOS.
<!-- /release-standard:bios -->

## Status

Latest release: v0.1.4, built on psxrecomp pin I 0.1.23.

- Packages for Windows x64, Linux x64, macOS Apple Silicon and macOS Intel passed the CI build and package checks.
- Replay check: on Windows, a build on pin I 0.1.23 played 1 of 1 recorded route to the end without a crash. That check compares memory, not the picture, and is not a play test.
- Not claimed: full-game completion, audio fidelity or multiplayer. Setup and gameplay reports from Linux, macOS and Steam Deck are welcome.

Known issues for the current version are in its [release notes](https://github.com/alexbeavs-ps1-ports/metal-gear-solid-recomp/releases/tag/v0.1.4).

## Setup

1. Extract the complete setup ZIP into a writable folder.
2. Start `Metal_Gear_Solid_Recompiled` (`.exe` on Windows).
3. Select your CUE file and the required BIOS in the setup wizard.
4. Run Generate & rebuild and wait for the game to start.

On Windows, the setup wizard can download the portable build tools.
On Linux and macOS, install CMake, Ninja, Python 3, and a C/C++ compiler first.
Keep the CUE and all files it references together.
The BIOS must be 524288 bytes with SHA-256 `71af94d1e47a68c11e8fdb9f8368040601514a42a5a399cda48c7d3bff1e99d3`.

## Candidate status

This kit targets the USA release (SLUS-00594 and SLUS-00776) since October 1, 2026.
The USA target has not been built or run, and no version of it is released.
Versions 0.1.0 and 0.1.1 were candidates for the European release (SLES-01370 and SLES-11370); their checks do not carry over.
Package setup and gameplay acceptance are pending; native build checks do not establish gameplay support.
The exact source and dependency identities are in [project-manifest.toml](project-manifest.toml).
See [feasibility and validation](docs/FEASIBILITY.md) for the tested scope.

## About this project

This project was developed with AI assistance.
AI assists with code, documentation, and investigation; Alex tests the game and makes release decisions.
Validation claims describe only the tests actually performed.

## Credits and licenses

Framework: [PSXRecomp](https://github.com/mstan/psxrecomp).
Launcher: [recomp-ui](https://github.com/mstan/recomp-ui).
Their licenses and dependency notices remain in the corresponding source directories.
The original game and its trademarks belong to their respective owners.
