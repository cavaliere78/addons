# sslh addon for Home Assistant

_This add-on provide an sslh Demux_

## Description

It can demux the input traffic to a specific server:port basing on the protocol used in the incoming request.
The recognized protocols are:
```markdown
  --ssh=<host:port>             Set up ssh target
  --tls=<host:port>             Set up TLS/SSL target
  --openvpn=<host:port>         Set up OpenVPN target
  --tinc=<host:port>            Set up tinc target
  --wireguard=<host:port>       Set up WireGuard target
  --xmpp=<host:port>            Set up XMPP target
  --http=<host:port>            Set up HTTP (plain) target
  --adb=<host:port>             Set up ADB (Android Debug) target
  --socks5=<host:port>          Set up socks5 target
  --syslog=<host:port>          Set up syslog target
  --msrdp=<host:port>           Set up msrdp target
  --anyprot=<host:port>         Set up default target
```


## Installation

Copy the repository url https://github.com/cavaliere78/addons 
into "Supervisor" -> "Addon Store" -> "Add New repository URL" after install hasslh from it.

## Configuration 
#### Options:
```yaml
sslh_opts: -f --user root --listen 0.0.0.0:443 --ssh 192.168.1.120:22 --anyprot 192.168.1.120:4443
```
_the port used internally is the 443 so do not change --listen 0.0.0.0:443 to others values_
#### Port mapping:
```yaml
443:443
```
_default port mapping is on the port 443_
### Option `sslh_opts`

Set this to the option that will be passed to the sslh comand.

#### Usage:
```html
 [-Vfin] [-F <file>] [--verbose-config=<n>] [--verbose-config-error=<n>] [--verbose-connections=<n>] [--verbose-connections-try=<n>] [--verbose-connections-error=<n>] [--verbose-fd=<n>] [--verbose-packets=<n>] [--verbose-probe-info=<n>] [--verbose-probe-error=<n>] [--verbose-system-error=<n>] [--verbose-int-error=<n>] [--transparent] [-t <n>] [--udp-max-connections=<n>] [-u <str>] [-P <file>] [-C <path>] [--syslog-facility=<str>] [--logfile=<str>] [--on-timeout=<str>] [--prefix=<str>] [-p <host:port>]... [--ssh=<host:port>]... [--tls=<host:port>]... [--openvpn=<host:port>]... [--tinc=<host:port>]... [--wireguard=<host:port>]... [--xmpp=<host:port>]... [--http=<host:port>]... [--adb=<host:port>]... [--socks5=<host:port>]... [--syslog=<host:port>]... [--msrdp=<host:port>]... [--anyprot=<host:port>]...
  -F, --config=<file>           Specify configuration file
  --verbose-config=<n>          Print configuration at startup
  --verbose-config-error=<n>    Print configuration errors
  --verbose-connections=<n>     Trace established incoming address to forward address
  --verbose-connections-try=<n> Connection errors
  --verbose-connections-error=<n>       Connection attempts towards targets
  --verbose-fd=<n>              File descriptor activity, open/close/whatnot
  --verbose-packets=<n>         Hexdump packets on which probing is done
  --verbose-probe-info=<n>      Trace the probe process
  --verbose-probe-error=<n>     Failures and problems during probing
  --verbose-system-error=<n>    System call failures
  --verbose-int-error=<n>       Internal errors that should never happen
  -V, --version                 Print version information and exit
  -f, --foreground              Run in foreground instead of as a daemon
  -i, --inetd                   Run in inetd mode: use stdin/stdout instead of network listen
  -n, --numeric                 Print IP addresses and ports as numbers
  --transparent                 Set up as a transparent proxy
  -t, --timeout=<n>             Set up timeout before connecting to default target
  --udp-max-connections=<n>     Number of concurrent UDP connections
  -u, --user=<str>              Username to change to after set-up
  -P, --pidfile=<file>          Path to file to store PID of current instance
  -C, --chroot=<path>           Root to change to after set-up
  --syslog-facility=<str>       Facility to syslog to
  --logfile=<str>               Log messages to a file
  --on-timeout=<str>            Target to connect to when timing out
  --prefix=<str>                Reserved for testing
  -p, --listen=<host:port>      Listen on host:port
  --ssh=<host:port>             Set up ssh target
  --tls=<host:port>             Set up TLS/SSL target
  --openvpn=<host:port>         Set up OpenVPN target
  --tinc=<host:port>            Set up tinc target
  --wireguard=<host:port>       Set up WireGuard target
  --xmpp=<host:port>            Set up XMPP target
  --http=<host:port>            Set up HTTP (plain) target
  --adb=<host:port>             Set up ADB (Android Debug) target
  --socks5=<host:port>          Set up socks5 target
  --syslog=<host:port>          Set up syslog target
  --msrdp=<host:port>           Set up msrdp target
  --anyprot=<host:port>         Set up default target
```
![Supports aarch64 Architecture][aarch64-shield]
![Supports amd64 Architecture][amd64-shield]
![Supports armhf Architecture][armhf-shield]
![Supports armv7 Architecture][armv7-shield]
![Supports i386 Architecture][i386-shield]

[aarch64-shield]: https://img.shields.io/badge/aarch64-yes-green.svg
[amd64-shield]: https://img.shields.io/badge/amd64-yes-green.svg
[armhf-shield]: https://img.shields.io/badge/armhf-yes-green.svg
[armv7-shield]: https://img.shields.io/badge/armv7-yes-green.svg
[i386-shield]: https://img.shields.io/badge/i386-yes-green.svg
