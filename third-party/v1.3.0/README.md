# Third-party sources and build records — Video Compare v1.3.0

These materials are for inspecting or rebuilding the app's third-party dependencies. They are not needed to run Video Compare.

The FFmpeg9.0.2-2/mpv0.41.0-10 package versions and source-download set match the published v1.2.0 runtime. Use the preserved [exact source index and build records](../v1.2.0/README.md) in this tag, or the [v1.2.0-tagged index](https://github.com/skv89/SKV89s-Video-Compare-Tool/blob/v1.2.0/third-party/v1.2.0/README.md). Those records include official source URLs, hashes, patches, build recipes, dependency mappings and the stated librsvg preparation limitation.

Two GIO DLLs in v1.3.0 include an additional Windows registry-string correction. The portable package's `licenses/multimedia/glib-registry-fix/` contains the exact source reference, patch, build commands and binary/source hashes. The original GLib source package is in the existing index. Consult that included README when rebuilding or replacing these corrected DLLs.

The optional NVIDIA/LGPL runtime's corresponding source archives and replacement instructions remain inside `licenses/third-party-sources` and `licenses/GPU_LIBRARY_REPLACEMENT.md` in the portable package. Original component grants, notices and license options remain included. No private Video Compare application source or test data is included in these dependency records.

The distributor remains responsible for continued access to the exact upstream sources. A local archival copy is retained; broken source access requires an equivalent replacement. Sources are not an extra application download.
