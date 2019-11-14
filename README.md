# OpenAppFilter功能简介

OpenAppFilter模块采用layer 7深度识别技术，实现对单个app进行管控的功能

该模块支持主流linux版本，目前主要在OpenWrt各版本中测试，支持OpenWrt 15.05、OpenWrt 18.06、

OpenWrt 19.07、 LEDE等主流版本

## 主要使用场景
	- 家长对小孩上网行为进行管控，限制小孩玩游戏等
	- 限制员工使用某些app， 如视频、招聘、购物等
	
## 支持app列表(只列主流)
 - 游戏
   王者荣耀 英雄联盟 欢乐斗地主 梦幻西游 明日之后 ...
 - 音乐
 - 购物
   淘宝 京东 唯品会 拼多多 苏宁易购
 - 聊天
	QQ 微信 钉钉 
 - 招聘
 - 视频
   抖音小视频 斗鱼直播 腾讯视频 爱奇艺 火山小视频 YY 微视 虎牙直播 快手 小红书 ...

# 使用说明
## 编译说明
- 将该项目clone到openwrt package目录
- make menuconfig 在luci app中选上 luci oaf模块，保存
- 编译生成OpenWrt固件升级， 如果出现页面没有app的情况，保存并应用初始化

## 模块使用限制
- 必须关闭各种加速模块，如软加速、硬加速等
- 模块可能与qos等用到了netfilter mark字段的模块冲突， 自行检查
- 该模块只工作在路由模式， 交换机(桥)模式不会生效


# 技术支持

- 微信公众号: OpenWrt

- 技术交流QQ群: 943396288


forked from destan19/OpenAppFilter
