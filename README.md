# PacketQ - use SQL on PCAP files

PacketQ is a command line tool to run sql queries directly on pcap files.

However, PacketQ also contain a very simplistic webserver in order 
to inspect pcap files remotely and a simple GUI.

Sample command lines:

    packetq -s "select * from dns limit 10" sample.pcap

Retrives the 10 first packets containing dns information from the file "sample.pcap"

    packetq -d -p8080 -w html/ -r pcap/

Starts a webserver on port 8080 (-p8080) as a daemon (-d) servering files from the 
directory html/ (-w html/) and pcapfiles from the directory pcap/ (-r pcap/).

To install: download this repository and then type

    ./configure; make; make install

IIS has closed down the previous dotse repository, but the information
on the wiki is still available for more information:
https://github.com/dotse/packetq/wiki

A new mailing list has been setup for discussion on the future of PacketQ:
https://vic20.blipp.com/mailman/listinfo/packetq

A short demo-video of PacketQs capabilities is available on
http://www.youtube.com/watch?v=70wJmWZE9tY

The software is distributed under the BSD license, see full license text
in the [COPYING document](COPYING).
