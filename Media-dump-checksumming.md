# Command description
This operation will calculate the checksums for the media represented by a media dump image.

# Command usage
DiscImageChef verify -i \<dump\> -v [true/false] -d [true/false] -t [true/false] -w [true/false] -a [true/false] --crc16 [true/false] -c [true/false] --crc64 [true/false] -m [true/false] --ripemd160 [true/false] -s [true/false] --sha256 [true/false] --sha384 [true/false] --sha512 [true/false] -f

-i, --input=\<dump\> path to the media dump image  
-v, --verbose=[true/false] shows verbose output _[default false]_  
-d, --debug=[true/false] shows debug output _[default false]_  
-t, --separated-tracks=[true/false] calculates each track checksum separately _[default true]_  
-w, --whole-discs=[true/false] calculates the whole media checksum _[default true]_  
-a, --adler32=[true/false] calculates the Adler-32 checksum _[default true]_  
--crc16=[true/false] calculates the CRC16 checksum _[default true]_  
-c, --crc32=[true/false] calculates the CRC32 checksum _[default true]_  
--crc64=[true/false] calculates the ECMA CRC64 checksum _[default false]_  
-m, --md5=[true/false] calculates the MD5 hash _[default true]_  
-s, --sha1=[true/false] calculates the SHA1 hash _[default true]_  
--sha256=[true/false] calculates the SHA2 hash with 256-bit _[default false]_  
--sha384=[†rue/false] calculates the SHA2 hash with 384-bit _[default false]_  
--sha512=[true/false] calculates the SHA2 hash with 512-bit _[default false]_  
-f, --spamsum=[true/false] calculates the SpamSum fuzzy hash _[default true]_  
