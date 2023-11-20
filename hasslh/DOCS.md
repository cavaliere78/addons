# Home Assistant Add-on: sslh add-on

## This add-on provide a sslh Demux.
_Fill the sslh_opts configuration options. !_\
the default value is
sslh_opts: "-f --user root --listen 0.0.0.0:443 --ssh 192.168.1.120:22 --anyprot 192.168.1.120:4443"

-f                               ==> foreground mode     -- DO NOT CHANGE -- 
--user root                      ==> user used by sslh   -- DO NOT CHANGE -- 
--listen 0.0.0.0:443             ==> listen port         -- DO NOT CHANGE -- 
--ssh 192.168.1.120:22           ==> ssh server:port     
--anyprot 192.168.1.120:4443     ==> others protocoll server
