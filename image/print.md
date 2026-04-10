# Table of Contents

- [Command description](#command-description)
- [Command usage](#command-usage)
- [Example](#example)
- [Operating system support](#operating-system-support)

## Command description

This operation will print a hexadecimal dump of the chosen sector/block from the indicated media dump image to the console.

## Command usage

```text
USAGE:
    aaru image print-hex <image-path> [OPTIONS]

ARGUMENTS:
    <image-path>    Media image path

OPTIONS:
                          DEFAULT                                    
    -h, --help                       Prints help information         
    -l, --length          1          How many sectors to print       
    -r, --long-sectors               Print sectors with tags included
    -s, --start           0          Starting sector                 
    -w, --width           32         How many bytes to print per line
```

## Example

```bash
aaru image print-hex example.iso
```

## Operating system support

| macOS | Linux | Windows |
| ----- | ----- | ------- |
| Yes   | Yes   | Yes     |