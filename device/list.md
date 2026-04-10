# Table of Contents

- [Command description](#command-description)
- [Command usage](#command-usage)
- [Example](#example)
- [Operating system support](#operating-system-support)

## Command description

This operation will show all known attached devices on your system and if they are supported for device dependent operations.

## Command usage

```text
USAGE:
    aaru device list [aaru-remote-host] [OPTIONS]

ARGUMENTS:
    [aaru-remote-host]    aaruremote host

OPTIONS:
    -h, --help    Prints help information
```

## Example

```bash
aaru device list
```

## Operating system support

| macOS | Linux | Windows |
| ----- | ----- | ------- |
| No¹   | Yes   | Yes     |

1. Device list and other device-access commands are not currently supported on macOS.