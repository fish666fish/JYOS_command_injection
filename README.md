# JYOS_command_injection
JOYS is an operating system for thin client made by [Shenzhen Jieyun zhilian Technology Co., Ltd](https://jieyunzl.com/index.php?lang=en). During the boot procedure, the user can set some settings and take dianosis.
<img width="1320" alt="booting interface" src="https://github.com/fish666fish/JYOS_command_injection/assets/88928923/11f3077b-7cf2-4dc0-a52e-8ba493b94042">
However, there is inappropriate sanitization of the user input, leading to arbitrary command execution with root permission. This can be achieved quite simply by using a semicolon before the command. E.g., `; whoami`
<img width="1090" alt="PoC" src="https://github.com/fish666fish/JYOS_command_injection/assets/88928923/63d2c549-8371-4abe-988f-e68aaadd4dfe">
This vulnerability was tested on up-to-date JYOS, and it is platform-agnostic. Both ARM and x86_64 distributions were affected.
