# Table of Contents

- [Command description](#command-description)
- [Command usage](#command-usage)
- [Example](#example)
- [Operating system support](#operating-system-support)

## Command description

This operation will read the media inserted in the physical device and measure how fast it can be read sequentially.
It's not intended as a benchmark, but as a detector of damaged sectors, sectors that are losing readability, etc. When
finished it will check how fast can the device seek and report speed statistics.

## Command usage

```text
USAGE:
    aaru media scan <device-path> [OPTIONS]

ARGUMENTS:
    <device-path>    Device path

OPTIONS:
                                DEFAULT                                         
    -h, --help                             Prints help information              
    -m, --mhdd-log                         Write a log of the scan in the format
                                           used by MHDD                         
    -b, --ibg-log                          Write a log of the scan in the format
                                           used by ImgBurn                      
        --use-buffered-reads    True       For MMC/SD, use OS buffered reads if 
                                           CMD23 is not supported
```

## Example

```bash
aaru media scan /dev/rdisk2
```

## Operating system support

| macOS | Linux | Windows |
| ----- | ----- | ------- |
| No¹   | Yes   | Yes     |

1. Media scan and other device-access commands are not currently supported on macOS.