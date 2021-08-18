==Command description==
This command will analyze a media dump, and if the format is recognized and you choose so, it will search for [[Partitioning-schemes-recognized-by-Aaru|supported partitioning schemes]] and [[Filesystems-recognized-by-Aaru|supported filesystems]] on the dump, showing information about them.

==Command usage==
<code>Aaru filesystem info [options] <image-path></code>

==Arguments==
<code><image-path></code> Media image path<br />

==Options==
<code>-e, --encoding=[encoding]</code> sets which encoding is used by the contents of the media dump ''(default varies by filesystem)''<br />
<code>-f, --filesystems=[true/false]</code> searches and interprets filesystems ''(default true)''<br />
<code>-p, --partitions=[true/false]</code> searches and interprets partitions ''(default true)''<br />
<code>-v, --verbose=[true/false]</code> shows verbose output ''(default false)''<br />
<code>-d, --debug=[true/false]</code> shows debug output ''(default false)''<br />
<code>--pause=[true/false]</code> pauses before exiting. ''(default false)''<br />
<code>-?, -h, --help=[true/false]</code> show help and usage information ''(default false)''<br />

==Example==
<code>Aaru filesystem info mydisc.cue</code>

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