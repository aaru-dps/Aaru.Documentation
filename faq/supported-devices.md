The following physical devices are supported:

## Operating system support

| Device Type | macOS | Linux | Windows |
|-------------|-------|-------|---------|
| SCSI Block device | No¹ | Yes | Yes |
| SCSI MultiMedia device | Not yet² | Yes | Yes |
| SCSI Streaming device | No¹ | Yes | Yes |
| Parallel ATA | No¹ | Yes | Yes |
| Serial ATA | No¹ | Yes | Yes |
| USB | Not yet³ | Yes | Yes |
| FireWire | Not yet³ | Yes | Partial⁴ |
| PCMCIA | Not yet³ | Yes | Partial⁵ |
| SecureDigital / MultiMediaCard | No¹ | Yes | Untested⁶ |

1. macOS only allows talking with MultiMedia devices.
2. Support for MultiMedia devices in macOS will be added if users require it.
3. Only MultiMedia devices can be supported and descriptors will not be retrieved.
4. FireWire descriptors are not retrieved.
5. PCMCIA CIS is not retrieved.
6. Should work, but it remains untested due to lack of hardware.