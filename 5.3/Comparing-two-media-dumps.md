==Command description== This operation will compare two media dumps and print all differences between them. Dumps can be
in different formats.

==Command usage==
<code>Aaru image compare [options] <image-path1> <image-path2></code>

==Arguments==
<code><image-path1></code> First media image path<br />
<code><image-path2></code> Second media image path<br />

==Options==
<code>-v, --verbose=[true/false]</code> shows verbose output ''(default false)''<br />
<code>-d, --debug=[true/false]</code> shows debug output ''(default false)''<br />
<code>--pause=[true/false]</code> pauses before exiting. ''(default false)''<br />
<code>-?, -h, --help=[true/false]</code> show help and usage information ''(default false)''<br />

==Example==
<code>Aaru image compare mydisc.cue anotherdisc.mds</code>

==Operating system support== {| | FreeBSD | Yes |- | macOS | Yes |- | Linux | Yes |- | Windows | Yes |}
