# Rerun 0.40.0 manifest compatibility

This branch contains the published `re_viewer` and `re_redap_browser` crates in a standalone workspace.
Their normalized manifests allow a compatible `wasm-bindgen` patch version, so a consuming workspace can generate matching JavaScript and WebAssembly bindings.

Rust source and assets match the published archives. Original registry `.cargo_vcs_info.json` files are omitted; `UPSTREAM.json` records archive checksums and provenance. Upstream MIT and Apache 2.0 licenses are included.

Archive comparisons passed for every copied file. Dependency resolution and vendoring passed with these manifests in the consuming workspace. Runtime compatibility is not yet verified.
