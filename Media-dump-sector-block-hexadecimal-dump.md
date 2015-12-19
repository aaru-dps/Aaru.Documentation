# Command description
This operation will print in console a hexadecimal dump of the chosen sector/block of the indicated media dump image.

# Command usage
DiscImageChef printhex -i \<dump\> -v [true/false] -d [true/false] -s \<starting sector\> -l [sectors] -r [true/false] -w [width]

-i, --input=\<dump\> path to the media dump image  
-v, --verbose=[true/false] shows verbose output _[default false]_  
-d, --debug=[true/false] shows debug output _[default false]_  
-s, --start=\<starting sector\> starts the hexadecimal printing from this sector  
-l, --length=[sectors] how many sectors to print _[default 1]_  
-r, --long-sectors=[true/false] if hex print should include all [[sector tags|Sector-Tags]] stored in the media dump _[default false]_  
-w, --width=[width] how width, in characters, should the print be before creating a new line _[default 32]_  
