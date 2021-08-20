# Aaru Remote

The Aaru Remote is a slim, miniature application designed to receive device commands from a remote [Aaru](https://github.com/aaru-dps/Aaru)
instance, send it to a local device, and return the data to the instance.

The main motivation for this is the desire to update Aaru to the latest and greatest features of .NET and C#.
This creates a problem, as some people have old devices that do not work in modern Linux distributions.

This remote will support older versions of Linux and will, in future versions, be supported in FreeBSD, Windows, and possibly
network-enabled game consoles (like PSP, Wii, etc.).

While some people will suggest porting the whole Aaru to C or C++, that won't happen. For the only situation that
would be needed (accessing devices where C# does not run) this application is more than enough.

The usage is very simple, just run the remote and it will listen for a connection over TCP/IP in port 6666 then print out
the available IPs. Running as non-root user only works with some SCSI devices, so it is better to run as root.

On the other side, you can use the Aaru with the [remote](../remote.md) command and one of those IP addresses to test the
connection. Similarly, using the IP address as an argument for the *list-devices* command will list the devices available
remotely.

All commands that support devices are supported, with a URI with the following schema:
`aaru://<IP ADDRESS>/<DEVICE PATH>`.

## Feature matrix

|              | Minimum OS¹ | SCSI | CHS ATA | 28-bit LBA ATA | 48-bit LBA ATA | Secure Digital | MultiMediaCard | USB      | FireWire | PCMCIA | Special² |
|--------------|-------------|------|---------|----------------|----------------|----------------|----------------|----------|----------|--------|----------|
| FreeBSD      | 12          | Yes  | Yes     | Yes            | Yes            | Not yet        | Not yet        | Not yet⁴ | Not yet⁴ | No⁵    |          |
| Linux        | 2.6         | Yes  | Yes     | Yes            | Yes            | Yes            | Yes            | Yes      | Yes      | Yes⁶   |          |
| Nintendo Wii | 4.3         | No³  | No³     | No³            | No³            | Not yet        | Not yet        | Not yet  | No³      | No³    | Not yet  |
| Windows NT   | XP          | Yes  | Yes     | Yes            | Yes            | Yes            | Yes            | Yes      | Not yet⁴ | No⁵    |          |

1. Minimum operating system version where aaruremote has been tested. May work on early version.
2. Special storage media only available on that environment.
3. Hardware not available or supported by the operating system.
4. As SCSI device, not possible to retrieve special data.
5. As ATA device, not possible to retrieve special data.
6. Only ATA devices, not linear memory devices.

## TODO

- More buffer overflow guards
- Support PSP
- Support Wii
- Support Wii U
- Support connections thru serial port
- Timing under Linux

Licensed under the *GPLv3 license*.