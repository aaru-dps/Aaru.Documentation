# Table of Contents

- [Command description](#command-description)
- [Command usage](#command-usage)
- [Example](#example)
- [Operating system support](#operating-system-support)

## Command description

This operation will write or update metadata fields in an existing Aaru Image Format (`.aif`) image.

## Command usage

```text
USAGE:
    aaru image write-metadata <image-path> [OPTIONS]

ARGUMENTS:
    <image-path>    Media image path

OPTIONS:
    -h, --help                  Prints help information                         
        --comments              Image comments                                  
        --creator               Who (person) created the image?                 
        --drive-manufacturer    Manufacturer of the drive used to read the media
                                represented by the image                        
        --drive-model           Model of the drive used to read the media       
                                represented by the image                        
        --drive-revision        Firmware revision of the drive used to read the 
                                media represented by the image                  
        --drive-serial          Serial number of the drive used to read the     
                                media represented by the image                  
        --media-barcode         Barcode of the media represented by the image   
        --media-lastsequence    Last media of the sequence the media represented
                                by the image corresponds to                     
        --media-manufacturer    Manufacturer of the media represented by the    
                                image                                           
        --media-model           Model of the media represented by the image     
        --media-partnumber      Part number of the media represented by the     
                                image                                           
        --media-sequence        Number in sequence for the media represented by 
                                the image                                       
        --media-serial          Serial number of the media represented by the   
                                image                                           
        --media-title           Title of the media represented by the image
```

## Example

```bash
aaru image write-metadata example.aif
```

## Operating system support

| macOS | Linux | Windows |
| ----- | ----- | ------- |
| Yes   | Yes   | Yes     |