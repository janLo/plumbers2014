# Automatic NUMA Balancing

* Active balancing (Task placement)
* Strategies
  * Cpu follows memory (Task placement)
  * Memory follows cpu
  * see slides
* Slides!
* Scan the system for page faults
  * Build statistics (slide 17)
  * Move tasks ori pages to the optimal node
* Problems with task placement
  * Not every task fits in one node
  * Never create an imbalance
  * Placement algorithm is at the slides
* Use page false statistics to group tasks (processes)
  * better when they used shared memory
* Tasks with multiple threads and shared memory: "Pseudo interleaving" 
  * Slides have best explanation
* Backplane topology placement policy detects which nodes are better connected than others
  * Tries to group nodes and place tasks in groups
* Problems:
  * There will no statistics for unmoveable memory
    * Big problem
  * KSM
    * Not worth investigting (better 20% slower pagefaults than swap)
  * Interrupt locality
    * Today not investigated
    * What is the priority: interrupt or memory?
  * IPC
    * Not yet investigated
    * Unclear to implement
    * Similar problem like interrupt locality
* Its all heuristics
* If you need IRQ affinity - do it manually
* tasks will only moved to allowed nodes
  * does not interference with pinning
  * if you pin a task to two nodes it will be moved only between this
* it only works for processes that uses some seconds of cpu time
* Manually assign numa architecture to a kvm guest and run automatic
  balancing will work and help the host to figure out what should be optimal

