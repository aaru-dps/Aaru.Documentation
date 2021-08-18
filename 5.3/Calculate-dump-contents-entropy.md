==Command description==
This operation will calculate uniqueness and entropy of the media represented by a media dump image. It's not affected my the image format compression if applicable.

==Command usage==
<code>Aaru entropy -d [true/false] -i <dump> -p [true/false] -t [true/false] -v [true/false] -w [true/false]</code> 

<code>-d, --debug=[true/false]</code> shows debug output ''(default false)''<br />
<code>-i, --input=<dump></code> path to the media dump image<br />
<code>-p, --duplicated-sectors=[true/false]</code> besides entropy also calculates how many sectors have the exact same data in their user area ''(default true)''<br />
<code>-t, --separated-tracks=[true/false]</code> separately calculates the entropy for each track dividing the media. Only applicable to certain kind of media (optical discs and digital tapes mostly) ''(default true)''<br />
<code>-v, --verbose=[true/false]</code> shows verbose output ''(default false)''<br />
<code>-w, --whole-disc=[true/false]</code> calculates the entropy for the whole media ''(default true)''

==Example==
<code>Aaru entropy -i mydisc.cue</code>

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