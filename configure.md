# Table of Contents

- [Command description](#command-description)
- [Command usage](#command-usage)
- [Example](#example)
- [Operating system support](#operating-system-support)

## Command description

This command will ask you which statistics to gather and if you want to share them anonymously. When sharing, no
information about you or your computer will be sent or stored, only the number of times a command have been used and the
operating system where Aaru is run. This information is not, and will never be, sold to any third party. Collected information is publicly
available at [https://www.aaru.app](https://www.aaru.app)

## Command usage

```text
USAGE:
    aaru configure [OPTIONS]

OPTIONS:
    -h, --help              Prints help information        
    -v, --verbose           Shows verbose output           
    -d, --debug             Shows debug output from plugins
        --logfile <PATH>    Path to log file               
        --pause             Pauses before exiting
```

## Example

```bash
aaru configure
```

## Operating system support

| macOS | Linux | Windows |
| ----- | ----- | ------- |
| Yes   | Yes   | Yes     |