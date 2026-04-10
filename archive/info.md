# Table of Contents

- [Command description](#command-description)
- [Command usage](#command-usage)
- [Example](#example)
- [Operating system support](#operating-system-support)

## Command description

This operation will show information about the selected archive file and the format Aaru detected for it.

## Command usage

```text
USAGE:
    aaru archive info <path> [OPTIONS]

ARGUMENTS:
    <path>    Archive file path

OPTIONS:
    -h, --help        Prints help information          
    -e, --encoding    Name of character encoding to use
```

## Example

```bash
aaru archive info example.zip
```

## Operating system support

| macOS | Linux | Windows |
| ----- | ----- | ------- |
| Yes   | Yes   | Yes     |