# Table of Contents

- [Command description](#command-description)
- [Command usage](#command-usage)
- [Example](#example)
- [Operating system support](#operating-system-support)

## Command description

This operation will list the contents of the selected archive file.

## Command usage

```text
USAGE:
    aaru archive list <path> [OPTIONS]

ARGUMENTS:
    <path>    Archive file path

OPTIONS:
    -h, --help           Prints help information          
    -e, --encoding       Name of character encoding to use
    -l, --long-format    Use long format
```

## Example

```bash
aaru archive list example.zip
```

## Operating system support

| macOS | Linux | Windows |
| ----- | ----- | ------- |
| Yes   | Yes   | Yes     |