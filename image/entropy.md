# Table of Contents

- [Command description](#command-description)
- [Command usage](#command-usage)
- [Example](#example)
- [Operating system support](#operating-system-support)

## Command description

This operation will calculate uniqueness and entropy of the media represented by a media dump image. It's not affected by the image format compression, if applicable.

## Command usage

```text
USAGE:
    aaru image entropy <image-path> [OPTIONS]

ARGUMENTS:
    <image-path>    Media image path

OPTIONS:
                                DEFAULT                                         
    -h, --help                             Prints help information              
    -p, --duplicated-sectors    True       Calculates how many sectors are      
                                           duplicated (have same exact data in  
                                           user area)                           
    -t, --separated-tracks      True       Calculates entropy for each track    
                                           separately                           
    -w, --whole-disc            True       Calculates entropy for the whole disc
```

## Example

```bash
aaru image entropy example.iso
```

## Operating system support

| macOS | Linux | Windows |
| ----- | ----- | ------- |
| Yes   | Yes   | Yes     |