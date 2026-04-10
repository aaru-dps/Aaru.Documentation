# Table of Contents

- [Command description](#command-description)
- [Command usage](#command-usage)
- [Example](#example)
- [Operating system support](#operating-system-support)

## Command description

This operation will analyze a media dump and, if the format is recognized, create a CICM XML metadata sidecar with all information that can be automatically retrieved from it, as well as all [supported checksum algorithms.](../faq/supported-checksums.md)

## Command usage

```text
USAGE:
    aaru image create-sidecar <image-path> [OPTIONS]

ARGUMENTS:
    <image-path>    Media image path

OPTIONS:
                            DEFAULT                                             
    -h, --help                         Prints help information                  
    -b, --block-size        512        Only used for tapes, indicates block     
                                       size. Files in the folder whose size is  
                                       not a multiple of this value will simply 
                                       be ignored                               
    -e, --encoding                     Name of character encoding to use        
    -t, --tape                         When used indicates that input is a      
                                       folder containing alphabetically sorted  
                                       files extracted from a linear block-based
                                       tape with fixed block size (e.g. a SCSI  
                                       tape device)                             
        --enable-spamsum               Enables calculation of Spamsum fuzzy     
                                       hashes
```

## Example

```bash
aaru image create-sidecar example.iso
```

## Operating system support

| macOS | Linux | Windows |
| ----- | ----- | ------- |
| Yes   | Yes   | Yes     |