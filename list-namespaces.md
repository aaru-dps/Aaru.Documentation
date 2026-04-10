# Table of Contents

- [Command description](#command-description)
- [Command usage](#command-usage)
- [Example](#example)
- [Operating system support](#operating-system-support)

## Command description

This operation will list all the supported namespaces of the [Filesystems recognized by Aaru](faq/filesystems.md).

## Command usage

```text
USAGE:
    aaru list-namespaces [OPTIONS]

OPTIONS:
    -h, --help              Prints help information        
    -v, --verbose           Shows verbose output           
    -d, --debug             Shows debug output from plugins
        --logfile <PATH>    Path to log file               
        --pause             Pauses before exiting
```

## Example

```bash
aaru list-namespaces
```

## Operating system support

| macOS | Linux | Windows |
| ----- | ----- | ------- |
| Yes   | Yes   | Yes     |