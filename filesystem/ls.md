# Table of Contents

- [Command description](#command-description)
- [Command usage](#command-usage)
- [Example](#example)
- [Operating system support](#operating-system-support)

## Command description

This operation will analyze and find all filesystems in a media dump, then list all the files that are contained in [supported filesystems](../faq/filesystems.md).

## Command usage

```text
USAGE:
    aaru filesystem list <image-path> [OPTIONS]

ARGUMENTS:
    <image-path>    Media image path

OPTIONS:
    -h, --help         Prints help information                                  
    -e, --encoding     Name of character encoding to use                        
    -O, --options      Comma separated name=value pairs of options to pass to   
                       filesystem plugin                                        
    -n, --namespace    Namespace to use for filenames
```

## Example

```bash
aaru filesystem list example.iso
```

## Operating system support

| macOS | Linux | Windows |
| ----- | ----- | ------- |
| Yes   | Yes   | Yes     |