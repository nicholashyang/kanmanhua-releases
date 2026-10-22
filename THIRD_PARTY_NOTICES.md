# Third-party notices

KanManhua is licensed under Apache-2.0. It is an independent client and is not affiliated with Manhuagui or Mihon.

## Keiyoushi extensions-source

Repository: https://github.com/keiyoushi/extensions-source

Reference revision: `1d3d7c4b3e876fb0c26ae3ade8113fb329af15fa`.

License: Apache License 2.0; full license is included in LICENSE.

- `app/src/main/java/keiyoushi/lib/lzstring/LZString.kt`: upstream implementation, originally inspired by pieroxy/lz-string; modified to enforce an optional decompressed output limit.
- `app/src/main/java/keiyoushi/lib/unpacker/{Unpacker,SubstringExtractor}.kt`: unmodified upstream implementations; Unpacker references Dean Edwards' packer.
- `source/ManhuaguiSource.kt`: adapted selectors and packed-image extraction from the upstream Manhuagui extension. Modified to provide independent suspend interfaces, explicit failure states, bounded input, strict URL construction, source IDs and request throttling. It does not include the extension host or unrelated extension behavior.

The reading experience and library scheduling are informed by Mihon's public architecture and feature set: https://github.com/mihonapp/mihon (Apache-2.0). No Mihon application code is copied.

AndroidX, Kotlin, kotlinx.serialization, OkHttp, Coil, and jsoup retain their respective licenses. Third-party copyright and license notices in imported source files are retained.
