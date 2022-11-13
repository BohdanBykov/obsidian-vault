#  Command [[dmesg]] :

***

## About:

### - show latest core events

***


## Use Cases:

### - use dmesg
```sh
[bohdan@fedora ~]$ dmesg
[    0.000000] Linux version 5.19.12-200.fc36.x86_64 (mockbuild@bkernel02.iad2.fedoraproject.org) (gcc (GCC) 12.2.1 20220819 (Red Hat 12.2.1-2), GNU ld version 2.37-36.fc36) #1 SMP PREEMPT_DYNAMIC Wed Sep 28 17:11:05 UTC 2022
[    0.000000] Command line: BOOT_IMAGE=(hd0,gpt6)/vmlinuz-5.19.12-200.fc36.x86_64 root=UUID=0a3c4880-65e3-4d48-b997-b5cfdaf2dafe ro rootflags=subvol=@ resume=UUID=7531c219-ce97-4746-89b2-1c09ca0c3ab6 rhgb quiet
[    0.000000] x86/fpu: Supporting XSAVE feature 0x001: 'x87 floating point registers'
[    0.000000] x86/fpu: Supporting XSAVE feature 0x002: 'SSE registers'
[    0.000000] x86/fpu: Supporting XSAVE feature 0x004: 'AVX registers'
[    0.000000] x86/fpu: xstate_offset[2]:  576, xstate_sizes[2]:  256
[    0.000000] x86/fpu: Enabled xstate features 0x7, context size is 832 bytes, using 'compacted' format.
[    0.000000] signal: max sigframe size: 1776
[    0.000000] BIOS-provided physical RAM map:
[    0.000000] BIOS-e820: [mem 0x0000000000000000-0x000000000009efff] usable
[    0.000000] BIOS-e820: [mem 0x000000000009f000-0x00000000000bffff] reserved
[    0.000000] BIOS-e820: [mem 0x0000000000100000-0x0000000009afffff] usable
[    0.000000] BIOS-e820: [mem 0x0000000009b00000-0x0000000009dfffff] reserved

```

### - use to 
```sh

```


## Keys:
```sh
Options:
 -C, --clear                 clear the kernel ring buffer
 -c, --read-clear            read and clear all messages
 -D, --console-off           disable printing messages to console
 -E, --console-on            enable printing messages to console
 -F, --file <file>           use the file instead of the kernel log buffer
 -f, --facility <list>       restrict output to defined facilities
 -H, --human                 human readable output
 -J, --json                  use JSON output format
 -k, --kernel                display kernel messages
 -L, --color[=<when>]        colorize messages (auto, always or never)
                               colors are enabled by default
 -l, --level <list>          restrict output to defined levels
 -n, --console-level <level> set level of messages printed to console
 -P, --nopager               do not pipe output into a pager
 -p, --force-prefix          force timestamp output on each line of multi-line messages
 -r, --raw                   print the raw message buffer
     --noescape              don't escape unprintable character
 -S, --syslog                force to use syslog(2) rather than /dev/kmsg
 -s, --buffer-size <size>    buffer size to query the kernel ring buffer
 -u, --userspace             display userspace messages
 -w, --follow                wait for new messages
 -W, --follow-new            wait and print only new messages
 -x, --decode                decode facility and level to readable string
 -d, --show-delta            show time delta between printed messages
 -e, --reltime               show local time and time delta in readable format
 -T, --ctime                 show human-readable timestamp (may be inaccurate!)
 -t, --notime                don't show any timestamp with messages
     --time-format <format>  show timestamp using the given format:
                               [delta|reltime|ctime|notime|iso]
Suspending/resume will make ctime and iso timestamps inaccurate.
     --since <time>          display the lines since the specified time
     --until <time>          display the lines until the specified time

 -h, --help                  display this help
 -V, --version               display version

Supported log facilities:
    kern - kernel messages
    user - random user-level messages
    mail - mail system
  daemon - system daemons
    auth - security/authorization messages
  syslog - messages generated internally by syslogd
     lpr - line printer subsystem
    news - network news subsystem

Supported log levels (priorities):
   emerg - system is unusable
   alert - action must be taken immediately
    crit - critical conditions
     err - error conditions
    warn - warning conditions
  notice - normal but significant condition
    info - informational
   debug - debug-level messages

```

### --help
```sh
Usage:
 dmesg [options]

```

***

## [[Boot]]

***
