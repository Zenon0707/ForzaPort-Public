# Credits and acknowledgements

ForzaPort's database extraction work benefited from the following community projects. Thank you to their authors and contributors for making this research possible:

- **Doliman100 — [ForzaTech-crypto-tool](https://github.com/Doliman100/ForzaTech-crypto-tool)**: ForzaTech file encryption/decryption and GameDB deobfuscation research/tooling. Its repository carries GPL-3.0.
- **DVS-code — [Forza-Crypto-Tool](https://github.com/DVS-code/Forza-Crypto-Tool)**: additional Forza crypto/database tooling used in the extraction workflow.

These are independent third-party projects, not bundled ForzaPort components or endorsements. Credits do not imply that every tool operates locally, that all releases were audited, or that the converter invokes either tool automatically. ForzaPort currently expects a separately prepared readable source database. Their code, binaries and keys are not redistributed here; upstream license and usage terms remain applicable.

The experimental native runtime derives from **FH2 ExtraOptions**. Its GPL source, notices and license are retained under `runtime/`; that license is not replaced by this acknowledgement.

The Windows desktop build uses **Python**, **Tcl/Tk** and **PyInstaller**. Build dependencies and the PyInstaller bootloader exception retain their respective licenses; accompanying distribution notices are included with the desktop download. No blanket license has been chosen for the project's original code. ModelProbe dependency provenance/build acquisition remains a separate outstanding task.

Forza, vehicle brands and game assets belong to their respective owners. No game assets or saves are distributed by this source repository or desktop download.

The staged shader-contract research audit reuses **conner-mcvay and contributors — [fh2-mods](https://github.com/conner-mcvay/fh2-mods)** FM5 importer sources under MIT. The source-reference files were retained in the private development backup; their full MIT notice is retained in `Dependencies/Notices/licenses/fh2-mods-MIT.txt`. Its wheel-path, lighting and reversible-installation research informed the comparison; its installers and runtime DLLs are not automatically installed by ForzaPort.

The RC app also carries the unmodified CPython 3.11.9 documentation license page as `licenses/Python-ThirdParty.html` (sourced from the official installed CPython documentation). It contains the OpenSSL 3 Apache-2.0 and other bundled-library notices. Selected CPython native library hashes are recorded in `DEPENDENCIES.json`; Microsoft redistributable conditions remain applicable. This notice inventory does not clear ForzaPort original code or external ModelProbe/vendor components for public release.

**Rock — AO texture adaptation.** `app/rock_ao.py` is Rock's contributed `bc7_alpha_r8.py`, integrated with his express permission on 22 October 2026. Thank you for sharing the BC7 alpha extraction, Xbox tiling, mip handling and FH2 swatchbin writer. ForzaPort's scene-selection adapter and reporting are separate integration work. This permission does not cover redistribution of Microsoft's native `xg.dll`; that dependency remains separately supplied. No blanket third-party licence is inferred for Rock's contribution.

**Pillow contributors — image decoding.** Pillow decodes source BC7 alpha; its licence and bundled notices are retained under `Dependencies/Notices/licenses/Pillow` in packaged builds.

ForzaPort 0.10.16 optionally builds a generic suspension-limit overlay from pinned current FH2 ExtraOptions 0.2.98 source (26225c0). Its complete corresponding source and GPL licence accompany ExperimentalRuntime. The standard official binary remains separate. This overlay does not incorporate third-party wheel-mod code or the historical vehicle-specific drift/anti-lag branches.
