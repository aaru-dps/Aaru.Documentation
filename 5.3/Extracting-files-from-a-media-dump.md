==Command description==
This operation will analyze and find all filesystems in a media dump and extract the files that are contained in [[Filesystems-recognized-by-Aaru|supported filesystems]].

==Command usage==
<code>Aaru filesystem extract [options] <image-path> <output-dir></code> 

==Arguments==
<code><image-path></code> Media image path<br />
<code><output-dir></code> Directory where extracted files will be created. Will abort if it exists<br />

==Options==
<code>-e, --encoding=[encoding]</code> sets which encoding is used by the contents of the media dump ''(default varies by filesystem)''<br />
<code>-O, --options=[options]</code> comma separated name=value pairs of options to pass to filesystem plugin<br />
<code>-x, --xattrs=[true/false]</code> extract extended attributes if present ''(default false)''<br />
<code>-n, --namespace=[namespace]</code> namespace to use for filenames<br />
<code>-v, --verbose=[true/false]</code> shows verbose output ''(default false)''<br />
<code>-d, --debug=[true/false]</code> shows debug output ''(default false)''<br />
<code>--pause=[true/false]</code> pauses before exiting. ''(default false)''<br />
<code>-?, -h, --help=[true/false]</code> show help and usage information ''(default false)''<br />

==Example==
<code>Aaru filesystem extract -x -e iso8859-15 mydisc.cue contents</code>

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