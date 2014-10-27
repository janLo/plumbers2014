# Network Queuing is all wet

* Bufferbloat!
* Netalyzr
* Demonstration: "This is a ten-gig-bottle"
* Use Fair queu or codel
* sysctl -w sys.net.core.default_qdisc=fq_codel
* Bad part: Wireless! (buffering firmware, ...)
* "Network have the same problem but hey probably cant drop packets"


# Systematic testing of fault handling code in Linux kernel

* Fault injection
* Describing a example
* Inject failures in filesystems and look how the code behave
* Engine that generates the failures is "opensource but not free of charge"

