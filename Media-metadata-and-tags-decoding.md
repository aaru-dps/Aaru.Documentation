# Command description
This operation will decode all [[sector tags|Sector-tags]] and [[media tags|Media-tags]] on a media dump image.

# Command usage
DiscImageChef decode -i \<dump\> -v [true/false] -d [true/false] -s [start sector] -l [sectors] -k [true/false] -t [true/false]

-i, --input=\<dump\> path to the media dump image  
-v, --verbose=[true/false] shows verbose output _[default false]_  
-d, --debug=[true/false] shows debug output _[default false]_  
-s, --start=[start-sector] starting sector _[default 0]_  
-l, --length=[sectors] how many sectors to decode or _all_ to decode all _[default all]_  
-k, --disk-tags=[true/false] decodes all [[media tags|Media-tags]] _[default true]_  
-t, --sector-tags=[true/false] decodes all [[sector tags|Sector-tags]] _[default true]_
