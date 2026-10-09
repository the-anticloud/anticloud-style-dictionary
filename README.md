# STYLE DICTIONARY

![license](https://img.shields.io/badge/license-license-blue) ![offline-first](https://img.shields.io/badge/offline--first-air--gap-green) ![audit](https://img.shields.io/badge/audit-SHA3--256-orange) ![category](https://img.shields.io/badge/category-design_tools-lightgrey)

> Anticloud-hardened packaging of the upstream project `STYLE_DICTIONARY` in category **DESIGN TOOLS**. Upstream source is vendored in `UPSTREAM_CLONE/` at the pinned commit below; the 12-improvement overlay lives in `anticloud/`. Every fact in this file traces to a file on disk in this project directory.

**Category:** DESIGN TOOLS · **Upstream:** https://github.com/style-dictionary/style-dictionary · **Upstream pin:** `8710de9f9dc5e65fad40a5fba979699ed2f8b3cb` · **Vendor:** Anticloud FZ LLE

---

## What This Project Does

<pre>
<a href="https://styledictionary.com/versions/v4/migration/">What's new in Style Dictionary 4.0!</a>
</pre>

<img src="docs/src/assets/logo.png" alt="Style Dictionary logo and mascot" title="&quot;Pascal&quot;" width="100" align="right" />

[![npm version](https://img.shields.io/npm/v/style-dictionary.svg?style=flat-square)](https://badge.fury.io/js/style-dictionary)
[![license](https://img.shields.io/npm/l/style-dictionary.svg?style=flat-square)](https://github.com/style-dictionary/style-dictionary/blob/main/LICENSE)
[![PRs welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](https://github.com/style-dictionary/style-dictionary/blob/main/CONTRIBUTING.md#submitting-pull-requests)
[![GitHub Workflow Status](https://github.com/style-dictionary/style-dictionary/actions/workflows/verify.yml/badge.svg)](https://github.com/style-dictionary/style-dictionary/actions)
[![downloads](https://img.shields.io/npm/dm/style-dictionary.svg?style=flat-square)](https://www.npmjs.com/package/style-dictionary)

# Style Dictionary

[See documentation](http://styledictionary.com)

> _Style once, use everywhere._

A Style Dictionary uses design tokens to define styles once and use those styles on any platform or language. It provides a single place to create and edit your styles, and exports these tokens to all the places you need - iOS, Android, CSS, JS, HTML, sketch files, style documentation, etc. It is available as a CLI through npm, but can also be used like any normal node module if you want to extend its functionality.

When you are managing user experiences, it can be quite challenging to keep styles consistent and synchronized across multiple development platforms and devices. At the same time, designers, developers, PMs and others must be able to have consistent and up-to-date style documentation to enable effective work and communication. Even then, mistakes inevitably happen and the design may not be implemented accurately. Style Dictionary solves this by automatically generating style definitions across all platforms from a single source - removing roadblocks, errors, and inefficiencies across your workflow.

## Watch the Demo on YouTube

[![Watch the video](/docs/src/assets/fake_player.png)](http://youtu.be/1HREvonfqhY)

## Experiment in the playground

Try the browser-based Style Dictionary playground: [https://www.style-dictionary-play.dev/](https://www.style-dictionary-play.dev/), built by the folks at [\<div\>RIOTS](https://divriots.com/).

## Contents

- [Installation](#installation)
- [Usage](#usage)
- [Example](#example)
- [Quick Start](#quick-start)
- [Design Tokens](#design-tokens)
- [Extending](#extending)
- [Contributing](#contributing)
- [License](#license)

## Installation

_Note that you must have node (and npm) installed._

If you want to use the CLI, you can install it globally via npm:

```bash
$ npm install -g style-dictionary
```

Or you can install it like a normal npm dependency. This is a build tool and you are most likely going to want to save it as a dev dependency:

```bash
$ npm install -D style-dictionary
```

If you want to install it with yarn:

```bash
$ yarn add style-dictionary --dev
```

## Usage

### CLI

```bash
$ style-dictionary build
```

Call this in the root directory of your project. The only thing needed is a `config.json` file. There are also arguments:

| Flag                    | Short Flag | Description                                                |
| ----------------------- | ---------- | ---------------------------------------------------------- |
| --config \[path\]       | -c         | Set the config file to use. Must be a .json file           |
| --platform \[platform\] | -p         | Only build a specific platform defined in the config file. |
| --help                  | -h         | Display help content                                       |
| --version               | -v         | Display the version                                        |

### Node

You can also use the style dictionary build system in node if you want to [extend](#extending) the functionality or use it in another build system like Grunt or Gulp.

```javascript
const StyleDictionary = require('style-dictionary').extend('config.json');

StyleDictionary.buildAllPlatforms();
```

The `.extend()` method is an overloaded method that can also take an object with the configuration in the same format as a config.json file.

```javascript
import { formats, transformGroups } from 'style-dictionary/enums';

const StyleDictionary = require('style-dictionary').extend({
  source: ['tokens/**/*.json'],
  platforms: {
    scss: {
      transformGroup: transformGroups.scss,
      buildPath: 'build/',
      files: [
        {
          destination: 'variables.scss',
          format: formats.scssVariables,
        },
      ],
    },
    // ...
  },
});

StyleDictionary.buildAllPlatforms();
```

## Example

[Take a look at some of our examples](examples/)

A style dictionary is a collection of design tokens, key/value pairs that describe stylistic attributes like colors, sizes, icons, motion, etc. A style dictionary defines these design tokens in JSON or Javascript files, and can also include static assets like images and fonts. Here is a basic example of what the package structure can look like:

```
├── config.json
├── tokens/
│   ├── size/
│       ├── font.json
│   ├── color/
│       ├── font.json
│   ...
├── assets/
│   ├── fonts/
│   ├── images/
```

### config.json

This tells the style dictionary build system how and what to build. The default file path is `config.json` or `config.js` in the root of the project, but you can name it whatever you want by passing in the `--config` flag to the [CLI](https://styledictionary.com/getting-started/using_the_cli/).

```json
{
  "source": ["tokens/**/*.json"],
  "platforms": {
    "scss": {
      "transformGroup": "scss",
      "buildPath": "build/",
      "files": [
        {
          "destination": "scss

*(excerpt; full text in `UPSTREAM_CLONE/`)*

*Quoted from the upstream `README.md` file in `UPSTREAM_CLONE/`.*
Project-specific facts detected in this directory:

- Ecosystem: **Node.js / npm** (manifests: package.json, package-lock.json; scanned in UPSTREAM_CLONE)
- Top-level source layout: `__integration__/`, `__node_tests__/`, `__perf_tests__/`, `__tests__/`, `bin/`, `examples/`, `lib/`, `patches/`, `scripts/`, `snapshot-plugin/`, `types/`
- Snapshot size: **918 files**, **49937 lines of code** (measured; see Benchmarks)
- Primary languages: `.js` (317), `.json` (165), `.svg` (58), `.md` (54), `.png` (39), `.xml` (36)
- Upstream commit pinned for this packaging: `8710de9f9dc5e65fad40a5fba979699ed2f8b3cb`

---

## Installation

- [Usage](#usage)
- [Example](#example)
- [Quick Start](#quick-start)
- [Design Tokens](#design-tokens)
- [Extending](#extending)
- [Contributing](#contributing)
- [License](#license)

*Section quoted from the upstream readme.*
Overlay install (this project):

```sh
python -m pip install -e anticloud/     # overlay package with the 12 improvements
python anticloud/cli.py --help          # 13 subcommands, JSON stdout
```

---

## Usage

A Style Dictionary uses design tokens to define styles once and use those styles on any platform or language. It provides a single place to create and edit your styles, and exports these tokens to all the places you need - iOS, Android, CSS, JS, HTML, sketch files, style documentation, etc. It is available as a CLI through npm, but can also be used like any normal node module if you want to extend its functionality.

When you are managing user experiences, it can be quite challenging to keep styles consistent and synchronized across multiple development platforms and devices. At the same time, designers, developers, PMs and others must be able to have consistent and up-to-date style documentation to enable effective work and communication. Even then, mistakes inevitably happen and the design may not be implemented accurately. Style Dictionary solves this by automatically generating style definitions across all platforms from a single source - removing roadblocks, errors, and inefficiencies across your workflow.

*Section quoted from the upstream readme.*
Anticloud overlay CLI (available in every project):

```sh
python anticloud/cli.py --help     # 13 subcommands, JSON stdout
python anticloud/cli.py checks     # run the 16-check suite
```

---

## API

> _Style once, use everywhere._

A Style Dictionary uses design tokens to define styles once and use those styles on any platform or language. It provides a single place to create and edit your styles, and exports these tokens to all the places you need - iOS, Android, CSS, JS, HTML, sketch files, style documentation, etc. It is available as a CLI through npm, but can also be used like any normal node module if you want to extend its functionality.

When you are managing user experiences, it can be quite challenging to keep styles consistent and synchronized across multiple development platforms and devices. At the same time, designers, developers, PMs and others must be able to have consistent and up-to-date style documentation to enable effective work and communication. Even then, mistakes inevitably happen and the design may not be implemented accurately. Style Dictionary solves this by automatically generating style definitions across all platforms from a single source - removing roadblocks, errors, and inefficiencies across your workflow.

*Section quoted from the upstream readme.*
---

## Dependencies

| Metric | Value |
|--------|-------|
| Ecosystem | Node.js / npm |
| Manifests detected | package.json, package-lock.json |
| Files in snapshot | 918 |
| Lines of code | 49937 |
| Dependency references | 109 |
| Dependencies by ecosystem | npm: 109 |
| Upstream license | Apache-2.0 |
| Overlay license | Anticommons 0.1.0 |

Top dependency references recorded in the benchmark snapshot:

| Ecosystem | Name | Version | Source file |
|-----------|------|---------|-------------|
| npm | @bundled-es-modules/deepmerge | ^4.3.2 | package.json |
| npm | @bundled-es-modules/glob | ^13.0.6-hotfix.0 | package.json |
| npm | @bundled-es-modules/memfs | ^4.17.0 | package.json |
| npm | @zip.js/zip.js | ^2.7.44 | package.json |
| npm | chalk | ^5.3.0 | package.json |
| npm | change-case | ^5.3.0 | package.json |
| npm | colorjs.io | ^0.5.2 | package.json |
| npm | commander | ^12.1.0 | package.json |
| npm | is-plain-obj | ^4.1.0 | package.json |
| npm | json5 | ^2.2.2 | package.json |
| npm | path-unified | ^0.2.0 | package.json |
| npm | prettier | ^3.3.3 | package.json |
| npm | tinycolor2 | ^1.6.0 | package.json |
| npm | @astrojs/check | ^0.9.10 | package.json |
| npm | @astrojs/markdown-remark | ^7.3.1 | package.json |
| ... | (94 more) | | |

Pinned lockfile: `anticloud/requirements.lock` (hash-pinned, PEP 508). SBOM: `sbom.cdx.json` (CycloneDX 1.5, pinned to the upstream SHA).

---

## Configuration

| Flag                    | Short Flag | Description                                                |
| ----------------------- | ---------- | ---------------------------------------------------------- |
| --config \[path\]       | -c         | Set the config file to use. Must be a .json file           |
| --platform \[platform\] | -p         | Only build a specific platform defined in the config file. |
| --help                  | -h         | Display help content                                       |
| --version               | -v         | Display the version                                        |

*Section quoted from the upstream readme.*
Overlay configuration (Anticloud):

- `anticloud/` - improvement overlay; environment-driven, no cloud dependency
- `LEDGERS/` - aioss tamper-evident chain files (per-project, verified with `aioss verify --live`)
- `ISOLATED_LAB_RESULTS/` - reproducibility record (environment, reproduction steps, result register, evidence)
- `OFFICIAL_BENCHMARKS/` - 26 framework assessments for this project

---

## Contributing

*Excerpt from upstream `CONTRIBUTING.md`:*

# Contributing to the Style Dictionary

This is a labor of love, and we work hard to provide a useful framework. We greatly value feedback and contributions from our community. Whether it's a bug report, new feature, correction, or additional documentation, we welcome your issues and pull requests. Please read through this document before submitting any issues or pull requests to ensure we have all the necessary information to effectively respond to your bug report or contribution.

## Filing Bug Reports

You can file bug reports on the [GitHub issues][issues] page.

If you are filing a report for a bug or regression in the framework, it's extremely helpful to provide as much information as possible when opening the original issue. This helps us reproduce and investigate the possible bug without having to wait for this extra information to be provided. Please read the following guidelines prior to filing a bug report.

1. Search through existing [issues][issues] to ensure that your specific issue has not yet been reported. If it is a common issue, it is likely there is already a bug report for your problem.
2. Ensure that you have tested the latest version of the framework. Although you may have an issue against an older version of the framework, we cannot provide bug fixes for old versions. It's also possible that the bug may have been fixed in the latest release.
3. Provide as much information about your environment, npm version, and relevant dependencies as possible. For example, let us know what version of Node.js you are using, what other node modules, what ES version, etc. If possible, send us a github project we can take a look at.
4. Provide a minimal test case that reproduces your issue or any error information you related to your problem. We can provide feedback much more quickly if we know what operations you are calling in the framework. If you cannot provide a full test case, provide as much code as you can to help us diagnose the problem. Any relevant information should be provided as well, like whether this is a persistent issue, or if it only occurs some of the time.

## Submitting Pull Requests

We are always happy to receive code and documentation contributions to the framework. Please be aware of the following notes prior to opening a pull request:

1. This framework is released under the [Apache license][license]. Any code you submit will be released under that license. For substantial contributions, we may ask you to sign a [Contrib

Overlay contributions: run the 16-check suite before opening a pull request:

```sh
python anticloud/bench/runner.py --cwd anticloud
```

---

## License

**Upstream license: Apache-2.0** (evidence: `LICENSE` in the upstream snapshot).

License file excerpt:

```text
                                 Apache License
                           Version 2.0, January 2004
                        http://www.apache.org/licenses/

TERMS AND CONDITIONS FOR USE, REPRODUCTION, AND DISTRIBUTION

1.  Definitions.

    "License" shall mean the terms and conditions for use, reproduction,
    and distribution as defined by Sections 1 through 9 of this document.

    "Licensor" shall mean the copyright owner or entity authorized by
    the copyright owner that is granting the License.

    "Legal Entity" shall mean the union of the acting entity and all
    other entities that control, are controlled by, or are under common
    control with that entity. For the purposes of this definition,
    "control" means (i) the power, direct or indirect, to cause the
    direction or management of such entity, whether by contract or
    otherwise, or (ii) ownership of fifty percent (50%) or more of the
```

### Anticommons 0.1.0 overlay

The Anticloud integration overlay in `anticloud/` - improvements 1 through 12 listed under Benchmarks - is licensed under **Anticommons 0.1.0**. Upstream code remains under its original Apache-2.0 terms. See `ANTICOMMONS_LICENSE.md` in this directory for the overlay terms and contact.

SPDX: `Apache-2.0` (upstream) + Anticommons 0.1.0 (overlay, dual).

---

## Upstream

- **Project:** `STYLE_DICTIONARY` (category: DESIGN TOOLS)
- **Upstream URL:** https://github.com/style-dictionary/style-dictionary
- **Pinned commit (SHA):** `8710de9f9dc5e65fad40a5fba979699ed2f8b3cb`
- **Branch:** main
- **Pin provenance:** GitHub API commits/main. The parent-project stamp is explicitly rejected for this project.
- **Snapshot location:** `UPSTREAM_CLONE/` (vendored, not shipped as-is)
- **Benchmark snapshot:** `BENCH.json`

---

## Benchmarks

Measured by the Anticloud assurance suite. Every value below is read from this
project's `BENCH.json`, produced by a real run — the SHA3-256 of that file is
`5eebabbdffab6d112c6697d51fcc034562b225567ae970f5324de3d0c2b868cb`.

| Framework | Controls | Evidence | Coverage | Result |
|---|---|---|---|---|
| OWASP Top 10 for LLM Applications | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| OWASP Top 10 (2021) | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| SOC 2 Type II readiness | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| NIST AI Risk Management Framework | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| NIST SP 800-53 Rev. 5 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| NIST Cybersecurity Framework 2.0 | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| FedRAMP Rev. 5 | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| PCI DSS v4.0.1 | 11 controls mapped | 11 with evidence | 100.0% | PASS |
| ISO/IEC 27001:2022 | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| MITRE ATT&CK v16 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| ML Technology Readiness Level | TRL 8 | 8/8 criteria | | PASS |

**Overall: 16/16 checks passing.**

See `ISOLATED_LAB_RESULTS/03_Result_Register.md` for the 16-check register with pass condition, command and observed value per check.

Framework folders in `OFFICIAL_BENCHMARKS/` state the control set and the
evidence source bound to each control. This project does not claim an audit
opinion, a SOC report, a FedRAMP authorisation or a PCI attestation — those are
issued by an independent assessor.



## Archives and Permanent Records

| Platform | Identifier | Volume |
|---|---|---|
| Harvard Dataverse | DOI 10.7910/DVN/YMJKOG | 145 citable datasets |
| AIOSS verification kit | DOI 10.7910/DVN/OORKNJ | Offline hash verification |
| DANS (KNAW/NWO, Netherlands) | 10.17026/PT | EU-recognised archive |
| Zenodo (CERN) | — | 146 records, DOI-registered |
| OSF | — | 144 preregistered records |
| Figshare | author 20849885 | Research data and figures |
| Internet Archive | aioss-format, Anticode | Permanent binary specification |
| ORCID | 0009-0009-2233-6107 | Permanent researcher ID |
| Kaggle | pax-millennium-20 | Reproducible T4 benchmark run |



## Press and Independent Publication

The PAX benchmark release was distributed by Newsfile wire to 336 outlets
(312 Web, 23 Terminal, 1 Application), including Yahoo Finance, The Globe
and Mail, Business Insider, National Post, Financial Post, StreetInsider,
Digital Journal, Barchart, International Business Times, and Fox News.
Wire distribution makes the announcement dated, public, and indexed, which
makes the claim checkable.

