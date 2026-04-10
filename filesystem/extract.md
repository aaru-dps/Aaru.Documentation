# Table of Contents

- [Command description](#command-description)
- [Command usage](#command-usage)
- [Example](#example)
- [Operating system support](#operating-system-support)

## Command description

This operation will analyze and find all filesystems in a media dump, then extract the files that are contained in [supported filesystems.](../faq/filesystems.md)

## Command usage

```text
USAGE:
    aaru filesystem extract <image-path> <output-dir> [OPTIONS]

ARGUMENTS:
    <image-path>    Media image path                                            
    <output-dir>    Directory where extracted files will be created. Will abort 
                    if it exists                                                

OPTIONS:
    -h, --help         Prints help information                                  
    -e, --encoding     Name of character encoding to use                        
    -O, --options      Comma separated name=value pairs of options to pass to   
                       filesystem plugin                                        
    -x, --xattrs       Extract extended attributes if present                   
        --volume       Extract only from the specified volume number            
                       (0-indexed). If not specified, extracts from all volumes 
    -n, --namespace    Namespace to use for filenames
```

## Example

```bash
aaru filesystem extract example.iso output
```

## Operating system support

| macOS | Linux | Windows |
| ----- | ----- | ------- |
| Yes   | Yes   | Yes     |