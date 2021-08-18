==Command description== This operation will calculate the checksums for the media represented by a media dump image.

==Command usage==
<code>Aaru image checksum [options] <image-path></code>

==Arguments==
<code><image-path></code> Media image path<br />

==Options==
<code>-a, --adler32=[true/false]</code> calculates the Adler-32 checksum ''(default true)''<br />
<code>--crc16=[true/false]</code> calculates the CRC16 checksum ''(default true)''<br />
<code>-c, --crc32=[true/false]</code> calculates the CRC32 checksum ''(default true)''<br />
<code>--crc64=[true/false]</code> calculates the ECMA CRC64 checksum ''(default false)''<br />
<code>--fletcher16=[true/false]</code> calculates the Fletcher-16 checksum ''(default false)''<br />
<code>--fletcher32=[true/false]</code> calculates the Fletcher-32 checksum ''(default false)''<br />
<code>-m, --md5=[true/false]</code> calculates the MD5 hash ''(default true)''<br />
<code>-t, --separated-tracks=[true/false]</code> calculates each track checksum separately ''(default true)''<br />
<code>--ripemd160=[true/false]</code> calculates the RIPEMD160 hash ''(default false)''<br />
<code>-s, --sha1=[true/false]</code> calculates the SHA1 hash ''(default true)''<br />
<code>--sha256=[true/false]</code> calculates the SHA2 hash with 256-bit ''(default false)''<br />
<code>--sha384=[†rue/false]</code> calculates the SHA2 hash with 384-bit ''(default false)''<br />
<code>--sha512=[true/false]</code> calculates the SHA2 hash with 512-bit ''(default false)''<br />
<code>-f, --spamsum=[true/false]</code> calculates the SpamSum fuzzy hash ''(default true)''<br />
<code>-w, --whole-disc=[true/false]</code> calculates the whole media checksum ''(default true)''<br />
<code>-v, --verbose=[true/false]</code> shows verbose output ''(default false)''<br />
<code>-d, --debug=[true/false]</code> shows debug output ''(default false)''<br />
<code>--pause=[true/false]</code> pauses before exiting. ''(default false)''<br />
<code>-?, -h, --help=[true/false]</code> show help and usage information ''(default false)''<br />

==Example==
<code>Aaru image checksum -a false --sha512=true mydisc.cue</code>

==Operating system support== {| | FreeBSD | Yes |- | macOS | Yes |- | Linux | Yes |- | Windows | Yes |}
