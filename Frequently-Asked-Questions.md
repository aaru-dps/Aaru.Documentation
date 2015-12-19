# Why the name, why DiscImageChef?
Because a chef is someone that takes raw ingredients and according to a recipe makes magic with them, and so DiscImageChef does with media dump images.

# Which operating systems does DiscImageChef work under?
Any operating system with a .NET runtime should work. Has been tested under Windows, Linux, Mac OS X and FreeBSD.

# Will you implement physical device support for Mac OS X?
No. The Mac OS X kernel severely limits what commands a user application can send to physical devices to a limited list of known commands and to some specific devices. While some people has created kernel extensions enhancing this ability, I don't have the time to create or test them, and also, El Capitan rootless mode has made their usage more complicated than simply running Linux from a live USB.

# Will you implement physical device support for FreeBSD?
Yes, after Linux and Windows are fully tested.

# Will you support dumping media?
Yes, that is currently being actively developed and should be ready in 1Q2016.

# Will you support media dump image format XXXX?
If you can send me documentation, test images and/or the application that creates them, I will do my best to.

# Will you support browsing filesystem contents?
Yes, but not soon, first I will try to support as much image formats and devices as possible.

# Will you create a graphical interface for DiscImageChef?
After all features are implemented (analyze, dump, browse), I will.

# Can I use any of your modules?
As long as you comply with the GPL license, yes. I would thank you if you tell me where you're using them.

# Can I use the CICM XML metadata sidecar format in my project?
Of course, I invite you to use it extensively and provide me with as much feedback as you can.

# I have tried DiscImageChef and found a bug, how can I tell you?
Please don't send me an email, it will simply fall in oblivion. Github has a pretty nice bug tracker, just click [Issues](https://github.com/claunia/DiscImageChef/issues) and create a New Issue, that way the bug will not be forgotten and you can follow progress on its solution.