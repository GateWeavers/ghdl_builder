# ghdl_builder

Prebuilt and pinned GHDL binary archives with immutable release tags and Bazel-compatible checksums (`SHA-256` and `integrity`).

## Purpose

Upstream `ghdl/ghdl` nightly releases overwrite a floating `nightly` tag, which breaks reproducible Bazel fetches (`http_archive` / `repository_rule`). This repository mirrors and pins specific GHDL builds under immutable tags (`v<major>.<minor>-nightly.<short_sha>`) so toolchains can fetch stable URLs with fixed integrity hashes.

## Available Archives

Each pinned release provides `.tar.gz` archives for `x86_64` across:
- **Backends:** `gcc`, `llvm`, `mcode`
- **Distributions:** `ubuntu24.04`, `ubuntu26.04`
