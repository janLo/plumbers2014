# Docker and the Linux kernel

* Do not use vfs storage provider
* aufs is fast but have a lot of stability problems
  * Only recommended on ext3 or ext4
  * Problems with directIO
  * Limit of 127 layers
  * Have to dereference hardlinks
* aufs is not supported on kernels whitch not brings aufs in the first place
* devicemapper use loopmounts by default (do not use that)
* devicemappers have bugs
  * EBUSY
  * potential data corruption with ext4
* devicemapper is more work to get run
* btrfs is buggy - affect docker
  * use kernels >= 3.10
  * do not use exotic mount options
  * performance degrades when fragmentation
    * balance it
* btrfs is automatic used when docker dir is on btrfs
* btrfs seems to be recommended if you have recent kernel
* general stable
* Can be used to transfer a setup for a given workload to some testing setup
