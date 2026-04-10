# Table of Contents

- [Command description](#command-description)
- [Command usage](#command-usage)
- [Example](#example)
- [Operating system support](#operating-system-support)

## Command description

This operation will update the master database and optionally clear the master and local databases.

## Command usage

```text
USAGE:
    aaru database update [OPTIONS]

OPTIONS:
    -h, --help         Prints help information               
        --clear        Clear existing main database          
        --clear-all    Clear existing main and local database
```

## Example

```bash
aaru database update --clear-all
```

## Operating system support

| macOS | Linux | Windows |
| ----- | ----- | ------- |
| Yes   | Yes   | Yes     |