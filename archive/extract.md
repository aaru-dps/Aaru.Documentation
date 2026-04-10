# Table of Contents

- [Command description](#command-description)
- [Command usage](#command-usage)
- [Example](#example)
- [Operating system support](#operating-system-support)

## Command description

This operation will extract the contents of an archive file to the selected output directory.

## Command usage

```text
USAGE:
    aaru archive extract <path> <output> [OPTIONS]

ARGUMENTS:
    <path>      Archive file path                                               
    <output>    Directory where extracted files will be created. Will abort if  
                it exists                                                       

OPTIONS:
    -h, --help        Prints help information               
    -e, --encoding    Name of character encoding to use     
    -x, --xattrs      Extract extended attributes if present
```

## Example

```bash
aaru archive extract example.zip output
```

## Operating system support

| macOS | Linux | Windows |
| ----- | ----- | ------- |
| Yes   | Yes   | Yes     |