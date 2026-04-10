# Table of Contents

- [Command description](#command-description)
- [Command usage](#command-usage)
- [Example](#example)
- [Operating system support](#operating-system-support)

## Command description

This operation will create a media dump from real media using a physical device. It will retry errors and when finished, create an XML metadata sidecar. The dumping operation can be interrupted and continued later with supported formats, even from a different device.

## Command usage

```text
USAGE:
    aaru media dump <device-path> <output-path> [OPTIONS]

ARGUMENTS:
    <device-path>    Device path                                                
    <output-path>    Output image path. If filename starts with # and exists, it
                     will be read as a list of output images, its extension will
                     be used to detect the image output format, each media will 
                     be ejected and confirmation for the next one will be asked 

OPTIONS:
                                     DEFAULT                                    
    -h, --help                                  Prints help information         
    -x, --cicm-xml                              Take metadata from existing CICM
                                                XML sidecar                     
    -e, --encoding                              Name of character encoding to   
                                                use                             
        --first-pregap                          Try to read first track pregap. 
                                                Only applicable to CD/DDCD/GD   
        --fix-offset                 True       Fix audio tracks offset. Only   
                                                applicable to CD/GD             
    -f, --force                                 Continue dumping whatever       
                                                happens                         
    -t, --format                                Format of the output image, as  
                                                plugin name or plugin id. If not
                                                present, will try to detect it  
                                                from output image extension     
        --metadata                   True       Enables creating Aaru Metadata  
                                                sidecar                         
        --trim                       True       Enables trimming errored from   
                                                skipped sectors                 
    -O, --options                               Comma separated name=value pairs
                                                of options to pass to output    
                                                image plugin                    
        --persistent                            Try to recover partial or       
                                                incorrect data                  
    -r, --resume                     True       Create/use resume mapfile       
    -p, --retry-passes               5          How many retry passes to do     
    -k, --skip                       512        When an unreadable sector is    
                                                found skip this many sectors    
    -s, --stop-on-error                         Stop media dump on first error  
        --subchannel                 any        Subchannel to dump. Only        
                                                applicable to CD/GD. Values:    
                                                any, rw, rw-or-pq, pq, none     
        --speed                      0          Speed to dump. Only applicable  
                                                to optical drives, 0 for maximum
        --private                               Do not store paths and serial   
                                                numbers in log or metadata      
        --fix-subchannel-position    True       Store subchannel according to   
                                                the sector they describe        
        --retry-subchannel           True       Retry subchannel. Implies fixing
                                                subchannel position             
        --fix-subchannel                        Try to fix subchannel. Implies  
                                                fixing subchannel position      
        --fix-subchannel-crc                    If subchannel looks OK but CRC  
                                                fails, rewrite it. Implies      
                                                fixing subchannel               
        --generate-subchannels                  Generates missing subchannels   
                                                (they don't count as dumped in  
                                                resume file)                    
        --skip-cdiready-hole         True       Skip the hole between data and  
                                                audio in a CD-i Ready disc      
        --eject                                 Eject media after dump finishes 
        --max-blocks                 64         Maximum number of blocks to read
                                                at once                         
        --use-buffered-reads         True       For MMC/SD, use OS buffered     
                                                reads if CMD23 is not supported 
        --store-encrypted            True       Store encrypted data as is      
        --bypass-wii-decryption                 Skip Wii disc encryption        
                                                processing during conversion or 
                                                dump                            
        --title-keys                 True       Try to read the title keys from 
                                                CSS encrypted DVDs (very slow)  
        --ignore-cdr-runouts         10         How many CD-R(W) run-out sectors
                                                to ignore and regenerate (0 for 
                                                none)                           
    -g, --create-graph               True       Create graph of dumped media.   
                                                Currently only supported for    
                                                CD/DVD/BD/GD/UMD                
        --dimensions                 1080       Dimensions in pixels of the     
                                                square that will contain the    
                                                graph of dumped media           
        --aaru-metadata                         Take metadata from existing Aaru
                                                Metadata sidecar                
        --paranoia                              Do not trust the drive, check   
                                                the sectors integrity before    
                                                writing them to the image. Valid
                                                only for CD/GD                  
        --cure-paranoia                         Try to fix sectors that do not  
                                                pass the integrity checks       
        --raw                                   EXPERIMENTAL: Enable raw dumping
                                                mode. This feature is           
                                                experimental and may not work   
                                                correctly with all devices or   
                                                media types. Use at your own    
                                                risk.
```

## Example

macOS:

```bash
aaru media dump -f /dev/rdisk2 mydisc.aif
```

Linux:

```bash
aaru media dump -r -f -p 15 /dev/sr0 mydisc.aif
```

Windows:

```bash
aaru media dump -f -p 0 \\.\PhysicalDrive3 mydisk.aif
```

## Operating system support

| Device Type | macOS | Linux | Windows |
|-------------|-------|-------|---------|
| SCSI Block device | No¹ | Yes | Yes |
| SCSI MultiMedia device | No¹ | Yes | Yes |
| SCSI Streaming device | No¹ | Yes | Yes |
| Parallel ATA | No¹ | Yes | Yes |
| Serial ATA | No¹ | Yes | Yes |
| USB | No¹ | Yes | Yes |
| FireWire | No¹ | Yes | Partial² |
| PCMCIA | No¹ | Yes | Partial³ |
| SecureDigital / MultiMediaCard | No¹ | Yes | Untested⁴ |

1. Media dump and other device-access commands are not currently supported on macOS.
2. FireWire descriptors are not retrieved.
3. PCMCIA CIS is not retrieved.
4. Should work, but it remains untested due to lack of hardware.