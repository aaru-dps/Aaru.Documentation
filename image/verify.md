# Table of Contents

- [Command description](#command-description)
- [Command usage](#command-usage)
- [Example](#example)
- [Operating system support](#operating-system-support)

## Command description

This operation will verify a media dump. If the media dump format includes a hash or checksum, it will calculate and compare it. If the media sector/block format include a hash, checksum, or error recovery system, it will calculate and compare them.

## Command usage

```text
USAGE:
    aaru image verify <image-path> [OPTIONS]

ARGUMENTS:
    <image-path>    Media image path

OPTIONS:
                            DEFAULT                                             
    -h, --help                         Prints help information                  
    -w, --verify-disc       True       Verify media image if supported          
    -s, --verify-sectors    True       Verify all sectors if supported          
    -g, --create-graph      True       Create graph of verified disc (currently 
                                       only implemented for optical discs)      
    -d, --dimensions        1080       Dimensions, as a square, in pixels, for  
                                       the graph of verified media              
    -t, --data-only         True       Verify only data tracks
```

## Example

```bash
aaru image verify example.iso
```

## Operating system support

| macOS | Linux | Windows |
| ----- | ----- | ------- |
| Yes   | Yes   | Yes     |