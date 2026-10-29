# VIP Fucker — public patch assets (source preparation)

The manager source repository remains private. This repository publishes the
current three built-in root declarations plus a committed **source selection**
containing every compiled built-in patch family and its runtime support.

**Not an executable download catalog:** revision 29 of the Android manager still
bundles its patches/backend/loader. It does not download/apply these assets and is
not yet lightweight. Compiled Kotlin source is not a runtime DEX/module. Runtime
partitioning, a signed download catalog, bounded cache and Android bootstrap
integration must be completed before an on-demand build can be released.

`catalog/source-inventory.json` lists 25 package entries (including Telegram aliases),
their implemented/unavailable actions and exact source-payload SHA-256/size. Its
detached RSA signature uses a separate private administrator key, **not** the public
APK patch-signing key. Verify against an independently pinned public-key hash; a key
downloaded from this repository is not, by itself, a trust anchor.

CapCut: only five local Pro getter overrides are implemented. Effects/templates,
guest exports, network fixes, email login and watermark removal are not implemented
or device-verified. Local flags grant no purchase or server entitlement.

No target APK, private signing key, GitHub token or UI/account data is included.
Original source notices are preserved; see LICENSE and NOTICE.md. The source ZIP is
a patch/runtime selection, not a full standalone manager build-source distribution.
