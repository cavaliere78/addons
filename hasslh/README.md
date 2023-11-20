# Home Assistant Add-on: Example add-on

_This add-on provide a sslh Demux_

Fill the sslh_opts configuration options.\
The default value is
sslh_opts: "-f --user root --listen 0.0.0.0:443 --ssh 192.168.1.120:22 --anyprot 192.168.1.120:4443"

-f                               ==> foreground mode     -- DO NOT CHANGE -- 
--user root                      ==> user used by sslh   -- DO NOT CHANGE -- 
--listen 0.0.0.0:443             ==> listen port         -- DO NOT CHANGE -- 
--ssh 192.168.1.120:22           ==> ssh server:port     
--anyprot 192.168.1.120:4443     ==> others protocoll server

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
