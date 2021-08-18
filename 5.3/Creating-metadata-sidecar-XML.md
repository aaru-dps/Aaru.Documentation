==Command description==
This operation will analyze a media dump, and if the format is recognized, create a CICM XML metadata sidecar with all information that can be automatically get about it, as well as all [[Supported-checksums|supported checksum algorithms]].

==Command usage==
<code>Aaru create-sidecar -b [block size] -d [true/false] -e [encoding] -i <dump> -t tape [true/false] -v [true/false]</code>

<code>-b, --block-size=[block size]</code> used only for tapes, indicates fixed block size in bytes. File in dump folder not multiple of this value will be ignored ''(default 512)''<br />
<code>-d, --debug=[true/false]</code> shows debug output ''(default false)''<br />
<code>-e, --encoding=[encoding]</code> sets which encoding is used by the contents of the media dump ''(default varies by filesystem)''<br />
<code>-i, --input=<dump></code> path to the media dump image<br />
<code>-t, --tape=[true/false]</code> indicates that dump points to a folder containing alphabetically sorted files extracted from a linear block-based tape with fixed block size (e.g. a SCSI streaming device) ''(default false)''<br />
<code>-v, --verbose=[true/false]</code> shows verbose output ''(default false)''<br />

==Examples==
<code>Aaru create-sidecar -i mydisc.cue</code><br />
<code>Aaru create-sidecar -i mytapedir -t -b 1024</code><br />
<code>Aaru create-sidecar -i "My japanese software.img" -e shift_jis</code><br />

==Operating system support==
{|
| FreeBSD
| Yes
|-
| macOS
| Yes
|-
| Linux
| Yes
|-
| Windows
| Yes
|}