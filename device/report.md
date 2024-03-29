# Table of Contents

- [Command Description](#command-description)
- [Command usage](#command-usage)
- [Example](#example)
- [Operating system support](#operating-system-support)

## Command description

This operation will test a physical device for its read capabilities. If the media is removable, it will ask you to insert different media into it, as read capabilities vary with different media. The report will be saved in the executing directory, and sent to us. Shared reports can be seen in https://www.aaru.app

## Command usage

```Aaru -d [true/false] -v [true/false] device-report -h [true/false] <device-path/aaru-remote-host>```

```-d, --debug [true/false]``` shows debug output *(default false)*

```-v, --verbose [true/false]``` shows verbose output *(default false)*

```-h, --help [true/false]``` shows help screen for the command instead of running it, ignores all other switches *(default false)*

```-t, --trap-disc [true/false]``` does a device report using a trap disc. *(default false)*

```<aaru-remote-host>``` connects to an Aaru Remote Host with ```aaru://<IP ADDRESS>/<DEVICE PATH>```

## Example

FreeBSD: ```aaru device-report /dev/cd0```

Linux: ```aaru device-report /dev/sdb```

Windows: ```aaru device-report \\.\PhysicalDrive3```

## Operating system support

| Device Type  | FreeBSD  | MacOS  | Linux  | Windows  |
|--------------|----------|--------|--------|----------|
| SCSI Block device | Yes | No¹ | Yes | Yes |
| SCSI MultiMedia device | Yes | Not yet² | Yes | Yes |
| SCSI Streaming device | Yes | No¹ | Yes | Yes |
| Parallel ATA | No³ | No¹ | Yes | Yes |
| Serial ATA | Yes | No¹ | Yes | Yes |
| USB | Partial⁴ | Partial⁵ | Yes | Yes |
| FireWire | Partial⁶ | Partial⁵ | Yes | Partial⁶ |
| PCMCIA | Partial⁷ | Partial⁵ | Yes | Partial⁷ |
| SecureDigital / MultiMediaCard | Not yet⁸ | No¹ | Yes | Untested⁹ |

1. macOS only allows talking with MultiMedia devices
2. Support for MultiMedia devices in macOS will be added if users require it
3. Not supported due to upstream bug
4. USB descriptors are not retrieved
5. Only MultiMedia devices can be supported and descriptors will not be retrieved
6. FireWire descriptors are not retrieved
7. PCMCIA CIS is not retrieved
8. Support will come with FreeBSD 12-RELEASE
9. Should work, untested due to no available hardware

