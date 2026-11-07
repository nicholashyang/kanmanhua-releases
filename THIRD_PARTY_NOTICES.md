# Third-party notices

KanManhua is licensed under Apache-2.0. It is an independent client and is not affiliated with Manhuagui or Mihon.

Mangabz and Komiic.cc are independent third-party sites and are not affiliated with this client.

## Keiyoushi extensions-source

Repository: https://github.com/keiyoushi/extensions-source

Reference revision: `1d3d7c4b3e876fb0c26ae3ade8113fb329af15fa`.

License: Apache License 2.0; full license is included in LICENSE.

- `app/src/main/java/keiyoushi/lib/lzstring/LZString.kt`: upstream implementation, originally inspired by pieroxy/lz-string; modified to enforce an optional decompressed output limit.
- `app/src/main/java/keiyoushi/lib/unpacker/{Unpacker,SubstringExtractor}.kt`: unmodified upstream implementations; Unpacker references Dean Edwards' packer.
- `source/ManhuaguiSource.kt`: adapted selectors and packed-image extraction from the upstream Manhuagui extension. Modified to provide independent suspend interfaces, explicit failure states, bounded input, strict URL construction, source IDs and request throttling. It does not include the extension host or unrelated extension behavior.

Additional reference revision for the new sources: `b647c92fd14801fda23e866d5a7da7d5fdd7ec92` (2026-11-07).

- `source/MangabzSource.kt`: adapted list/detail/chapter selectors, filter tuples, and packed-image decoding from `src/zh/mangabz`. Modified for independent suspend requests, bounded responses, lazy native image resolution, and source-scoped IDs.
- `source/KomiicSource.kt`: adapted GraphQL field names, pagination, chapter metadata, and image endpoint from `src/zh/komiic`. Modified to use `https://komiic.cc`, explicit error handling, stable IDs, and independent suspend requests.
- `source/SourceSessionInterceptor.kt`: Komiic token-expiry refresh behavior informed by the same upstream extension; cookies stay in the local Android WebView store.

The reading experience and library scheduling are informed by Mihon's public architecture and feature set: https://github.com/mihonapp/mihon (Apache-2.0). No Mihon application code is copied.

AndroidX, Kotlin, kotlinx.serialization, OkHttp, Coil, and jsoup retain their respective licenses. Third-party copyright and license notices in imported source files are retained.

