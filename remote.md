# Table of Contents

- [Command description](#command-description)
- [Command usage](#command-usage)
- [Example](#example)
- [Operating system support](#operating-system-support)

## Command description

This operation tests the connection between Aaru and the specified Aaru Remote Server.

## Command usage

```text
USAGE:
    aaru remote <host> [OPTIONS]

ARGUMENTS:
    <host>    aaruremote host

OPTIONS:
    -h, --help              Prints help information        
    -v, --verbose           Shows verbose output           
    -d, --debug             Shows debug output from plugins
        --logfile <PATH>    Path to log file               
        --pause             Pauses before exiting
```

## Example

```bash
aaru remote aaru://192.168.1.25
```

## Operating system support

| macOS | Linux | Windows |
| ----- | ----- | ------- |
| Yes   | Yes   | Yes     |