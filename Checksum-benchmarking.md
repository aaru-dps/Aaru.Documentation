# Command description
This operation will create random data in RAM and calculate how fast are we calculating all known [[checksums and hashes|Supported-checksums]]

# Command usage
DiscImageChef benchmark -v [true/false] -d [true/false] -b [block size] -s [buffer size]

-v, --verbose=[true/false] shows verbose output _[default false]_  
-d, --debug=[true/false] shows debug output _[default false]_  
-b, --block-size=[block size] how big in bytes to do each block _[default 512]_  
-s, --buffer-size=[buffer size] how big in mebibytes to create the random data _[default 128]_  
