
# 测试用例

## 1. 固件升级测试
### 1.1 测试方法
- 使用恢复工具更新到V1.0.1。
- OTA 升级到当前版本。
- 使用恢复工具更新到K-TOUCH 最新版本
- OTA 升级到当前版本。

### 1.2 期望结果
- 可正常升级到当前版本。 

---

## 2. U盘识别
### 2.1 测试方法
格式化时选择不同的扇区大小，容量为4G-8G大小

| 类型           | 扇区大小(KB)                |
|----------------|----------------------------|
| U盘            | 512        |
| U盘            | 4096       |
| U盘            | 8192       |
| 读卡器+sd卡     | 512        |
| 读卡器+sd卡     | 4096       |
| 读卡器+sd卡     | 8192       |

### 2.2 期望结果
- 不同扇区大小格式化后每种类型都可以正常识别。

---

## 3. OTA页面连接不同的WIFI
<img src=/Images/ota_img_remind.png width="600"/>


### 3.1 测试方法
- 更新旧版本的.img文件，让Panda Touch提示OTA，如果更新固件后直接提示了这个页面，就不需要使用旧版本.img文件
- 点击右侧wifi列表选择一个不同的wifi进行连接
- 根据提示更新最新的.img文件

### 3.2 期望结果
- 可以连接到不同的wifi
- 可以更新.img文件
---

## 4.切换语言
<img src=/Images/language_custom.png width="600"/>

### 4.1 测试方法
- 更新一个非英文版本的.img文件
- 选择语言为 '自定义'
- 屏幕上的文本显示为对应语言包的文本
- 选择语言为 'English' ,再次切换回 'English' 版本

### 4.2 期望结果
- 切换语言后，屏幕上的文本可以正常显示

---

## 5. 扫描打印机
### 5.1 测试方法
<img src=/Images/guide_printer.png width="600"/>

- 确保WIFI已连接上并且与打印机处于同一个局域网
- 点击扫描后，再次点击重新扫描
- 连续测试3次

### 5.2 期望结果
- 每次都可以正常扫描到打印机

---

## 6. Panda PWR使能开关
<img src=/Images/hide_pwr.png width="600"/>

### 6.1 测试方法
设置页面的Panda PWR开关切换为开启
设置页面的Panda PWR开关切换为关闭

### 6.2 期望结果
- 可以显示和隐藏Panda PWR功能

---

## 7. 休眠时间
### 7.1 测试方法
- 设置不同的休眠时间，记录测试结果

| 时间           | 实测                                 |
|----------------|--------------------------------------|
| 2分钟          |2分钟后，看屏幕是否熄灭，再次点击屏幕     |
| 60分钟         |60分钟后，看屏幕是否熄灭，再次点击屏幕    |
| 始终开启       |60分钟后，看屏幕是否熄灭，再次点击屏幕    | 

### 7.2 期望结果
- 对比实测结果

| 时间           | 结果                          |
|----------------|---------------------------------|
| 2分钟          |2分钟后屏幕熄灭，再次点击会点亮     |
| 60分钟         |60分钟后屏幕熄灭，再次点击会点亮    |
| 始终开启       |60分钟或者更长时间后屏幕仍然不会熄灭 | 

## 8. 亮度调节
### 8.1 测试方法
- 将背光调节到10%左右 重启
- 将背光调节到50%左右 重启
- 将背光调节到100% 重启

### 8.2 期望结果
- Panda Touch可正常重启，并且保持上一次背光亮度

## 9. 多台加热延迟
<img src=/Images/group_delay.png width="600"/>

### 9.1 测试方法
- 添加至少2台打印机
- 设置不同的时间，记录测试结果
 
假设添加了三台打印机
| 时间           | 结果                            |
|----------------|--------------------------------------------------|
| 1分钟          |第一台打印机开始加热 1分钟后， 第二台打印机开始加热 ，1分钟后， 第三台打印机开始加热 |
| 2分钟          |第一台打印机开始加热 2分钟后， 第二台打印机开始加热 ，2分钟后， 第三台打印机开始加热 | 

### 9.2 期望结果
- 延时时间与设置的相符合

## 10. 打印机-默认文件夹
<img src=/Images/cache_root.png width="600"/>

### 10.1 测试方法
- 在设置页面，切换默认文件夹为Cache
- 切换到Panda Touch的打印机文件列表面板
- 在设置页面，切换默认文件夹为CacheRoot
- 切换到Panda Touch的打印机文件列表面板

### 10.2 期望结果
- 可显示对应文件夹的文件列表

## 11. 恢复出厂设置
### 11.1 测试方法
- 安装非英文版本的语言包 
- 点击恢复出厂设置

### 11.2 期望结果
- Panda Touch可正常恢复出厂设置

## 12. 账号
<img src=/Images/input_account.png width="600"/>

### 12.1 测试方法
- 点击登录拓竹账号 
- 输入验证码
- 同步打印机
- 删除账号

### 12.2 期望结果
- 可正常登录账号、同步打印机、并删除账号

## 13. 温度轴控制
### 13.1 测试方法
- 设置喷嘴温度 
- 设置热床温度
- 控制x、y、z轴、挤出机
- 切换不同速度，在APP上查看是否成功 

### 13.2 期望结果
- 所有控制都能正常响应

## 14. 耗材
<img src=/Images/filament_screen.png width="600"/>

### 14.1 测试方法
- 外挂料盘的加载和卸载 
- AMS的槽位选择 

### 14.2 期望结果
- 外挂料盘和AMS都可以正常加载和卸载耗材

## 15. 文件列表
### 15.1 测试方法
- SD卡文件列表 
- U盘文件列表 
- 历史记录文件列表

### 15.2 期望结果
- 可以正常显示文件列表

## 16. 可正常添加打印机
### 16.1 测试方法
- 在打印机页面，点击右下角按钮"+" 
- 选择添加打印机 
- 扫描打印机
- 输入访问码
- 选择添加组
- 勾选你对应打印机
<img src=/Images/group_choose_printer.png width="600"/>

- 控制组内打印机的轴移动或者灯泡亮灭

### 16.2 期望结果
- 可正常添加打印机和打印机组
- 可控制组内所有打印机

## 17. 打印机的编辑和删除
<img src=/Images/edit.png width="600"/>

### 17.1 测试方法
- 编辑打印机的名称、IP、访问码、SN号、型号等参数
- 删除打印机  

### 17.2 期望结果
- 可正常编辑打印机参数
- 可正常删除打印机

## 18. 主页面参数
<img src=/Images/thumbnail_preview.png width="600"/>

### 18.1 测试方法
- 查看喷嘴温度、热床温度、灯状态、打印进度是否正确
- 点击对应按钮进行跳转 
- 在Panda Touch主页点击 '重新打印'

### 18.2 期望结果
- 主页显示的数值与app上显示的相同
- 可正常跳转相应页面
- 可在Panda Touch主页发起重新打印

## 19. 发起打印
### 19.1 测试方法
- 使用AMS，在打印机的SD卡面板发起打印任务，选择A1-A4，发起打印，每个槽位都测试一遍
- 使用AMS，在U盘面板发起打印任务，选择A1-A4，发起打印，每个槽位都测试一遍
- 在打印历史发起打印任务
- 使用AMS，在Panda Touch主页发起重新打印，如果重新打印按钮为绿色时，选择A1-A4，发起打印，每个槽位都测试一遍

### 19.2 期望结果
- 使用AMS时，可正常设置每隔槽位
- 不使用AMS，可正常发起打印 

## 20. 文件排序
### 20.1 测试方法
- 打开SD卡面板，不使用缩略图模式，可以按照时间和名称排序 
- 打开U盘面板，不使用缩略图模式，可以按照时间和名称排序 

### 20.2 期望结果
- 可正常排序

## 21. 电池电量显示
### 21.1 测试方法
- 切换供电模式为DC5V
- 切换供电模式为电池

### 21.2 期望结果
- DC5V时，电池图标为循环充电动画
- 电池模式时，电池图标显示对应级别
    * 0-30 显示为1格
    * 31-50 显示为2格
    * 51-100 显示为3格