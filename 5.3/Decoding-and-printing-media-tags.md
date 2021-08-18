==Command description==
This operation will decode all [[Sector-tags|sector tags]] and [[Media-tags|media tags]] on a media dump image.

==Command usage==
<code>Aaru decode -d [true/false] -i <dump> -k [true/false] -l [sectors] -t [true/false] -s [start sector] -v [true/false]</code>

<code>-d, --debug=[true/false]</code> shows debug output ''(default false)''<br />
<code>-i, --input=<dump></code> path to the media dump image<br />
<code>-k, --disk-tags=[true/false]</code> decodes all [[Media-tags|media tags]] ''(default true)''<br />
<code>-l, --length=[sectors]</code> how many sectors to decode or ''all'' to decode all ''(default all)''<br />
<code>-t, --sector-tags=[true/false]</code> decodes all [[Sector-tags|sector tags]] ''(default true)''<br />
<code>-s, --start=[start-sector]</code> starting sector ''(default 0)''<br />
<code>-v, --verbose=[true/false]</code> shows verbose output ''(default false)''<br />

==Example==
<code>Aaru decode -i mydisc.cue -s 1000 -l 15 -t false</code>

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