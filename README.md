# network-test
Scripts and info to test the performance of a network

## Read adapter configuration
`ip addr show`

## Network monitoring
1. [EtherApe](http://etherape.sourceforge.net)
`sudo etherape &`

2. [iftop](http://www.ex-parrot.com/pdw/iftop)
`sudo xterm -e "iftop -i wlp1s0" &`

## Link/host reliability
1. [ping](http://linux.die.net/man/8/ping)
`ping uvkkeb29ca8e.vicente-gonzalez-ruiz.koding.io`

## Route/network discovery
1. [traceroute](http://linux.die.net/man/8/traceroute)
2. [zenmap](https://nmap.org/zenmap)

## Packet/Protocol analysis
1. [tcpdump](http://www.tcpdump.org)
2. [wireshar](https://www.wireshark.org)

## Port scanning
1. [nmap](https://nmap.org)

## Bandwidth measurement
1. [opentracker](http://erdgeist.org/arts/software/opentracker/)
2. [rtorrent](https://github.com/rakshasa/rtorrent)
3. [iperf3](https://github.com/esnet/iperf)



1. Download the Big Buck Bunny movie using BitTorrent.

`iperf3 -c uvkkeb29ca8e.vicente-gonzalez-ruiz.koding.io`
