==Command description==
This operation will request and show all information about the inserted media in a physical device. For information about supported physical devices check [[Supported-devices|the list of supported physical devices]]

==Command usage==
<code>Aaru media-info -d [true/false] -i <device> -v [true/false] -w [prefix]</code>

<code>-d, --debug=[true/false]</code> shows debug output ''(default false'')<br />
<code>-i, --input=<device></code> path to the physical device<br />
<code>-v, --verbose=[true/false]</code> shows verbose output ''(default false'')<br />
<code>-w, --output-prefix=[prefix]</code> writes binary responses from device to that prefix  

==Example==
FreeBSD: <code>Aaru media-info -i /dev/cd0</code><br />
Linux: <code>Aaru media-info -i /dev/sdb</code><br />
Windows: <code>Aaru media-info -i \\.\PhysicalDrive3</code><br />

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
| No <ref name="atamedia">Use device-info command</ref>
| No <ref name="atamedia"/>
| No <ref name="atamedia"/>
| No <ref name="atamedia"/>
|-
| Serial ATA
| No <ref name="atamedia"/>
| No <ref name="atamedia"/>
| No <ref name="atamedia"/>
| No <ref name="atamedia"/>
|-
| USB
| Yes
| Yes
| Yes
| Yes
|-
| FireWire
| Yes
| Yes
| Yes
| Yes
|-
| PCMCIA
| Yes
| Yes
| Yes
| Yes
|-
| SecureDigital / MultiMediaCard
| No <ref name="atamedia"/>
| No <ref name="atamedia"/>
| No <ref name="atamedia"/>
| No <ref name="atamedia"/>
|}

<references/>