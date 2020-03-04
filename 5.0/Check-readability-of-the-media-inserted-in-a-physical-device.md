# Table of Contents

- [Command Description](#command-description)
- [Command usage](#command-usage)
- [Example](#example)
- [Operating system support](#operating-system-support)


## Command Description

This operation will read the media inserted in the physical device, and measure how fast it can be read sequentially. It's not intended as a benchmark, but as a detector of damaged sectors, sectors that are losing readability, etc. When finished it will check how fast can the device seek, and report speed statistics.

## Command usage

```bash
Aaru -d [true/false] -v [true/false] media scan -h [true/false] -b [ibglog] -m [mhddlog] <device-path/aaru-remote-host>
```

`-d, --debug [true/false]` shows debug output *(default false)*  
`-v, --verbose [true/false]` shows verbose output *(default false)*  
`-h, --help [true/false]` shows help screen for the command instead of running it, ignores all other switches *(default false)*  
`-b, --ibg-log [ibglog]` writes a log in the format used by ImgBurn  
`-m, --mhdd-log [mhddlog]`  writes a log in the format used by MHDD  
`<aaru-remote-host>` connects to an Aaru Remote Host with aaru:///

## Example

FreeBSD: `Aaru media scan /dev/cd0`  
Linux: `Aaru media scan /dev/sdb`  
Windows: `Aaru media scan \\.\PhysicalDrive3`

## Operating system support

| Device Type  | FreeBSD  | MacOS  | Linux  | Windows  |
|--------------|----------|--------|--------|----------|
| SCSI Block device  | Yes  | No [^1]  | Yes  | Yes  |
| SCSI MultiMedia device  | Yes  | Not yet [^2] | Yes  | Yes  |
| SCSI Streaming device  | Yes  | No [^1]  | Yes  | Yes  |
| Parallel ATA  | No [^3] | No [^1]  | Yes  | Yes  |
| Serial ATA  | Yes  | No [^1]  | Yes  | Yes  |
| USB  | Partial [^4] | Partial [^5] | Yes  | Yes  |
| FireWire  | Partial [^6] | Partial [^5] | Yes  | Partial [^6] |
| PCMCIA  | Partial [^7] | Partial [^5] | Yes  | Partial [^7] |
| SecureDigital / MultiMediaCard  | Not yet [^8] | No [^1]  | Yes  | Untested [^9] |
[^1]: macOS only allows talking with MultiMedia devices.
[^2]: Support for MultiMedia devices in macOS will be added if users require it
[^3]: Not supported due to upstream bug
[^4]: USB descriptors are not retrieved
[^5]: Only MultiMedia devices can be supported and descriptors will not be retrieved
[^6]: FireWire descriptors are not retrieved
[^7]: PCMCIA CIS is not retrieved
[^8]: Support will come with FreeBSD 12-RELEASE
[^9]: Should work, untested due to not available hardware