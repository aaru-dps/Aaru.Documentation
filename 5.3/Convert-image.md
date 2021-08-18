==Command description== This operating will convert a dump from one image format to another.

==Command usage==
<code>Aaru image convert [options] <input-path> <output-path></code>

==Arguments==
<code><input-path></code> Input image path<br />
<code><output-path>></code> Output image path<br />

==Options==
<code>--cicm-xml, -x=<xml sidecar></code> take metadata from existing CICM XML sidecar<br />
<code>--comments=<comments></code> image comments<br />
<code>-c, --count=<count></code> how many sectors to convert at once ''(default 64)''<br />
<code>--creator=<creator></code> who (person) created the image?<br />
<code>--drive-manufacturer=<drive-manufacturer></code> manufacturer of the drive used to read the media represented by
the image<br />
<code>--drive-model=<drive-model></code> model of the drive used to read the media represented by the image<br />
<code>--drive-revision=<drive-revision></code> firmware revision of the drive used to read the media represented by the
image<br />
<code>--drive-serial=<drive-serial></code> serial number of the drive used to read the media represented by the
image<br />
<code>-f, --force=[true/false]</code> continue conversion even if sector or media tags will be lost in the process ''(
default false)''<br />
<code>--format, -p=<format></code> format of the output image, as plugin name or plugin id. If not present, will try to
detect it from output image extension.<br />
<code>--media-barcode=<media-barcode></code> barcode of the media represented by the image<br />
<code>--media-lastsequence=<media-lastsequence></code> last media of the sequence the media represented by the image
corresponds to ''(default 0)''<br />
<code>--media-manufacturer=<media-manufacturer></code> manufacturer of the media represented by the image<br />
<code>--media-model=<media-model></code> model of the media represented by the image<br />
<code>--media-partnumber=<media-partnumber></code> part number of the media represented by the image<br />
<code>--media-sequence=<media-sequence></code> number in sequence for the media represented by the image ''(default
0)''<br />
<code>--media-serial=<media-serial></code> serial number of the media represented by the image<br />
<code>--media-title=<media-title></code> title of the media represented by the image<br />
<code>-O, --options=<options></code> comma separated name=value pairs of options to pass to output image plugin<br />
<code>-r, --resume-file=<resume-file></code> take list of dump hardware from existing resume file<br />
<code>--fix-subchannel-position=[true/false]</code> store subchannel according to the sector they describe.<br />
<code>--fix-subchannel=[true/false]</code> try to fix subchannel. Implies fixing subchannel position.<br />
<code>--fix-subchannel-crc=[true/false]</code> if subchannel looks OK but CRC fails, rewrite it. Implies fixing
subchannel.<br />
<code>--generate-subchannels=[true/false]</code> generates missing subchannels.<br />
<code>-d, --debug=[true/false]</code> shows debug output from plugins ''(default false)''<br />
<code>-v, --verbose=[true/false]</code> shows verbose output ''(default false)''<br />

==Example==
<code>Aaru image convert -c 32 --comments="My converted image" --creator="Jane Doe" --drive-manufacturer="LG"
--drive-model="CD-RW 1234" --drive-revision="1.0" --drive-serial="AABBCCDDEEFF01" --media-lastsequence=2
--media-sequence=1 --media-title="Important software" -O "deduplicate=true,nocompress=false" -r dd_dump.resume.xml -x
dd_dump.cicm.xml dd_dump.iso dump.aaruf</code>