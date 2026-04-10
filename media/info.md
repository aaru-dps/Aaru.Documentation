# Table of Contents

- [Command description](#command-description)
- [Command usage](#command-usage)
- [Example](#example)
- [Operating system support](#operating-system-support)

## Command description

This operation will request and show all information about the inserted media from a physical device. For information about supported physical devices check [the list of supported physical devices.](../faq/supported-devices.md)

## Command usage

```text
USAGE:
    aaru media info <device-path> [OPTIONS]

ARGUMENTS:
    <device-path>    Device path

OPTIONS:
    -h, --help             Prints help information                         
    -w, --output-prefix    Prefix for saving binary information from device
```

## Example

```bash
aaru media info /dev/rdisk2
```

## Operating system support

| macOS | Linux | Windows |
| ----- | ----- | ------- |
| No¹   | Yes   | Yes     |

1. Media info and other device-access commands are not currently supported on macOS.