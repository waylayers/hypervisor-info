# Hypervisor cracks - best practices and release requirements

How to minimize risks while using hypervisor cracks and what hypervisor crack releases must or should fulfill to be allowed on this forum.

## Related topics

- **EDUCATION**: [Hypervisor cracks and Windows security - an introduction](./introduction.md) - Basics to help  you understand security implications so that you can decide if you want to use hypervisor cracks.
- **INFO**: (This topic) - How to use hypervisor cracks responsibly and quality requirements for approved crack releases.

## Best practices for using hypervisor cracks

Before disabling security features and running the crack:

- **Malware-free**: Check your system with one or multiple reputable, portable AV scanners, have a closer look at running processes in Task Manager, do not browse filesharing sites without a good ad blocker like uBlock Origin.
- **Trusted source**: Verify that all files included with the crack and all files for the game in question are clean and come from a trusted source,
- **File verification**: Verify file checksums that you obtained from a different, trusted source, if available.
- **The power of open source**: Even better than checksums - compile the included source code yourself, if you know how to. Compare the source code with the original projects on Github that the crack hypervisors are based on to review the differences.
- **Reviewed and approved methods only**: For disabling virtualized security and the Windows hypervisor, use open source scripts from approved releases posted to this forum.
- **Networking**: Disconnect the PC from all networks, preferably outside of the OS, e.g. by unplugging the cable.
- **Minimize exposure**: __**IMPORTANT**__. Revert the changes to Windows security and reboot your PC after you are done playing the game.
- **Stay skeptical**: Prefer crack releases that do not instruct you to run closed source binaries with admin privileges.

Advanced users may want to consider running hypervisor cracks in a virtual machine (that supports nested virtualization) with GPU passthrough, such as KVM on Linux or Hyper-V, or a dedicated computer without personal data on it. This has a performance penalty though.

## Requirements for hypervisor crack releases on this forum

### Mandatory requirements:

- **Release posts**:
  - Must link to this post and to [Hypervisor cracks and Windows security - an introduction](./introduction.md),
  - must link to the support topic and emphasize that all questions go there,
  - must clearly state that the release is experimental, if there are any stability issues, especially BSODs.
- **Documentation**:
  - Must be consistent with the information in these posts,
  - must emphasize that Windows security changes should be reverted immediately after playing,
  - must not instruct to disable more security than absolutely necessary,
  - must explain all system changes that are not addressed in this post or the introductory post linked above,
  - must recommend disabling DSE via the advanced boot menu option (over experimental malware-style runtime patching via vulnerable signed drivers),
  - must warn Bitlocker users to make sure they have their recovery key ready,
  - must warn Windows Hello users to make sure they know their normal login password.
- **Tools for disabling Windows security**:
  - Must be consistent with included documentation and guides on this forum,
  - must be open source, with appropriate comments, warnings and readable code,
  - must follow the minimal method established by the introductory post linked above,
  - must prevent Hyper-V from loading the Windows hypervisor with the "hypervisorlaunchtype off" boot option,  instead of removing Hyper-V,
  - must use the advanced boot menu option for disabling DSE by default,
  - must gracefully handle all possible system configurations or abort when unsupported configurations are detected,
  - must not make any system changes that are not required,
  - must ensure that all changes to the system are easily reversible,
  - must be reviewed and approved by a staff member.
- **Hypervisor drivers**:
  - Must include source code (and build scripts or project files that are necessary for compilation) or link to code repository.
- **Closed-source binaries**:
  - Must not require to be run as administrator.


### Optional, recommended properties that may become mandatory in the future:

- **Secure implementation**: Interfaces between privileged and unprivileged components of the crack solution should have input sanitization with a documented thought process.
- **Reproducible**: when compiling from source, users should be able to reproduce binaries that are byte-identical to the included. precompiled binaries.

We may also allow open source solutions for the runtime patching method for DSE in releases, if stable methods emerge. We encourage open development and discussion on this in our Developer section.

---

Written by ResourcectoR in cs.rin.ru