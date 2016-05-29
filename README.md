# network-test
Scripts and info to test the performance of a network

## Read adapter/kernel configuration

`ip addr show`

`ip route show`

## Network monitoring
* [EtherApe](http://etherape.sourceforge.net)

`sudo etherape &`

* [iftop](http://www.ex-parrot.com/pdw/iftop)

`sudo xterm -e "iftop -i wlp1s0" &`

## Link/host reliability
* [ping](http://linux.die.net/man/8/ping)

`ping uvkkeb29ca8e.vicente-gonzalez-ruiz.koding.io`

## Route/network discovery
* [traceroute](http://linux.die.net/man/8/traceroute)
* [zenmap](https://nmap.org/zenmap)

## Packet/Protocol analysis
* [tcpdump](http://www.tcpdump.org)
* [wireshar](https://www.wireshark.org)

## Port scanning
* [nmap](https://nmap.org)

## Bandwidth measurement
* [opentracker](http://erdgeist.org/arts/software/opentracker/)
* [rtorrent](https://github.com/rakshasa/rtorrent)
* [iperf3](https://github.com/esnet/iperf)



1. Download the Big Buck Bunny movie using BitTorrent.

`iperf3 -c uvkkeb29ca8e.vicente-gonzalez-ruiz.koding.io`
