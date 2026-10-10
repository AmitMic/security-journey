# Virtualisation Basics

## Main idea
Virtualisation lets one physical computer be split into several isolated
virtual computers that share its hardware (CPU, RAM, storage).

## Key concepts
- **Hypervisor:** software that creates and manages virtual machines.
  - *Type 1* runs directly on hardware.
  - *Type 2* runs on top of an operating system (e.g. VirtualBox).
- **Virtual machine (VM):** a complete computer simulated inside another
  computer, with its own OS and kernel.
- **Container:** a lightweight isolated environment that shares the host's
  kernel instead of running its own OS. It usually runs one application
  plus what that application needs.

## VM vs container
| | VM | Container |
|---|---|---|
| Kernel | Own kernel | Shares host kernel |
| Startup | Minutes | Seconds |
| Isolation | Stronger | Weaker |
| Size | Large (full OS) | Small |

## Why virtualisation is used
Instead of buying a separate physical machine for every server, you run
many VMs on one machine. The benefits that matter most:
- **Cost and resource usage:** one machine's hardware is shared efficiently.
- **Fast deployment and scalability:** a new VM can be created or cloned in
  minutes instead of buying and setting up hardware.
- **Portability:** a VM can be moved or backed up as a file.
(Others: flexibility, centralised management.)

## Relation to cyber security
- **Safe testing:** snapshots let me break things and revert, so I can
  practise attacks and analyse malware without risking my real system.
- **Isolation is a security boundary, but not a perfect one:** VM escapes
  exist, so analysis VMs should use restricted networking and no shared
  folders or clipboard.
- **Attack surface:** containers share a kernel, so a kernel flaw can
  affect every container on the host.

## Hands-on
**In the room:** I used a VM manager, created VMs, and monitored the
different machine states (list the states you saw here).

**Before the room:** I installed VirtualBox, set up Kali Linux, and
practised navigating the filesystem and using the terminal.
