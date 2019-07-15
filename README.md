# Livepatch overlay
Open standard for livepatch patches management for compatibility on different vendors.

## Why
We have differents livepatch services, each one with their own way of storing the livepatch patches.  
This repository is trying to fix this by creating a open standard for storing and sharing livepatch patches in a reusable way.
This can be optimized, giving the freedom to share and condivide livepatch patches repository with other users.

For discussion of the standard open [issues](https://github.com/elivepatch/livepatch-overlay/issues) on this repository.

## How
This open standard livepatch overlay can be used by [elivepatch-client](https://github.com/gentoo/elivepatch-client/) for producing livepatch objects.

## livepatch-overlay structure example:

```
livepatch_version: 0.1

- 4.18.1
      - patch_id: 1
        cve_id: CVE-2018-15572 
        commit_id: f8a0aeefc2f6e1bfd6653fcc30453ce7e582fac8
        repository: https://github.com/torvalds/linux
        comment: x86/speculation: Protect against userspace-userspace spectreRSB
      - patch_id: 2
        cve_id: CVE-2018-15594
        commit_id: b13b271933eea6161e741825487d6e73e800bedf 
        repository: https://github.com/torvalds/linux
        comment: x86/paravirt: Fix spectre-v2 mitigations for paravirt guests
      - patch_id: 3
        cve_id: CVE-2018-3620
        commit_id: abf914eefa19098727455f11acd895c57621a822
        repository: https://github.com/torvalds/linux
        comment: x86/microcode: Allow late microcode loading with SMT disabled
      - patch_id: 4
        path: patches/4.18.1/meminfo_allcaps_change.patch
        comment: Change VmallocChunk text to all caps
        license: GPLv2
- 4.18.2
      - patch_id: 5 
        cve_id: CVE-2018-9363
        commit_id: f47e3431b15ae9cae8acc0fdf20fc083422c9f61
        repository: https://github.com/torvalds/linux
        comment: Bluetooth: hidp: buffer overflow in hidp_process_report
```
## Contributors

See [brief biographies of the
contributors](CONTRIBUTORS.md)
to livepatch-overlay and [add
yourself](/../../edit/master/CONTRIBUTORS.md) if
you are a contributor.
