# Table of Contents

- [Command description](#command-description)
- [Command usage](#command-usage)
- [Example](#example)
- [Operating system support](#operating-system-support)

## Command description

This operation will list all character set encodings supported in your environment. This list depends on the libraries
installed on your system, so if an encoding is available in one environment there are no guarantees it will be available
in another one.

## Command usage

```text
USAGE:
    aaru list-encodings [OPTIONS]

OPTIONS:
    -h, --help              Prints help information        
    -v, --verbose           Shows verbose output           
    -d, --debug             Shows debug output from plugins
        --logfile <PATH>    Path to log file               
        --pause             Pauses before exiting
```

## Example

```bash
aaru list-encodings
```

## Operating system support

| macOS | Linux | Windows |
| ----- | ----- | ------- |
| Yes   | Yes   | Yes     |