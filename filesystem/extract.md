# Table of Contents

- [Command Description](#command-description)
- [Command usage](#command-usage)
- [Example](#example)
- [Operating system support](#operating-system-support)

## Command description

This operation will analyze and find all filesystems in a media dump, then extract the files that are contained
in [supported filesystems.](../faq/filesystems.md)

## Command usage

```bash
Aaru -d [true/false] -v [true/false] filesystem extract -h [true/false] -e [encoding] -O <options> -x [true/false] -n <namespace>
```

`-d, --debug [true/false]` shows debug output *(default false)*                
`-v, --verbose [true/false]` shows verbose output *(default false)*                  
`-h, --help [true/false]` shows help screen for the command instead of running it, ignores all other switches *(default
false)*                       
`-e, --encoding [encoding]` sets which encoding is used by the contents of the media dump *(default varies by
filesystem)*        
`-O, --options <options>` specifies comma separated name=value pairs of options to pass to output filesystem
plugin            
`-x, --xattrs [true/false]` extracts extended attributes if present *(default false)*          
`-n, --namespace <namespace>` specifies namespace to use for filenames *(default varies by filesystem)*

## Example

```bash
Aaru filesystem extract -x -e iso8859-15 mydisc.cue contents
```

## Operating system support

| FreeBSD | macOS | Linux | Windows |
| ------- | ----- | ----- | ------- |
| Yes     | Yes   | Yes   | Yes     |

