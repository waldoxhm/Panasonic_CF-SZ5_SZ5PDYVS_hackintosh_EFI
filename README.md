![screenshot1](https://user-images.githubusercontent.com/4980738/132847673-d1db2b64-1376-4986-b399-bfe51c74e6ea.jpg)

# Panasonic_CF-SZ5_SZ5PDYVS_hackintosh_EFI
opencore 0.7.4 efi partition  
OSX Big sur 11.6

### update2021.10.13 （osx Big sur 11.6 with opencore 0.7.4 ）
 - fixed trackpad gesture 
 - upgrade opencore version to 0.7.4

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
 - Trachpad(touchpad and keyboard not waking after sleep due to Voodoops2.kext)

### Things to do
 - Replace #YOUR UUID# and #YOUR MB SERIAL# and #YOUR SERIAL NUMBER# in config.plist with a generator,such as hacintosh tool.  
 - [Optional but Recommanded] Unlock CFG-lock refer to https://dortania.github.io/OpenCore-Post-Install/misc/msr-lock.html#turning-off-cfg-lock-manually  
   1. In my case (BIOS Version SZ5_V300L15)CFG-lock address is 0xA0F, set it to 0x00.  
   2. Boot into modGRUBShell.efi.  
   3. <code>setup_var_3 0xA0F 0x00</code> (use mine with your own risk.I didn't test it in other environment, you'd prefer to do the whole thing in the link above.)  
   4. Reboot into ControlMsrE2.efi, check message, UNLOCKED means SUCCESS.  
   5. set "AppleCpuPmCfgLock","AppleXcpmCfgLock" to false in config.plist.  
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
# 松下_CF-SZ5_SZ5PDYVS_hackintosh_EFI
opencore 0.7.4 efi 分区文件
OSX Big sur 11.6

### 更新2021.10.13 （osx Big sur 11.6 with opencore 0.7.4 ）
 - 修复触摸板手势 
 - opencore版本升级至0.7.4

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
 - 触摸板(触摸板和键盘在睡眠之后无法正常使用，voodoops2.kext的问题)
 
 ### 完善
 - 替换config.plist里的 #YOUR UUID#、#YOUR MB SERIAL#、#YOUR SERIAL NUMBER#，找一个生成器，可以用hacintosh tool。
 - [可选，但是推荐]解锁 CFG-lock 参考https://dortania.github.io/OpenCore-Post-Install/misc/msr-lock.html#turning-off-cfg-lock-manually  
   1. 我的BIOS(BIOS版本 SZ5_V300L15)CFG-lock 地址是0xA0F，将其设为0x00。  
   2. 引导进入 modGRUBShell.efi。  
   3. <code>setup_var_3 0xA0F 0x00</code> (用我的CFG-lock变量地址有一定风险,没有在别的型号和bios版本机器上测试过，最好按照上面的教程链接自己做一遍。)  
   4. 引导进入ControlMsrE2.efi, 一串输出中显示UNLOCKED意味解锁成功。   
   5. 把config.plist中的"AppleCpuPmCfgLock"和"AppleXcpmCfgLock"设置为false。  
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

