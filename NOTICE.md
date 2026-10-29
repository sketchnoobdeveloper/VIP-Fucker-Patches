# Licensing and attribution

**Free forever · Developed by Sketch Noob Developer.** Support is optional and
does not unlock features. This product statement and developer credit do not
replace the existing source license or third-party rights.

VIP Fucker source: **GPL-3.0-only**, copyright © 2026 VIP Fucker contributors.
Provided WITHOUT ANY WARRANTY. Redistribution and modification are permitted
under GNU GPL version 3; the complete text is in `LICENSE`. Source accompanies
the development APK.

The original VF monogram and bundled identification artwork were created for
this module. Installed target icons are displayed from Android's PackageManager,
not repackaged from target APKs. App names and marks belong to their respective
owners; no affiliation or endorsement is implied.

The current revision excludes the NexAlloy Strava/AllTrails source plans and the
1DM hook. Their historical attribution remains in Git history and the earlier
source delivery. No NexAlloy-derived plan is included in the current module DEX.
The existing GPL-3.0 license remains unchanged.

## Rootless loader and patching backend

`app/src/main/assets/nonroot-loader/*` and `libs/nonroot-backend.jar` are derived
from **JingMatrix/LSPatch v1.2 (487)**, commit
`0dc50f42503711b14f5e2bb217c2bdd6321ce5be`, released under
**GPL-3.0**. Upstream: https://github.com/JingMatrix/LSPatch. Release SHA-256:
`d238fdc414d121b7fa454d8b4ccf420df3a8c97d563761861ff92bd9c5da2165`.
Exact file hashes and the extraction rules are in `third_party/lspatch/vendor-lock.json`
and `tools/vendor_nonroot.py`. The default upstream keystores and command-line
front end are not shipped. `nonroot/NonRootEngine.kt` is a modified adaptation of
`ApkPatcher` with integrated mode only, optional level-2 app-local signature compatibility, no version
downgrade, and a single embedded module. Corresponding source for this GPL work
is the delivered source ZIP. The upstream loader native libraries are included
unmodified for arm64-v8a, armeabi-v7a, x86 and x86_64.

`assets/nonroot-signer/patch-signer.jks` and `.p12` are this project's intentionally
public shared patch key, not upstream defaults, the original target key or the
private manager release key. The shipped key/password are extractable by design;
they must not authorize privileged access or identify trusted production releases.

AndroidX/Compose and Kotlin are unmodified dependencies under their respective
upstream licenses. The legacy Xposed API JAR is compile-only and its definitions
are excluded from the module DEX. Telegram and TM target classes, native
libraries, APKs, account data and credentials are not bundled.

## Smali method recipe engine

The direct recipe route uses **Google smali / baksmali / dexlib2 3.0.3**
(`com.android.tools.smali` Maven artifacts), under BSD 3-Clause with Apache 2.0
Android Open Source Project portions. Copyright Ben Gruver, Google LLC and AOSP.
Upstream source and notices: https://github.com/google/smali (version `3.0.3`).
ANTLR runtime is under the BSD license; StringTemplate is under BSD licensing.
Preserve the dependency-provided copyright/license notices when redistributing.
See `third_party/smali/NOTICE.md` and the complete `third_party/smali/LICENSE`,
exported as `SMALI-LICENSE.txt` with the release. Android packaging excludes the
dependency's root license resource; distribute the accompanying license materials.
These libraries assemble/disassemble DEX; no target APK or target runtime is bundled.
Guava, JCommander and JSR305 are supplied by the pinned backend rather than duplicated.
