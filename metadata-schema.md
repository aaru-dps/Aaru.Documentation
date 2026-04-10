# Table of Contents

- [Command description](#command-description)
- [Command usage](#command-usage)
- [Example](#example)
- [Operating system support](#operating-system-support)

## Command description

This operation will generate the JSON schema used by Aaru metadata files and write it to the selected output path.

## Command usage

```text
USAGE:
    aaru metadata-schema <output> [OPTIONS]

ARGUMENTS:
    <output>    Output file for the JSON schema

OPTIONS:
    -h, --help              Prints help information        
    -v, --verbose           Shows verbose output           
    -d, --debug             Shows debug output from plugins
        --logfile <PATH>    Path to log file               
        --pause             Pauses before exiting
```

## Example

```bash
aaru metadata-schema metadata-schema.json
```

## Operating system support

| macOS | Linux | Windows |
| ----- | ----- | ------- |
| Yes   | Yes   | Yes     |