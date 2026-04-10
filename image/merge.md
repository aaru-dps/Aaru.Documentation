# Table of Contents

- [Command description](#command-description)
- [Command usage](#command-usage)
- [Example](#example)
- [Operating system support](#operating-system-support)

## Command description

This operation will merge two compatible media images into a new output image, optionally taking sectors or metadata from the secondary image when needed.

## Command usage

```text
USAGE:
    aaru image merge <primary-image> <secondary-image> <output-image> [
OPTIONS]

ARGUMENTS:
    <primary-image>      Path to the primary image file      
    <secondary-image>    Path to the secondary image file    
    <output-image>       Path to the output merged image file

OPTIONS:
                                     DEFAULT                                    
    -h, --help                                  Prints help information         
        --secondary-tags                        Use media tags from secondary   
                                                image (otherwise when in both   
                                                images, primary image tags are  
                                                used)                           
        --sectors-file                          File containing list of sectors 
                                                to take from secondary image    
                                                (one sector number per line)    
        --ignore-media-type                     Ignore mismatched image media   
                                                type. Merged image will still   
                                                have primary image media type   
        --comments                              Image comments                  
    -c, --count                      64         How many sectors to convert at  
                                                once                            
        --creator                               Who (person) created the image? 
        --drive-manufacturer                    Manufacturer of the drive used  
                                                to read the media represented by
                                                the image                       
        --drive-model                           Model of the drive used to read 
                                                the media represented by the    
                                                image                           
        --drive-revision                        Firmware revision of the drive  
                                                used to read the media          
                                                represented by the image        
        --drive-serial                          Serial number of the drive used 
                                                to read the media represented by
                                                the image                       
    -p, --format                                Format of the output image, as  
                                                plugin name or plugin id. If not
                                                present, will try to detect it  
                                                from output image extension     
        --media-barcode                         Barcode of the media represented
                                                by the image                    
        --media-lastsequence         0          Last media of the sequence the  
                                                media represented by the image  
                                                corresponds to                  
        --media-manufacturer                    Manufacturer of the media       
                                                represented by the image        
        --media-model                           Model of the media represented  
                                                by the image                    
        --media-partnumber                      Part number of the media        
                                                represented by the image        
        --media-sequence             0          Number in sequence for the media
                                                represented by the image        
        --media-serial                          Serial number of the media      
                                                represented by the image        
        --media-title                           Title of the media represented  
                                                by the image                    
    -O, --options                               Comma separated name=value pairs
                                                of options to pass to output    
                                                image plugin                    
        --primary-resume                        Resume file for primary image   
        --secondary-resume                      Resume file for secondary image 
    -g, --geometry                              Force geometry, only supported  
                                                in not tape block media. Specify
                                                as C/H/S                        
        --fix-subchannel-position    True       Store subchannel according to   
                                                the sector they describe        
        --fix-subchannel                        Try to fix subchannel. Implies  
                                                fixing subchannel position      
        --fix-subchannel-crc                    If subchannel looks OK but CRC  
                                                fails, rewrite it. Implies      
                                                fixing subchannel               
        --generate-subchannels                  Generates missing subchannels   
        --decrypt                               Try to decrypt encrypted sectors
        --ignore-negative-sectors               Ignore negative sectors         
        --ignore-overflow-sectors               Ignore overflow sectors
```

## Example

```bash
aaru image merge primary.aif secondary.aif merged.aif
```

## Operating system support

| macOS | Linux | Windows |
| ----- | ----- | ------- |
| Yes   | Yes   | Yes     |