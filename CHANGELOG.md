# Changelog

All notable changes to lsc are recorded here. The format follows
[Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and versions follow
[Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.2.0](https://github.com/unsigned-gg/lsc/compare/v0.1.0...v0.2.0) - 2026-10-18

### Added

- **LeanSpec status aliases** (SPEC-0001):
  - `proposed` and `draft` read as `planned`;
  - `accepted` reads as `in-progress`;
  - `implemented` reads as `complete`.
- **Folder-layout specs**, `specs/NNN-slug/README.md`, alongside flat `specs/NNNN-slug.md`. In the folder layout, identity comes from the folder name (SPEC-0005).
- **Schema-v4 validation receipts** with validity fingerprints (XT-10).
- **projectfile:** SPEC-0003 requirements 15, 16 and 17; `XtaskCompiler::generate`; a per-stage summary; `--goal`; the TOOLS table; and the spawn-mode env scrub.
- **cargo xtask:** the gates, `ci` and `install` (SPEC-0004, XT-1 to XT-8), plus the xwork stage-order compiler with its dispatch mode and drift check.

### Changed

- **BREAKING:** the crates `ls` and `ls-domain` are renamed to `lsc` and `lsc-core`.
- lsc is dual-licensed under Apache-2.0 OR MIT.

### Fixed

- **projectfile:**
  - a tool pin row with a missing field is rejected;
  - goal names are escaped in generated xtask code;
  - an empty `--goal` closure lowers to an empty table.
