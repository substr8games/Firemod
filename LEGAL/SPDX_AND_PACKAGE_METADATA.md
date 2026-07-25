# Firemod SPDX and Package Metadata
## Version 0.2

## Source-file header

```text
SPDX-FileCopyrightText: 2026 Giz@SUBSTR8Games
SPDX-License-Identifier: LicenseRef-FCIL-0.2
```

A file containing third-party material must use the correct additional or replacement declarations required for that material.

## Cargo

Use `license-file` for each first-party package:

```toml
[package]
license-file = "../../LICENSE"
```

Adjust the relative path to resolve from the package manifest. Do not write `license = "MIT"` or another SPDX license for first-party Firemod code.

## npm

```json
{
  "license": "SEE LICENSE IN LICENSE"
}
```

Ensure the referenced `LICENSE` file is included in the published package.

## Arch PKGBUILD

```bash
license=('LicenseRef-FCIL-0.2')
```

Install the canonical license:

```bash
install -Dm644 LICENSE "$pkgdir/usr/share/licenses/firemod/LICENSE"
```

Use project-relative paths in actual build logic.

## Public project description

> Firemod is source-available software distributed under the Firemod Capture Immunity License. Inspection, local execution, modification, community redistribution, and independent interoperability are permitted under the license. Proprietary capture, paid rehosting, closed redistribution, and unauthorized commercial packaging are prohibited.

## Repository license labels

Where a platform cannot identify FCIL, use:

- `Other`
- `Custom`
- `Source available`
- `LicenseRef-FCIL-0.2`

Do not select MIT as a placeholder.
