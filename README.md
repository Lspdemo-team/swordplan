# swordplan

执剑计划：将设备交给云端决定设备恢复出厂，适用设备被技术人员分析时及时恢复出厂销毁证据

在新版本中 执剑计划为可选第三方服务器地址

method:POST

参数
|params|type|note
|--|--|--|
|mac|string|设备mac地址(获取不到将返回androidid)
|sn|string|设备sn,仅限Lenovo android10可获取|
|ver|string|设备版本
|device|string|设备型号信息
|romver|string|rom版本
|pkgname|string|app包名
|system|string|系统信息(api level+系统指纹)
|currmdm|int|当前mdm,-1为未找到,2(CSDK),3(Mia)
|currstate|string|当前设备管理状态(deviceadmin/owner/Not Activited)
|lcmdm_version|string|launcher3 mdm版本|

返回

仅接受一个数字

**1**为恢复出厂

**0**为不恢复出厂
