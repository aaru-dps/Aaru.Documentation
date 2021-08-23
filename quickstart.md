# Quickstart

## How to Dump a Disk Image

It’s very easy to dump any supported media quickly with Aaru! You just have to
run `aaru media dump <drive> <output image>` for the most basic options. If you dump to something that’s not Aaru Image
Format (images with the extensions `.aaruformat`, `.aaruf`, and `.aif`), you will also have to add the “-f” option at the end
of the command.

### Examples (Windows):

`aaru media dump E: Image.aaruf`

`aaru media dump F: Image.iso -f`

### Examples (Linux):

`aaru media dump /dev/sr0 Image.aaruf`

`aaru media dump /dev/sr1 Image.iso -f`

## Comparing Between Two Media Dumps

Comparing between media dumps using Aaru is simple! All you have to do is run the
command `aaru image compare image-1 image-2`. Neither of the dumps being compared have to be created by Aaru, they can
be any of the supported formats from any software.

### Examples (All OS’):

`aaru image compare Image1.aaruf Image2.cue`

`aaru image compare Image1.iso Image2.ccd`

## Analysing a Media Dump

WIP

## Extracting Content From a Media Dump

Aaru can extract the files from any supported media dump, as long as it uses a supported filesystem to store its files.
The command for this is “aaru filesystem extract *Image* *Output folder*”. You can also add “-x” to the end of the
command to extract the more technical extended attributes from an image as well.

### Examples:

`aaru filesystem extract Image.aaruf Output`

`aaru filesystem extract Image.ccd Output -x`

## Extracting audio from an Audio CD

While Aaru does not directly support extracting audio from an audio CD image, there are multitudes of software that can. First, if the image is an Aaru Format Image, you have to convert it to a more common format. For example, you can bchunk (https://github.com/extramaster/bchunk) to extract the audio to WAV if you convert the image to CUE.



## Listening to audio from an Aaru Format Image

While Aaru itself isn't able to play any audio, another part of the Aaru Data Preservation Suite can! RedBookPlayer (https://github.com/aaru-dps/RedBookPlayer) was specifically created in order to play audio from Aaru Format Images, which is also the only image format supported by it. Although it isn't fully stable or feature complete yet, the core functionality (and then some) is already present, so it's more than worth the time to look into if you want to listen to the audio on your Aaru Format Images!

 

## Why do so many recordable CDs have 2-3 errors at the end of the disc?

The simplified answer is that it seems that these sectors aren't actually meant to contain data, and are purely a side effect of burning a recordable CD in the TAO burning mode.



## Caution when dumping a large HDD

As of 5.3, dumping a large HDD as an Aaru Format Image has very significant speed issues, and if you want to bypass this, it's recommended to dump to the QCOW2 image format instead. This image can then be mounted using guestmount on most Linux distributions, and can also be navigated quite easily using 7-zip (https://www.7-zip.org/).



## Extracting files from NTFS/HFS/HFS+/etc. filesystems

Unfortunately, Aaru does not support extracting from several well known filesystems at the moment, some notable ones include NTFS, HFS, and HFS+. In cases like these, if you have an Aaru Format Image, you have to convert it to a more well known image format and use other software to mount and/or navigate it. 
