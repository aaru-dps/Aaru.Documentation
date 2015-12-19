# Command description
This operation will analyze a media dump, and if the format is recognized and you choose so, it will search for [[supported partitioning schemes|partitions]] and [[supported filesystems|filesystems]] on the dump, showing information about them.

# Command usage
DiscImageChef analyze -i \<dump\> -p [true/false] -f [true/false] -v [true/false] -d [true/false]

-i, --input=\<dump\> path to the media dump image  
-p, --partitions=[true/false] searches and interprets partitions [default true]  
-f, --filesystems=[true/false] searches and interprets filesystems [default true]  
-v, --verbose=[true/false] shows verbose output  
-d, --debug=[true/false] shows debug output  

