# Network Virtualization Security Microconference

* Notes at https://etherpad.fr/p/LPC2014_NetVirt


# File and Storage Systems Microconference

* Notes at https://etherpad.fr/p/LPC2014_Storage
* Grub2 can now boot from btrfs snapshots


# Linux packet processing performance improvements

* Unlocked full potential of the driver
* Implemented bulking in qdisc layer
* Pktgen 15.8Mpps on a single core (10G wirespeed)
* skb have xmit_more indicator
  * defer (expensive) writes to hw
* Hard part: bulk without add latency
* if skb->next btw - xmit_more
* RX optimization has started
  * highly tuned setups at 6.5  Mpps
  * Forward only 1-2 Mpps
  * Patches shows from 6.5 to 9.4 Mpps via build_skb() prefetch tuning
* Slides: http://people.netfilter.org/hawk/presentations/
