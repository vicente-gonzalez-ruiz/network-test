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

`sudo traceroute -I uvkkeb29ca8e.vicente-gonzalez-ruiz.koding.io`

* [tracepath](http://linux.die.net/man/8/tracepath)

`tracepath uvkkeb29ca8e.vicente-gonzalez-ruiz.koding.io`

* [nmap](https://nmap.org)/[zenmap](https://nmap.org/zenmap)

`sudo nmap -traceroute uvkkeb29ca8e.vicente-gonzalez-ruiz.koding.io`

`sudo zenmap -t uvkkeb29ca8e.vicente-gonzalez-ruiz.koding.io -p "Quick traceroute"` &

## Host discovery
* [nmap](https://nmap.org)

`sudo nmap -sP 192.168.1.0/24`

## Packet-sniffing/Protocol analysis
* [tcpdump](http://www.tcpdump.org)
 
`sudo tcpdump | grep "your filter here"

* [wireshar](https://www.wireshark.org)

`sudo tshark | grep "your filter here"`

## Port scanning
* [nmap](https://nmap.org)

`sudo nmap -v -p1-1024,5201 uvkkeb29ca8e.vicente-gonzalez-ruiz.koding.io`

## Bandwidth stress
* [iperf3](https://github.com/esnet/iperf)

`iperf3 -P 2 -t 0 -c uvkkeb29ca8e.vicente-gonzalez-ruiz.koding.io` # TCP upload 

`iperf3 -P 2 -t 0 -R -c uvkkeb29ca8e.vicente-gonzalez-ruiz.koding.io` # TCP download

`iperf3 -P 2 -t 0 -u -b 0 -c uvkkeb29ca8e.vicente-gonzalez-ruiz.koding.io` # UDP upload


* [opentracker](http://erdgeist.org/arts/software/opentracker/)+[rtorrent](https://github.com/rakshasa/rtorrent)

`wget wget http://www.frostclick.com/torrents/video/animation/Big_Buck_Bunny_1080p_surround_frostclick.com_frostwire.com.torrent`

`mktorrent Big_Buck_Bunny_1080p_surround_frostclick.com_frostwire.com -a -p 127.0.0.1:6969`

1. Download the Big Buck Bunny movie using BitTorrent.

`iperf3 -c uvkkeb29ca8e.vicente-gonzalez-ruiz.koding.io`
