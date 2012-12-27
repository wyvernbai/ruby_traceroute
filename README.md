###ruby_traceroute
ruby_traceroute is a poor & naive traceroute just for my Net Dev homework.

---

###Usage:
```
  ruby traceroute.rb [dest_addr|host] [options] <parameters>+
  sample: ruby traceroute.rb google.com
where [options] are:
    --max-ttl, -m <i>:   Set the max time-to-live (max number of hops) used in outgoing probe packets. default: 64 (default: 64)
  --first-ttl, -f <i>:   Set the initial time-to-live used in the first outgoing probe packet. default: 1 (default: 1)
  --pack-size, -p <i>:   Set the outgoing probe packet's size in byte. default: 0 byte, max: 512 (default: 0)
       --port, -o <i>:   Protocol specific. For UDP and TCP, sets the base port number used in probes default:33434 (default: 33434)
        --version, -v:   Print version and exit
           --help, -h:   Show this message
```

---

###Demo:
```
sudo ruby traceroute.rb asiteof.me -m 128 -f 3 -p 128
```
output:
```
traceroute to asiteof.me (67.208.116.206), 128 hops max, 128 byte packets
3	61.167.60.126 (61.167.60.126)	6.258 ms
4	202.118.168.1 (202.118.168.1)	2.505 ms
5	202.118.168.73 (202.118.168.73)	2.590 ms
6	202.118.170.37 (202.118.170.37)	2.733 ms
7	202.118.170.38 (202.118.170.38)	2.837 ms
8	njqd3.cernet.net (202.112.46.233)	9.414 ms
9	202.112.62.53 (202.112.62.53)	19.887 ms
10	202.112.61.158 (202.112.61.158)	19.227 ms
11	202.112.61.14 (202.112.61.14)	19.009 ms
12	61.8.59.37 (61.8.59.37)	74.848 ms
13	gi3-0-0.cr3.hkg3.asianetcom.net (203.192.134.65)	70.266 ms
14	te0-0-2-0.wr1.hkg0.asianetcom.net (61.14.157.101)	72.220 ms
15	te0-2-0-0.wr1.osa0.asianetcom.net (61.14.157.70)	129.990 ms
16	212.6.118.110 (212.6.118.110)	171.054 ms
17	gi6-0-0.gw1.sjc1.asianetcom.net (61.14.157.98)	69.260 ms
18	202.118.253.126 (202.118.253.126)	0.016 ms
19	po2-0-1.gw2.sjc1.asianetcom.net (202.147.50.166)	175.734 ms
20	ge-11-3-1.mpr3.sjc7.us.above.net (64.125.13.101)	77.354 ms
21	xe-0-3-0.cr1.lax112.us.above.net (64.125.26.25)	193.485 ms
22	ge--2-0-0---0.car01.ekgv.ca.frontiernet.net (74.40.40.57)	259.032 ms
23	62.2.4.182 (62.2.4.182)	166.656 ms
24	212.6.118.110 (212.6.118.110)	8.601 ms
25	xe-1-1-0.er2.dfw2.us.above.net (64.125.26.214)	308.152 ms
26	64.124.196.226.t00876-01.above.net (64.124.196.226)	6.716 ms
27	206.123.64.77 (206.123.64.77)	318.681 ms
28	67.208.119.110.reverse.crucialx.net (67.208.119.110)	320.106 ms
29	202.118.253.126 (202.118.253.126)	99.457 ms
30	67.208.116.206.reverse.crucialx.net (67.208.116.206)	190.217 ms
Destination reached. Trace complete.
```
