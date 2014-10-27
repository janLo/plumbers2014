# Ftrace Kernel Hooks: More than just tracing

* Simple to use through debugfs
* /sys/kernel/debug/tracing
* https://www.kernel.org/doc/Documentation/trace/ftrace.txt
* call o register_ftrace_function()

## News:

* Dynamic function traces (dynamic trampolines)
  * perf vs ftrace ( different targets)
  * list_func calls all registred tracers - even if they are not interested
  * iteration trough both is not optimal
  * problem: when to free dynamic trampoline
* fentry
* Live kernel patching
  * instead using ftrace ops - replace ftrace hook with the new func

