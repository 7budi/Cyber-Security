At first our access to a remote server is usually in the context of low-privileged user.
so to gain a full access to the server we need to find an internal /local vulnerability that would escalate our privilege to the root user on linux or the administrator/system in windows.

# PrivEsc Checklists
once we gain initial access to a box, we want to thoroughly enumerate he box to find any potential vulnerabilities we can exploit to achieve higher privilege level.

We can find many checklists and cheat sheets online that have a collection of checks we can run and the commands to run these checks. One excellent resource is [HackTricks](https://book.hacktricks.xyz), which has an excellent checklist for both [Linux](https://book.hacktricks.xyz/linux-unix/linux-privilege-escalation-checklist) and [Windows](https://book.hacktricks.xyz/windows/checklist-windows-privilege-escalation) local privilege escalation.

# Enumeration Scripts
We can run many scripts to automatically enumerate the server by running common commands that return any interesting findings. Some of the common Linux enumeration scripts include [LinEnum](https://github.com/rebootuser/LinEnum.git) and [linuxprivchecker](https://github.com/sleventyeleven/linuxprivchecker), and for Windows include [Seatbelt](https://github.com/GhostPack/Seatbelt) and [JAWS](https://github.com/411Hall/JAWS).