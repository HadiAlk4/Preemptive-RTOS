# RTOS on the Raspberry Pi Pico

A small real-time operating system for the Raspberry Pi Pico. Tasks share one processor and show their work on an 8-digit seven-segment display and a USB serial shell.

Two schedulers were built.

**Non-preemptive.** Every task gets the same turn. The interval is fixed at 100 microseconds. Priority is stored and not used.

**Preemptive.** Three levels. High runs for 1 second, medium for 0.5 seconds, and low for 0.2 seconds. A new task with a higher level starts at once. The shell is medium, so a high task can cut in and a low task waits.
