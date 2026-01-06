# MARC Validator

**MARC Validator** is a tool for validating bibliographic data in the **MARC 21** format.  
It focuses on validating coded MARC data fields — particularly the *leader*, fields *008*, *040*, *020*, and date-related fields (*008*, *260*, *264*).  
The tool takes into account cataloguing rules such as **RDA** and **AACR2**.

Its main goal is to identify errors that could cause issues during the transition to **Linked Data**, expected to become the standard for bibliographic data in the Czech Republic from **2028 onwards**.

***

## Features

- Validation of MARC 21 bibliographic data in MARCXML format.
- Detection of structural and logical errors in coded fields.
- Output as JSON or a human-readable text report.
- Compatible with cataloguing standards (RDA, AACR2).
- Extensible plugin-based architecture.
- Command-line interface for integration into workflows.

***

## Command-Line Tools

### `marc-validator`

A CLI tool for validating MARC records.  
Implemented in the [App::MARC::Validator](https://github.com/michal-josef-spacek/App-MARC-Validator) project,  
with validation logic in [MARC::Validator](https://github.com/michal-josef-spacek/MARC-Validator).

#### Syntax

```
marc-validator [-d] [-h] [-i id] [-l] [-o output_file] [-p] [-v] [--version] marc_xml_file..
```

#### Arguments

| Option | Description |
|--------|--------------|
| `-d` | Debug mode. |
| `-h` | Print help. |
| `-i id` | Record identifier defined by MARC field/subfield (default: `001`, e.g. `015a`). |
| `-l` | Print list of available plugins. |
| `-o output_file` | Save results to file (default: none). |
| `-p` | Pretty-print JSON output. |
| `-v` | Verbose mode. |
| `--version` | Print tool version. |
| `marc_xml_file..` | Input MARC XML file(s). |

#### Example

```
marc-validator records.xml
```

#### Output

- JSON file written to standard output.
- For each plugin, a list of detected errors is included.

***

### `marc-validator-report`

A CLI tool for generating human-readable validation reports.  
Repository: [App::MARC::Validator::Report](https://github.com/michal-josef-spacek/App-MARC-Validator-Report)  
CPAN: [App::MARC::Validator::Report](https://metacpan.org/dist/App-MARC-Validator-Report)

***

## Installation

Both tools are implemented in **Perl** and can be installed from [CPAN](https://metacpan.org) or via **Docker**.

### From CPAN

1. Install Perl interpreter:  
   - Debian: `apt-get install perl`  
   - Fedora: `dnf install perl-interpreter`
2. Install CPAN package manager:  
   - e.g. `dnf install perl-App-cpanminus`
3. Install the tools:  
   ```
   cpanm App::MARC::Validator
   cpanm App::MARC::Validator::Report
   ```
4. Check help:  
   ```
   marc-validator -h
   marc-validator-report -h
   ```

### Using Docker

#### MARC Validator

Image: [michaljosefspacek/marc-validator](https://hub.docker.com/r/michaljosefspacek/marc-validator)  
Pull and run:

```
docker pull michaljosefspacek/marc-validator:0.04
```

#### MARC Validator Report

Image: [michaljosefspacek/marc-validator-report](https://hub.docker.com/r/michaljosefspacek/marc-validator-report)  
Pull and run:

```
docker pull michaljosefspacek/marc-validator-report:0.01
```

***

## Test Data

Example datasets:  
[https://github.com/michal-josef-spacek/marc_validator_examples](https://github.com/michal-josef-spacek/marc_validator_examples)

***

## Repositories

- [App::MARC::Validator](https://github.com/michal-josef-spacek/App-MARC-Validator)
- [MARC::Validator](https://github.com/michal-josef-spacek/MARC-Validator)
- [MARC::Leader](https://github.com/michal-josef-spacek/MARC-Leader)
- [MARC::Leader::Utils](https://github.com/michal-josef-spacek/MARC-Leader-Utils)
- [MARC::Field008](https://github.com/michal-josef-spacek/MARC-Field008)
- [Data::MARC::Leader](https://github.com/michal-josef-spacek/Data-MARC-Leader)
- [Data::MARC::Field008](https://github.com/michal-josef-spacek/Data-MARC-Field008)

***

## License and Credits

© 2025 [Michal Josef Špaček](http://skim.cz) (<mailto:skim@cpan.org>)  
Licensed under the **BSD 2-Clause License**.

Development of this software has been supported by the **long-term strategic development of the National Library of the Czech Republic as a research organization**,  
funded by the **Ministry of Culture of the Czech Republic (DKRVO 2024–2028, Area 11: Linked Open Data)**.

***

## Version

**0.05**
