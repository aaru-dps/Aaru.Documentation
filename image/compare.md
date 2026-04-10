# Table of Contents

- [Command description](#command-description)
- [Command usage](#command-usage)
- [Example](#example)
- [Operating system support](#operating-system-support)

## Command description

This operation will compare two media dumps and print all differences between them. Dumps can be in different formats.

## Command usage

```text
USAGE:
    aaru image compare <image-path1> <image-path1> [OPTIONS]

ARGUMENTS:
    <image-path1>    First media image path 
    <image-path1>    Second media image path

OPTIONS:
    -h, --help            Prints help information     
    -r, --long-sectors    Use long sectors (with tags)
```

## Example

```bash
aaru image compare disc1.iso disc2.iso
```

## Operating system support

| macOS | Linux | Windows |
| ----- | ----- | ------- |
| Yes   | Yes   | Yes     |