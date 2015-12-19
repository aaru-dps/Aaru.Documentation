# Command description
This operation will analyze a media dump, and if the format is recognized and you choose so, it will search for [[supported partitioning schemes|Partitioning-schemes-recognized-by-DiscImageChef]] and [[supported filesystems|Filesystems-recognized-by-DiscImageChef]] on the dump, showing information about them.

# Command usage
DiscImageChef analyze -i \<dump\> -v [true/false] -d [true/false] -p [true/false] -f [true/false] 

-i, --input=\<dump\> path to the media dump image  
-v, --verbose=[true/false] shows verbose output _[default false]_  
-d, --debug=[true/false] shows debug output _[default false]_  
-p, --partitions=[true/false] searches and interprets partitions _[default true]_  
-f, --filesystems=[true/false] searches and interprets filesystems _[default true]_  

