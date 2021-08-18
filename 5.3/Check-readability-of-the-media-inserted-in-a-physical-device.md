==Command description==
This operation will read the media inserted in the physical device, and measure how fast it can be read sequentially. It's not intended as a benchmark, but as a detector of damaged sectors, sectors that are losing readability, etc. When finished it will check how fast can the device seek, and report speed statistics.

==Command usage==
<code>Aaru media-scan -b [ibglog] -d [true/false] -i <device> -m [mhddlog] -v [true/false]</code>

<code>-b, --ibg-log=[ibglog]</code> writes a log in the format used by ImgBurn<br />
<code>-d, --debug=[true/false]</code> shows debug output ''(default false)''<br />
<code>-i, --input=<dump></code> path to the physical device<br />
<code>-m, --mhdd-log=[mhddlog]</code> writes a log in the format used by MHDD<br />
<code>-v, --verbose=[true/false]</code> shows verbose output ''(default false)''<br />

==Example==
FreeBSD: <code>Aaru media-scan -i /dev/cd0</code><br />
Linux: <code>Aaru media-scan -i /dev/sdb</code><br />
Windows: <code>Aaru media-scan -i \\.\PhysicalDrive3</code><br />

==Operating system support==
{|
! Device type
! FreeBSD
! macOS
! Linux
! Windows
|-
| SCSI Block device
| Yes
| No <ref name="macOS permissions">macOS only allows talking with MultiMedia devices</ref>
| Yes
| Yes
|-
| SCSI MultiMedia device
| Yes
| Not yet <ref name="macOS users">Support for MultiMedia devices in macOS will be added if users require it</ref>
| Yes
| Yes
|-
| SCSI Streaming device
| Yes
| No <ref name="macOS permissions"/>
| Yes
| Yes
|-
| Parallel ATA
| No <ref name="FreeBSD bug">Not supported due to upstream bug</ref>
| No <ref name="macOS permissions"/>
| Yes
| Yes
|-
| Serial ATA
| Yes
| No <ref name="macOS permissions"/>
| Yes
| Yes
|-
| USB
| Partial <ref name="usb">USB descriptors are not retrieved</ref>
| Partial <ref name="macOS">Only MultiMedia devices can be supported and descriptors will not be retrieved</ref>
| Yes
| Yes
|-
| FireWire
| Partial <ref name="firewire">FireWire descriptors are not retrieved</ref>
| Partial <ref name="macOS"/>
| Yes
| Partial <ref name="firewire">FireWire descriptors are not retrieved</ref>
|-
| PCMCIA
| Partial <ref name="pcmcia">PCMCIA CIS is not retrieved</ref>
| Partial <ref name="macOS"/>
| Yes
| Partial <ref name="pcmcia">PCMCIA CIS is not retrieved</ref>
|-
| SecureDigital / MultiMediaCard
| Not yet <ref name="FreeBSD sd">Support will come with FreeBSD 12-RELEASE</ref>
| No <ref name="macOS permissions"/>
| Yes
| Untested <ref name="Windows sd">Should work, untested due to not available hardware</ref>
|}

<references/>