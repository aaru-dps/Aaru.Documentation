==Command description==
This operation will print in console a hexadecimal dump of the chosen sector/block of the indicated media dump image.

==Command usage==
<code>Aaru printhex -d [true/false] -i <dump> -l [sectors] -r [true/false] -s <starting sector> -v [true/false] -w [width]</code>

<code>-d, --debug=[true/false]</code> shows debug output ''(default false)''<br />
<code>-i, --input=<dump></code> path to the media dump image<br />
<code>-l, --length=[sectors]</code> how many sectors to print ''(default 1)''<br />
<code>-r, --long-sectors=[true/false]</code> if hex print should include all [[Sector-Tags|sector tags]] stored in the media dump ''(default false)''<br />
<code>-s, --start=<starting sector></code> starts the hexadecimal printing from this sector<br />
<code>-v, --verbose=[true/false]</code> shows verbose output ''(default false)''<br />
<code>-w, --width=[width]</code> how width, in characters, should the print be before creating a new line ''(default 32)''

==Example==
<code>Aaru printhex -i mydisc.cue -s 15 -l 30 -r -w 64</code>

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
