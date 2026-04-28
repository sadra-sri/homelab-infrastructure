```text
                [ VMware Workstation (Host) ]
                         │
         ┌───────────────┴───────────────┐
         │                               │
         │                               │
 ┌─────────────────────┐        ┌────────────────────────┐
 │        ESXi         │        │   External Client VM   │
 │ (Nested Hypervisor) │        │   (Windows 10)         │
 └─────────┬───────────┘        └───────────┬────────────┘
           │                                │
           │        VMnet3 (Host-only Network)
           └───────────────┬────────────────┘
                           │
                ┌──────────┴──────────┐
                │                     │
        ┌──────────────┐     ┌──────────────┐
        │ Domain Ctrl  │     │  Client VM   │
        │ (AD, DNS,    │     │ (Windows 10) │
        │  DHCP)       │     │              │
        └──────────────┘     └──────────────┘
```

## Architecture Overview

The lab is built using a nested virtualization setup where ESXi is installed inside VMware Workstation.

The Domain Controller and one client run inside ESXi, while another client runs externally on VMware Workstation.

All systems are connected through a Host-only network (VMnet3), ensuring an isolated environment and preventing external DHCP interference.
