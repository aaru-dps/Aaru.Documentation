In this page you can find a comparison between Aaru and other dump image managers or creators.

You can see a [[Comparison#comparison of optical discs image managers|comparison of optical discs image managers]],
a [[Comparison#comparison of floppy disk image managers|comparison of floppy disk image managers]], a 
[[Comparison#comparison of hard disk image managers|comparison of hard disk image managers]] and a
[[Comparison#comparison of digital tape image managers|comparison of digital tape image managers]].

==Comparison of optical discs image managers==
{|
!
! Aaru
! DiscImageCreator
! CDRWin
! CloneCD
! Alcohol 120%
! IsoBuster
! WinImage
|-
| Opensource
| Yes
| [https://github.com/saramibreak/DiscImageCreator Yes]
| No
| No
| No
| No
| No
|-
| Supported platforms
| Windows, Linux, macOS<ref name="notyetmacos">macOS does not yet support dumping media, only managing existing images</ref>
| Windows
| Windows
| Windows
| Windows
| Windows
| Windows
|-
| Supported formats
| [https://github.com/aaru-dps/Aaru/blob/master/README.md#supported-disk-image-formats-read-and-write 12]
| 3<ref name="discimagecreator">CDRWin, CloneCD and raw</ref>
| 1<ref name="cdrwin">CDRWin</ref>
| 1<ref name="clonecd">CloneCD</ref>
| 1<ref name="alcohol">Alcohol 120%</ref>
| 17<ref name="isobuster">Alcohol 120%, BlindWrite 5, BlindWrite 6, CD-i OptImage, CDRWin, CloneCD, DiscJuggler, Easy CD Creator, IsoBuster, Nero, NTI, PlexTools, Prassi PrimoCD, Prassi PrimoDVD, raw, Virtual CD and WinOnCD</ref>
| 1<ref name="winimage">Raw</ref>
|-
| Can dump Audio CD
| Yes<ref name="audiocd">It can lose a few seconds from start of audio on some discs</ref>
| Yes
| Yes
| Yes
| Yes
| Yes
| No
|-
| Can dump Mode 0 tracks
| Yes
| No
| No
| No
| No
| No
| No
|-
| Can dump Mode 1 tracks
| Yes
| Yes
| Yes
| Yes
| Yes
| Yes
| Yes
|-
| Can dump Mode 2 tracks
| Yes<ref name="audiocd">It can lose a few seconds from start of audio on some discs</ref>
| Yes
| Yes
| Yes
| Yes
| Yes
| Yes
|-
| Can dump multisession discs
| Yes
| Yes
| No
| Yes
| Yes
| Yes
| No
|-
| Can dump discs with errors
| Yes<ref name="partialdata">Depending on the drive it can recover data from sectors with errors</ref>
| Yes<ref name="fakedata">Writes fake data in the place of sectors with errors</ref>
| No<ref name="ignoreerrors">Ignores errors or stops on error</ref>
| Yes<ref name="fakedata"/>
| Yes<ref name="fakedata"/>
| Unknown
| Unknown
|-
| Reads subchannel
| Yes
| Yes
| No<ref name="cdg">Only if it detects the disc is | No
a CD+G</ref>
| Yes
| Yes
| Unknown
| No
|-
| Reads lead-in postgap
| Yes
| Yes
| No
| No
| No
| No
| No
|-
| Supports illegal TOCs
| Yes
| Yes
| No
| Yes
| Yes
| Yes
| No
|-
| Supports error based copy protections
| Yes
| Yes
| No
| Yes
| Yes
| Yes
| No
|-
| Supports twin sectors based copy protections
| Not yet<ref name="pendingformat">Pending format support</ref>
| No
| No
| No
| No
| No
| No
|-
| Supports position based copy protections
| Not yet<ref name="pendingformat"/>
| No
| No
| No
| Yes
| No
| No
|-
| Supports dumping DDCD
| Yes
| No<ref name="noddcd">None of its supported formats support the DDCD media</ref>
| No<ref name="noddcd"/>
| No<ref name="noddcd"/>
| No<ref name="noddcd"/>
| No<ref name="noddcd"/>
| No<ref name="noddcd"/>
|-
| Supports dumping GD
| Not yet<ref name="nextrelease">Feature will be added in next release</ref>
| Yes
| No
| No
| No
| No
| No
|-
| Supports dumping GameCube/Wii
| Not yet<ref name="nextrelease"/>
| Yes
| No
| No
| No
| No
| No
|-
| Supports dumping DVD<ref name="nocrypt">Does not include encrypted video media</ref><ref name="includedvd">Includes PlayStation DVD</ref>
| Yes
| Partial<ref name="losspfi">Customized PFI information, like PSN of start LBA in DVD-RAM will be lost</ref>
| No
| No
| Partial<ref name="losspfi"/>
| Partial<ref name="losspfi"/>
| Partial<ref name="losspfi"/>
|-
| Supports dumping HD DVD<ref name="nocrypt"/>
| Yes
| Partial<ref name="losshdpfi">Customized PFI information, like PSN of start LBA in HD DVD-RAM will be lost</ref>
| No
| No
| Partial<ref name="losshdpfi"/>
| Partial<ref name="losshdpfi"/>
| Partial<ref name="losshdpfi"/>
|-
| Supports dumping Blu-ray<ref name="nocrypt"/><ref name="includebd">Includes PlayStation Blu-ray</ref>
| Yes
| Yes
| No
| No
| Yes
| Yes
| Yes
|-
| Supports dumping Xbox Game discs
| Yes<ref name="xgd2untested">XGD2 are untested</ref><ref name="noxgd3">XGD3 are not supported</ref>
| Yes<ref name="noxgd3"/>
| No
| No
| No
| No
| No
|}

<references>