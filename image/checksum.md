# Table of Contents

- [Command description](#command-description)
- [Command usage](#command-usage)
- [Example](#example)
- [Operating system support](#operating-system-support)

## Command description

This operation will calculate the checksums for the media represented by a media dump image.

## Command usage

```text
USAGE:
    aaru image checksum <image-path> [OPTIONS]

ARGUMENTS:
    <image-path>    Media image path

OPTIONS:
                              DEFAULT                                   
    -h, --help                           Prints help information        
    -a, --adler32                        Calculates Adler-32            
        --crc16               True       Calculates CRC16               
    -c, --crc32               True       Calculates CRC32               
        --crc64               True       Calculates CRC64 (ECMA)        
        --fletcher16                     Calculates Fletcher-16         
        --fletcher32                     Calculates Fletcher-32         
    -m, --md5                 True       Calculates MD5                 
    -s, --sha1                True       Calculates SHA1                
        --sha256                         Calculates SHA256              
        --sha384                         Calculates SHA384              
        --sha512              True       Calculates SHA512              
    -f, --spamsum             True       Calculates SpamSum fuzzy hash  
    -w, --whole-disc          True       Checksums the whole disc       
    -t, --separated-tracks    True       Checksums each track separately
```

## Example

```bash
aaru image checksum example.iso
```

## Operating system support

| macOS | Linux | Windows |
| ----- | ----- | ------- |
| Yes   | Yes   | Yes     |