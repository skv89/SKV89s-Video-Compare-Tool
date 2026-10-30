# Third-party sources and build records — Video Compare v1.2.0

These materials are for inspecting, modifying or rebuilding third-party dependencies. **They are not needed to install or run Video Compare.** They contain no private application source.

## Obtain the matching sources

1. [MSYS2 source downloads](MSYS2_SOURCES.md) lists the exact FFmpeg 9.0.2-2, mpv 0.41.0-10 and dependency source packages, including incorporated header/build dependencies. Each official source package includes the upstream sources, packaging recipe and patches.
2. [Rust source downloads](RUST_SOURCES.md) provides the exact registry archives needed by the original lockfiles and the documented librsvg adjustment.
3. [Download build records](build-records.zip) for the binary `.BUILDINFO`/`.PKGINFO`, readable recipes, original Cargo locks and recorded preparation information. The archive inventory verifies every included file.
4. [SOURCE_INDEX.json](SOURCE_INDEX.json) contains every exact download URL, version, SHA-256, byte count and dependency mapping. [RUNTIME_FILES.json](RUNTIME_FILES.json) maps bundled files and hashes to the original binary packages.

All source downloads are public and free; no registration or request by email is needed. Download the versions listed here, rather than substituting a project's latest release. SHA-256 checksums identify the collected matching source archives. Original copyrights and licenses remain in the archives, and collected notices and license texts accompany the portable app.

## Build and replace dependencies

Use a Windows MSYS2 UCRT64 build environment. Extract the selected `.src.tar.zst`, follow its PKGBUILD, and use the build tools/dependency versions recorded in `.BUILDINFO`. Recipes include source preparation, patches, configure/compiler options and installation steps. [MSYS2 package-building instructions](https://www.msys2.org/wiki/Creating-Packages/) describe the tools. General build tools are not bundled as runnable software.

Registry `.crate` archives can populate a Cargo cache or local source directory; preserve the lockfile checksums. Recipes determine target/features. These records do not promise a byte-identical rebuild.

In a backup copy of the portable app, compatible modified EXE/DLL files can replace the corresponding files together in `tools/ffmpeg/bin` or `tools/mpv`. There is no signature/hash lock preventing replacement. Keep compatible DLL interfaces together. The app launches FFmpeg and mpv as separate programs. The optional NVIDIA/LGPL search runtime has separate source archives and replacement instructions already included in `licenses/third-party-sources` and `licenses/GPU_LIBRARY_REPLACEMENT.md` in the portable package.

## Distribution terms and source access

This distribution uses GPL version 3 for GPL-covered multimedia components whose grants permit version 3, and LGPL version 3 for LGPL-covered multimedia libraries whose grants permit a later version. Original notices and recipients' original license options are preserved. The accompanying GPL 3 and LGPL 3 texts apply to these distribution choices; permissive and other component licenses also remain applicable. The application itself is not relicensed by this notice.

[GPL 3 section 6(d)](https://www.gnu.org/licenses/gpl-3.0.html#section6) permits corresponding source on another server with clear directions alongside the binary. The exact official source links above implement that route. The distributor remains responsible for continued source availability; a broken link must be replaced by equivalent access to the same matching source. A local archival copy is retained for recovery. There is no requirement for users to download sources to use the app.

Some package catalog labels omit later-version options. The accompanying build records retain the relevant original grants for jbigkit, LAME, libdatrie, libgme, libplacebo, Pango, x264, x265, Xvid, libtasn1 and GMP. The libcaca library source grant is permissive (WTFPL); its original notices are retained. MPL-covered sources are provided by the same exact public source links under their original terms. This index does not change any original grant.

## librsvg preparation record

The official librsvg 2.63.4-1 recipe applies a patch and runs `cargo update -p windows-sys@0.61.2 --precise 0.60.2` before its frozen build. The historical post-prepare Cargo.lock was not recovered. The original lock, exact recipe/patch and compiler/build environment are retained. The index supplies all original registry sources and the compatible introduced windows-sys/targets/architecture/link sources with official index checksums. This covers the documented adjustment; it does not attest which compatible 0.53.x patch was resolved historically.

Windows system DLLs and the installed NVIDIA driver are supplied by the operating system/driver installation, not these source records.
