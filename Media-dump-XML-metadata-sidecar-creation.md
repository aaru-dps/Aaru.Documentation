# Command description
This operation will analyze a media dump, and if the format is recognized, create a CICM XML metadata sidecar with all information that can be get about it, as well as all [[supported checksum algorithms|Supported-checksums]].

# Command usage
DiscImageChef verify -i \<dump\> -v [true/false] -d [true/false] 

-i, --input=\<dump\> path to the media dump image  
-v, --verbose=[true/false] shows verbose output _[default false]_  
-d, --debug=[true/false] shows debug output _[default false]_  
-p, --partitions=[true/false] searches and interprets partitions _[default true]_  
-f, --filesystems=[true/false] searches and interprets filesystems _[default true]_  

