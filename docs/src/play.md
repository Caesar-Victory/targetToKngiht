### Apple相关
1. 将区域改为美国，或者将语言改为英语,会导致手机重置后无法从iCloud恢复交通卡以及银行卡(CN).
2. Apple Watch大多数情况下可以自动识别运动模式并且在运动暂停时，提示是否记录
### 翻墙折腾
1. 失败的经历：在闲鱼购买京东亚瑟云AX1800，两次出现重置之后192.168.0.1拒绝连接的情况，放弃折腾路由器翻墙
2. v2Rayn启动时报错：
```markdown
failed to listen TCP on 0.0.0.0:10820 > listen tcp 0.0.0.0:10820: bind: An attempt was made to access a socket in a way forbidden by its access permissions.
1. 可以命令行 netstat -ano | findstr :10820 检查端口是否被占用，若被占用可以在客户端中更换端口号，也可以在安装路径：binConfigs下修改config.json文件
2. 找到 v2RayN.exe，右键以管理员方式运行
3. 删除本地文件，全新安装低版本
4. 重启电脑（有效）
```
3. v2RayN没有任何替代品，其他产品都停止维护。
4. 对网络文件夹的访问记录，除了查看注册表，没有其他办法可以获取到。命令行或者在资源管理器查看最近访问，都是乱序的
5. Apple Watch 圆环不与手机同步，解决方法：取消 Watch 与 iPhone的配对
6. 删除PC的 Office 授权证书：https://sway.cloud.microsoft/1Gw2W5lJCYCP0oQY?ref=Link
7. 删除浏览器已经被组织接管的提示信息
```Powershell
reg delete "HKCU\Software\Microsoft\Windows\CurrentVersion\Policies" /f
reg delete "HKCU\Software\Microsoft\WindowsSelfHost" /f
reg delete "HKCU\Software\Policies" /f
reg delete "HKLM\Software\Microsoft\Policies" /f
reg delete "HKLM\Software\Microsoft\Windows\CurrentVersion\Policies" /f
reg delete "HKLM\Software\Microsoft\Windows\CurrentVersion\WindowsStore\WindowsUpdate" /f
reg delete "HKLM\Software\Microsoft\WindowsSelfHost" /f
reg delete "HKLM\Software\Policies" /f
reg delete "HKLM\Software\WOW6432Node\Microsoft\Policies" /f
reg delete "HKLM\Software\WOW6432Node\Microsoft\Windows\CurrentVersion\Policies" /f
reg delete "HKLM\Software\WOW6432Node\Microsoft\Windows\CurrentVersion\WindowsStore\WindowsUpdate" /f
```
8. Edge 浏览器AI主题生成的URL: https://www.microsoft.com/en-us/edge/create-a-theme?form=MT00OT&cs=357927189
9. 以命令行的方式，通过记事本打开相关文件，查看所有历史命令 `notepad (Get-PSReadLineOption).HistorySavePath`
10. 通过简洁的Powershell命令打印当前工作路径下所有文件夹名称 ```Get-ChildItem -Directory -Name```，此举主要是方便提交产品编号信息
11. iPhone在拨号键盘输入*3001#12345#*，然后拨打，可以快速查看参考信号接受功率，信噪比
12. VMWare虚拟网卡会导致进入路由器后台192.168.1.1被错误定向到虚拟网卡【一般考虑影响DNS的因素】，因此需要禁用该网卡，才能正确访问路由器后台
```Powershell
### 该命令运行后可以看到网口是VMware，因此开始怀疑虚拟网卡
Test-NetConnection -ComputerName 192.168.1.1 -Port 80
WARNING: TCP connect to (192.168.1.1 : 80) failed

ComputerName           : 192.168.1.1
RemoteAddress          : 192.168.1.1
RemotePort             : 80
InterfaceAlias         : VMware Network Adapter VMnet8
SourceAddress          : 192.168.1.1
PingSucceeded          : True
PingReplyDetails (RTT) : 0 ms
TcpTestSucceeded       : False
```
13. 查看修改注册表以支持DoH是否成功`Get-ItemProperty -Path "HKLM:\SYSTEM\CurrentControlSet\Services\Dnscache\Parameters" -Name "EnableAutoDoh"`
14. 预期返回结果 `EnableAutoDoh : 2`
15. iPhone不能设置消息置顶，但是Apple Wath收到消息回复时，有置顶消息的选项
16. 打开注册表，路径为：`计算机\HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced`新建项目:ShowSecondsInSystemClock,值的类型为:DWORD（32位）值,将其值修改为1
17. 早起打开电脑存在：在音频输出设备中切换时，会有短暂发生，但是切换之后就没有声音了。有以下解决步骤
    1. 关闭音频增强和空间音效
    2. 重装驱动
    3. 有异常现象：音频处理对象中每组音频效果，其中Elevoc有四组，Realtek有两组（目前正常情况是分别减半）
    4. 卸载声音，视频和游戏控制器分组下的所有驱动
    5. 重装驱动和重启设备

18. 独显电脑也要记得更新核心显卡，不然那天切换到核心显卡的时候，发现核显显卡驱动版本太低，又需要重新下载一次驱动，这种维护工作应该放在平时
19. placeholder.
20. 在Windows11电脑上，安装了8.0.42版本的MySQL Community Server。平时在PowerShell 
