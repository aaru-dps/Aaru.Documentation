==Command description== This operation will analyze and find all filesystems in a media dump and list all the files that
are contained in [[Filesystems-recognized-by-Aaru|supported filesystems]]

==Command usage==
<code>Aaru filesystem list [options] <image-path></code>

==Arguments==
<code><image-path></code> Media image path<br />

==Options==
<code>-e, --encoding=[encoding]</code> sets which encoding is used by the contents of the media dump ''(default varies
by filesystem)''<br />
<code>-l, --long-format=[true/false]</code> use a long listing format, showing sizes and extended attributes ''(default
false)''<br />
<code>-O, --options=[options]</code> comma separated name=value pairs of options to pass to filesystem plugin<br />
<code>-n, --namespace=[namespace]</code> namespace to use for filenames ''(default varies by filesystem)''<br />
<code>-v, --verbose=[true/false]</code> shows verbose output ''(default false)''<br />
<code>-d, --debug=[true/false]</code> shows debug output ''(default false)''<br />
<code>--pause=[true/false]</code> pauses before exiting. ''(default false)''<br />
<code>-?, -h, --help=[true/false]</code> show help and usage information ''(default false)''<br />

==Example==
<code>Aaru filesystem list -l -e x-mac-icelandic mydisc.cue</code>

==Operating system support== {| | FreeBSD | Yes |- | macOS | Yes |- | Linux | Yes |- | Windows | Yes |}