# Command description
This operation will calculate uniqueness and entropy of the media represented by a media dump image. It's not affected my the image format compression if applicable.

# Command usage
DiscImageChef entropy -i \<dump\> -v [true/false] -d [true/false] -p [true/false] -t [true/false] -w [true/false] 

-i, --input=\<dump\> path to the media dump image  
-v, --verbose=[true/false] shows verbose output _[default false]_  
-d, --debug=[true/false] shows debug output _[default false]_  
-p, --duplicated-sectors=[true/false] besides entropy also calculates how many sectors have the exact same data in their user area _[default true]_  
-t, --separated-tracks=[true/false] separately calculates the entropy for each track dividing the media. Only applicable to certain kind of media (optical discs and digital tapes mostly) _[default true]_  
-w, --whole-disc=[true/false] calculates the entropy for the whole media _[default true]_
