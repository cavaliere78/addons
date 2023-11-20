# Home Assistant Add-on: sslh add-on

## This add-on provide a sslh Demux.
This addon provide a sslh demux
It can demix the input traffic to a specific server:port basing on the protocoll used in the incoming request.

#### Installation
Add below repository to your Home assitant:\
    https://github.dev/cavaliere78/addons/

#### Configuration

In the configuration fill the sslh_opts oprions with a valid option strig for sslh.\
the default value is:\
sslh_opts: "-f --user root --listen 0.0.0.0:443 --ssh 192.168.1.120:22 --anyprot 192.168.1.120:4443"

-f                               ==> foreground mode     -- DO NOT CHANGE -- \
--user root                      ==> user used by sslh   -- DO NOT CHANGE -- \
--listen 0.0.0.0:443             ==> listen port         -- DO NOT CHANGE -- \
--ssh 192.168.1.120:22           ==> ssh server:port     \
--anyprot 192.168.1.120:4443     ==> others protocoll server
