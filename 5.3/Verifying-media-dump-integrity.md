==Command description==
This operation will verify a media dump.
If the media dump format includes a hash or checksum, it will calculate and compare it.
If the media sectors/blocks format include a hash, checksum or error recovery system, it will calculate and compare them.

==Command usage==
<code>Aaru verify -d [true/false] -i <dump> -s [true/false] -v [true/false] -w [true/false]</code>

<code>-d, --debug=[true/false]</code> shows debug output ''(default false)''<br />
<code>-i, --input=<dump></code> path to the media dump image<br />
<code>-s, --verify-sectors=[true/false]</code> calculates and verifies the hash/checksum/ecc of every sector/block in the media dump ''(default true)''<br />
<code>-v, --verbose=[true/false]</code> shows verbose output ''(default false)''<br />
<code>-w, --verify-disc=[true/false]</code> calculates and verifies a media dump format checksum/hash ''(default true)''<br />

==Example==
<code>Aaru verify -i mydisc.cue</code>

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
