==Command description== This operation will request and show all information about a physical device. For information
about supported physical devices check [[Supported-devices|the list of supported physical devices]]

==Command usage==
<code>Aaru device info [options] <device-path></code>

==Arguments==
<code><device-path></code> Device path<br />

==Options==
<code>--output-prefix, -w=[prefix]</code> writes binary responses from device to that prefix <br />
<code>-v, --verbose=[true/false]</code> shows verbose output ''(default false)''<br />
<code>-d, --debug=[true/false]</code> shows debug output ''(default false)''<br />
<code>--pause=[true/false]</code> pauses before exiting. ''(default false)''<br />
<code>-?, -h, --help=[true/false]</code> show help and usage information ''(default false)''<br />

==Example== FreeBSD: <code>Aaru device info /dev/cd0</code><br />
Linux: <code>Aaru device info /dev/sda</code><br />
Windows: <code>Aaru device info D:</code><br />

==Operating system support== {|
! Device type
! FreeBSD
! macOS
! Linux
! Windows |- | SCSI Block device | Yes | No <ref name="macOS permissions">macOS only allows talking with MultiMedia
devices</ref>
| Yes | Yes |- | SCSI MultiMedia device | Yes | Not yet <ref name="macOS users">Support for MultiMedia devices in macOS
will be added if users require it</ref>
| Yes | Yes |- | SCSI Streaming device | Yes | No <ref name="macOS permissions"/>
| Yes | Yes |- | Parallel ATA | No <ref name="FreeBSD bug">Not supported due to upstream bug</ref>
| No <ref name="macOS permissions"/>
| Yes | Yes |- | Serial ATA | Yes | No <ref name="macOS permissions"/>
| Yes | Yes |- | USB | Partial <ref name="usb">USB descriptors are not retrieved</ref>
| Partial <ref name="macOS">Only MultiMedia devices can be supported and descriptors will not be retrieved</ref>
| Yes | Yes |- | FireWire | Partial <ref name="firewire">FireWire descriptors are not retrieved</ref>
| Partial <ref name="macOS"/>
| Yes | Partial <ref name="firewire">FireWire descriptors are not retrieved</ref>
|- | PCMCIA | Partial <ref name="pcmcia">PCMCIA CIS is not retrieved</ref>
| Partial <ref name="macOS"/>
| Yes | Partial <ref name="pcmcia">PCMCIA CIS is not retrieved</ref>
|- | SecureDigital / MultiMediaCard | Not yet <ref name="FreeBSD sd">Support will come with FreeBSD 12-RELEASE</ref>
| No <ref name="macOS permissions"/>
| Yes | Untested <ref name="Windows sd">Should work, untested due to not available hardware</ref>
|}

<references/>