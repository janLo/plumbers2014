# Network Queuing is all wet

* Bufferbloat!
* Netalyzr
* Demonstration: "This is a ten-gig-bottle"
* Use Fair queu or codel
* sysctl -w sys.net.core.default_qdisc=fq_codel
* Bad part: Wireless! (buffering firmware, ...)
* "Network have the same problem but hey probably cant drop packets"
