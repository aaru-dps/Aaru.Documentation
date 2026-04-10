# Table of Contents

- [Command description](#command-description)
- [Command usage](#command-usage)
- [Example](#example)
- [Operating system support](#operating-system-support)

## Command description

This operation will decode all [sector tags](../faq/sector-tags.md) and [media tags](../faq/media-tags.md) in a media dump image.

## Command usage

```text
USAGE:
    aaru image decode <image-path> [OPTIONS]

ARGUMENTS:
    <image-path>    Media image path

OPTIONS:
                         DEFAULT                                        
    -h, --help                      Prints help information             
    -f, --disk-tags      True       Decode media tags                   
    -l, --length         all        How many sectors to decode, or "all"
    -p, --sector-tags    True       Decode sector tags                  
    -s, --start          0          Sector to start decoding from
```

## Example

```bash
aaru image decode example.iso
```

## Operating system support

| macOS | Linux | Windows |
| ----- | ----- | ------- |
| Yes   | Yes   | Yes     |