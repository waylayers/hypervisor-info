# Frequently asked questions

**Q: Where do I get hypervisor cracks?**
A: Releases are posted to game topics on this forum by the creators.

**Q: Can I use files from a hypervisor crack release for a different game?**
A: In general, no. Almost all components of the release, including the hypervisor drivers, may have game-specific code. Please wait for updates for the crack package that is meant for your game. The only exception is VBS.cmd, which is universal.

**Q: Can I use files from a hypervisor crack release for a different version of  the game?**
A: No, it must be exactly the same version that the release is meant for, otherwise the included Denuvo token will not be valid.

**Q: Is there Linux support?**
A: No, the SimpleSvm and HyperDbg projects that the hypervisors are based on are Windows-only. In theory, it might be possible to build a similar solution with KVM on Linux, but I don't think it's likely someone skilled enough will create anything like this for Linux from scratch.

**Q: After playing a hypervisor game, anti-cheat software stopped working, why?**
A: Most likely you did not revert the Windows security changes to your system properly or used an older HV crack release. You need to ensure that driver signature enforcement is on, meaning that testsigning is not configured and Windows was rebooted without special options and without Efiguard. You also cannot be using any DSE patchers. **Kernel-level anti-cheat solutions may ban you, if they detect (attempts or indicators of) kernel-level modifications, because sophisticated cheats also operate on kernel level.**