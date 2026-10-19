# Rerun 0.38.1 manifest compatibility

We keep the published `re_viewer` and `re_redap_browser` crates in a standalone workspace.
Each normalized manifest changes `wasm-bindgen = "=0.2.126"` to `wasm-bindgen = "0.2.126"` in its WebAssembly dependencies.
This lets Cargo resolve a newer compatible dependency version.

The Rust source and assets match the published crate archives.
We omit the archives’ original `.cargo_vcs_info.json` files because Cargo records this fork’s revision instead.
`UPSTREAM.json` records the archive URLs, checksums, and changes.

Both packages use the upstream MIT or Apache 2.0 licenses included here.

## Validation

Offline Cargo resolution, native Reindeer vendoring, and isolated native split rule generation passed for the patched packages.
The remaining Rerun packages resolve from crates.io.
Production builds and WebAssembly compatibility have not been verified.
