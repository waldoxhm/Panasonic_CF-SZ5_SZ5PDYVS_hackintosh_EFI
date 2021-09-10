# Panasonic_CF-SZ5_SZ5PDYVS_hacintosh_EFI
opencore 0.7.2 efi partition  
OSX Big sur 11.5.2
### System configuration 
 - CPU: Intel Core i5-6300U
 - Graphic: Intel HD520
 - WiFi&BT: Intel AC8260
 - Audio: Realtek ALC256
 - Ethernet: Intel I219-LM 
 - Card Reader: O2 micro SD/MMC

### What's working
 - IGPU
 - Audio
 - Ethernet
 - SD card reader
 - Original WIFI module(use heliport to connect wifi)
 - BLUETOOTH(BT4.x device failed to connect)
 - Native Power Management （patched）
 - Sleep(DSDT 0x6D patched)
 - HDMI + Audio
 - Brightness control
 - Keybroad(function hotkey mismatch)
 - Trachpad(act as a PS/2 compatiable mouse, system geature buged, SMBUS loaded ,but VRMI can't recognize it,"SYN0502"in ACPI.)

### Things to do
 - Replace #YOUR UUID# and #YOUR MB SERIAL# and #YOUR SERIAL NUMBER# in config.plist with a generator,such as hacintosh tool.
 - [Optional but Recommanded] Unlock CFG-lock refer to https://dortania.github.io/OpenCore-Post-Install/misc/msr-lock.html#turning-off-cfg-lock-manually
   In my case (BIOS Version SZ5_V300L15)CFG-lock address is 0xA0F, set it to 0x00.
   Boot into modGRUBShell.efi.
   setup_var_3 0xA0F 0x00 (use mine with your own risk.I didn't test it in other environment, you'd prefer to do the whole thing in the link above.)
   check message in ControlMsrE2.efi, UNLOCKED means SUCCESS.
   you can set "AppleCpuPmCfgLock","AppleXcpmCfgLock" to false in config.plist.
 - Download Heliport and install. https://github.com/OpenIntelWireless/HeliPort/releases
 
### Credits & Sources (in no particular order and maybe missing some)
 - Apple INC.
 - https://github.com/acidanthera
 - https://github.com/RehabMan
 - https://github.com/VoodooSMBus
 - https://github.com/corpnewt
 - https://www.insanelymac.com/
 - https://www.tonymacx86.com/
 - https://dortania.github.io/vanilla-laptop-guide/
 - https://blog.daliansky.net/
 - https://blog.xjn819.com/
 - https://github.com/OpenIntelWireless

 
——————————————————————————————————————————————————
# 松下_CF-SZ5_SZ5PDYVS_hacintosh_EFI
opencore 0.7.2 efi 分区文件
OSX Big sur 11.5.2

### 系统配置
 - 中央处理器: Intel Core i5-6300U
 - 显卡: Intel HD520
 - 无线网卡及蓝牙: Intel AC8260
 - 声卡: Realtek ALC256
 - 网卡: Intel I219-LM 
 - 读卡器: O2 micro SD/MMC

### 正常工作
 - 显卡
 - 声卡
 - 网卡
 - 读卡器
 - 原生网卡(使用heliport联网)
 - 蓝牙(蓝牙4.x的设备不能连接)
 - 原生电源管理（补丁）
 - 睡眠(DSDT 0x6D 补丁)
 - HDMI及声音
 - 背光控制
 - 键盘(功能热键不对应)
 - 触摸板(只能识别成PS/2鼠标,系统手势用不了, SMBUS能正确加载,但是VRMI认不出来触摸板,ACPI中触摸板是"SYN0502".)
 
 ### 完善
 - 替换config.plist里的 #YOUR UUID#、#YOUR MB SERIAL#、#YOUR SERIAL NUMBER#，找一个生成器，可以用hacintosh tool。
 - [可选，但是推荐]解锁 CFG-lock 参考https://dortania.github.io/OpenCore-Post-Install/misc/msr-lock.html#turning-off-cfg-lock-manually
   我的BIOS(BIOS版本 SZ5_V300L15)CFG-lock 地址是0xA0F，将其设为0x00。
   引导进入 modGRUBShell.efi。
   setup_var_3 0xA0F 0x00 (用我的CFG-lock变量地址有一定风险,没有在别的型号和bios版本机器上测试过，最好按照上面的教程链接自己做一遍。)
   引导进入ControlMsrE2.efi, 显示UNLOCKED意味解锁成功。 
   可以吧config.plist中的"AppleCpuPmCfgLock"和"AppleXcpmCfgLock"设置为false。
 - 下载 Heliport 并安装。 https://github.com/OpenIntelWireless/HeliPort/releases

### 感谢及出处 (没有特定顺序，并且可能遗漏)
 - 美国苹果电脑公司
 - https://github.com/acidanthera
 - https://github.com/RehabMan
 - https://github.com/VoodooSMBus
 - https://github.com/corpnewt
 - https://www.insanelymac.com/
 - https://www.tonymacx86.com/
 - https://dortania.github.io/vanilla-laptop-guide/
 - https://blog.daliansky.net/
 - https://blog.xjn819.com/
 - https://github.com/OpenIntelWireless
