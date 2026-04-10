# Table of Contents

- [Command description](#command-description)
- [Command usage](#command-usage)
- [Example](#example)
- [Operating system support](#operating-system-support)

## Command description

This operation will open a disc image and print information about the partitions and filesystems found inside it.

## Command usage

```text
USAGE:
    aaru filesystem info <image-path> [OPTIONS]

ARGUMENTS:
    <image-path>    Media image path

OPTIONS:
                         DEFAULT                                                
    -h, --help                      Prints help information                     
    -e, --encoding                  Name of character encoding to use           
    -p, --partitions     True       Searches and interprets partitions          
    -f, --filesystems    True       Searches and prints information about       
                                    filesystems
```

## Example

```bash
aaru filesystem info example.iso
```

## Operating system support

| macOS | Linux | Windows |
| ----- | ----- | ------- |
| Yes   | Yes   | Yes     |