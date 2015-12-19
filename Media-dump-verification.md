# Command description
This operation will verify a media dump.
If the media dump format includes a hash or checksum, it will calculate and compare it.
If the media sectors/blocks format include a hash, checksum or error recovery system, it will calculate and compare them.

# Command usage
DiscImageChef analyze -i \<dump\> -p [true/false] -f [true/false] -v [true/false] -d [true/false]

-i, --input=\<dump\> path to the media dump image  
-v, --verbose=[true/false] shows verbose output _[default false]_  
-d, --debug=[true/false] shows debug output _[default false]_  
-w, --verify-disc=[true/false] calculates and verifies a media dump format checksum/hash _[default true]_  
-s, --verify-sectors=[true/false] calculates and verifies the hash/checksum/ecc of every sector/block in the media dump _[default true]_  
