# ForzaPort 0.10.16.5 experimental RC

Windows evaluation converter for user-owned FH6 vehicle assets into FH2/Azimuth packages. Building and installing are separate operations. Arbitrary-car compatibility and complete interior animations are not guaranteed.

## Start here

1. Keep **ForzaPort.exe** beside its **Dependencies** folder. Double-click the EXE.
2. In Settings, choose your FH2/Azimuth folder. Prepared dependencies beside the EXE are detected automatically.
3. Click **Check setup**. Use **Prepare / update runtime** if requested.
4. On Convert, choose an original source car ZIP and click **Convert archive**. This builds a package; it does not install it.
5. Review the report. Choose **Add to game** to install, or **Export ZIP** to save the converted package. Close FH2 before installing or undoing.

An already-converted ZIP can be selected and added directly. It does not gain new conversion fixes merely by installing it with a newer app; reconvert the original source for those fixes.

```text
ForzaPort/
  ForzaPort.exe
  README.txt
  Dependencies/
```

## Remove an import

Click **Undo / recover import**. Select the vehicle marked **Installed - available to undo**, using its operation number and date/time. Completed Undo records and already-removed imports are history only. Interrupted operations offer recovery.

The confirmation about saved-car dependencies still applies. Saves are never edited. Changed or dependent records can block Undo; do not delete receipts or overwrite the database to bypass a guard.

## Required resources

The tested setup is Azimuth 0.9.10 with official Extra Options 0.2.98. Microsoft .NET 8 x64 Runtime is external; Python is included. Conversion also requires the matching prepared ModelProbe helper, texture libraries, readable source database and source materials. Check setup explains missing requirements. See Dependencies/SETUP.txt.

Keep the supplied dependency notices and credits. Source game archives, databases and materials come from your own installation. Prepared resources are detected automatically; missing resources are listed by Check setup.

## Current limits

- Source geometry, textures, wheels and supported attachments are converted through generic passes; structural validation is separate from gameplay acceptance.
- Source colours use glossy native solid paint by default. Source special finishes, material appearance and AO rendering still need testing.
- Unsupported engine/country data uses explicit native approximations where supported. Stock tyre selection uses exact part identity, including stock slick/off-road choices.
- Driver translation requires a consistent complete native pose set. Hand IK and arbitrary cabin controllers remain incomplete. Compatible rigid needles can use native telemetry clips; digital surfaces can use a complete native donor display layout. Both require gameplay testing.
- New builds report source/native instrument declarations and candidate models. Name matches alone are not treated as runtime bindings. Source screen design and dial calibration are not reproduced by native fallbacks.

Source and tests: this repository. Maintainer entry point: docs/CODEBASE_MAP.md. Windows build instructions: scripts/README.md.

## Instruments

History tables now use readable dark/light colours. Compatible analogue needles are split from static geometry, bound to native telemetry bones and placed with a checked pivot compensation. Native clips/binds stay unchanged; incompatible axes, skins or missing controllers are reported. Digital screen materials can use the donor digital-gauge shader and existing XAML/resources; the donor UI is a fallback, not the source screen design. Geometry/UV preservation is checked offline; rendered layout and readings require testing.

Selectable source spacers and rear-steering physics are not implemented. Widebody geometry does not prove either. No third-party wheel-mod source or runtime is bundled or installed.

## Experimental suspension / steering

Off by default. To try it, close FH2, open Settings, tick **Experimental suspension / steering**, then click **Prepare / update runtime** and accept the experimental runtime prompt. This installs a guarded ForzaPort overlay built from current Extra Options 0.2.98 source. It is distinct from the standard official DLL and has its own backup receipt.

Reconvert the original FH6 archive with the option enabled. Existing converted ZIPs do not gain this feature. Supported source drift suspension is added as an **additional Race suspension** in the upgrade menu, using the source price and compatible spring/damper calibration. Source per-selection steering limits are applied, including explicit normal-limit restoration when drift is removed. Source response rates and hand/steering-wheel animation travel are not retargeted by this experiment.

Experimental ZIPs require the matching runtime on the recipient. Add Car rebases the steering maps to recipient IDs. Undo removes their car-owned sidecar and database rows; no loose model folder is installed. Undo experimental imports before switching back to the standard runtime. Never delete receipts to bypass that guard.

**Four-wheel steering is not implemented.** Stock and optional source rear-steering profiles are retained in the experimental report. There is no verified FH2 rear-wheel orientation/tyre-force hook, so neither visual nor physical rear steering is applied. This RC is experimental, not a claim of full vehicle parity.
