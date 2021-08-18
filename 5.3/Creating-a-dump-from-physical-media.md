==Command description==
This operating will create a dump image from real media using a physical device. It will retry errors and when finished create an XML metadata sidecar and an Alcohol 120% media descriptor for optical media. The dumping operation can be interrupted and continued later, even with a different device.

==Command usage==
<code>Aaru dump-media -d [true/false] -e <encoding> -f [true/false] -i <device path> -k <sectors> --lead-in [true/false] -m [true/false] --no-metadata [true/false] --no-trim [true/false] -O <options> -o <filename> --persistent [true/false] -p <passes> -s [true/false] -t <plugin> -v [true/false] -x <xml sidecar></code>

<code>-d, --debug=[true/false]</code> shows debug output ''(default false)''<br />
<code>-e, --encoding=<encoding></code> character encoding to use when creating dump sidecar<br />
<code>-f, --force=[true/false]</code> continuing dumping whatever happens ''(default false)''<br />
<code>-i, --input=<device path></code> path to the physical device<br />
<code>-k, --skip=<sectors></code> skip this many sectors when an unreadable sector is found ''(default 512)''<br />
<code>--lead-in=[true/false]</code> try to dump Lead-in. Only applicable to CD, DDCD or GD media ''(default false)''<br />
<code>-m, --resume=[true/false]</code> create and/or use resume mapfile ''(default true)''<br />
<code>--no-metadata=[true/false]</code> disables creating CICM XML sidecar ''(default false)''<br />
<code>--no-trim=[true/false]</code> disables trimming errores from skipped sectors ''(default false)''<br />
<code>-O, --options=<options></code> comma separated name=value pairs of options to pass to output image plugin<br />
<code>-o, --output=<filename></code> output image filename<br />
<code>--persistent=[true/false]</code> try to recover partial or incorrect data ''(default false)''<br />
<code>-p, --retry-passes=<passes></code> how many times to retry reading a sector ''(default 5)''<br />
<code>-s, --stop-on-error=[true/false]</code> stops dumping on first error ''(default false)''<br />
<code>-t, --format=<plugin></code> format for the output image, as plugin name or plugin id. If not present, will try to detect it from output image extension<br/>
<code>-v, --verbose=[true/false]</code> shows verbose output ''(default false)''<br />
<code>-x, --cicm-xml=<xml sidecar></code> take metadata from existing CICM XML sidecar<br />

==Example==
FreeBSD: <code>Aaru dump-media -i /dev/cd0 -f --persistent=true --separate-subchannel -w mydisc</code><br />
Linux: <code>Aaru dump-media -i /dev/sdb -r -f -p 15 -w myusbfloppy</code><br />
Windows: <code>Aaru dump-media -i \\.\PhysicalDrive3 -f -p 0 --resume=false mydisk</code><br />

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