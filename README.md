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

`ping -s 1000 uvkkeb29ca8e.vicente-gonzalez-ruiz.koding.io`

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
 
`sudo tcpdump | grep "your filter here"`

* [wireshar](https://www.wireshark.org)

`sudo tshark | grep "your filter here"`

## Port scanning
* [nmap](https://nmap.org)

`sudo nmap -v -p1-1024,5201 uvkkeb29ca8e.vicente-gonzalez-ruiz.koding.io`

## Bandwidth stress
* [iperf3](https://github.com/esnet/iperf)

`uvkkeb29ca8e.vicente-gonzalez-ruiz.koding.io$ iperf3 -s`

`other$ iperf3 -P 2 -t 0 -c uvkkeb29ca8e.vicente-gonzalez-ruiz.koding.io` # TCP upload 

`other$ iperf3 -P 2 -t 0 -R -c uvkkeb29ca8e.vicente-gonzalez-ruiz.koding.io` # TCP download

`other$ iperf3 -P 2 -t 0 -u -b 0 -c uvkkeb29ca8e.vicente-gonzalez-ruiz.koding.io` # UDP upload


* [youtube-dl](https://rg3.github.io/youtube-dl/)+[opentracker](http://erdgeist.org/arts/software/opentracker)+[mktorrent](http://mktorrent.sourceforge.net)+[qbittorrent](http://www.qbittorrent.org)

`host1$ opentracker -i 0.0.0.0 -p 9000 &` # Listen to any interface

`host1$ youtube-dl https://www.youtube.com/watch?v=YE7VzlLtp-4`

`host1$ mktorrent -v -p -a http://<the_"public"_IP_address_of_host1_without"<>">:9000/announce big_buck_bunny_1280x738.mp4` # Create the .torrent file

`host1$ qbittorrent big_buck_bunny_1280x738.mp4.torrent &` # Serve (as a seeder) the video

`host2$ scp username@host1:big_buck_bunny_1280x738.mp4.torrent .`

`host2$ qbittorrent big_buck_bunny_1280x738.mp4.torrent &` # Download the file

