irqbetter
=========

Usage:
  ./irqbetter [OPTIONS] INTERFACE [INTERFACE]...

Description:
  This script attempts to bind each queue interrupt of a multi-queue
  NICs each to a different core.  If the NIC has seperate tx and rx
  queues, it will bind each set to the same core, ie:
  tx0|rx0 --> cpu0, tx1|rx1 --> cpu1.

Options:
  -t, --test    show what the affinities of each interrupt will be
                before and after running the script without actually
                changing them
  -p, --print   show the affinities found in /proc/irq/*/smp_affinity
      --hint    show the hints found in /proc/irq/*/affinity_hint
  -h, --help    show this help
