# taobao_taojinbi
本项目主要用于自动执行淘金币活动

**后续代码持续更新，力争完成淘金币全任务，你的☆就是我的动力**

# 测试环境
华为P30Pro + [autojs4.1.1](https://share.weiyun.com/owu3tBNr) + [淘宝v9.16.0](https://www.wandoujia.com/apps/32267/history)
(*华为P30Pro屏幕大小为1080x2340,此分辨率对特殊任务支持最佳*)

# 脚本功能列表
 - 自动执行淘金币所有浏览任务
 - 自动执行[逛好店领一大波金币]任务 (包含浏览10s+10金币任务/收藏店铺+10金币)
 - 自动执行[逛蚂蚁庄园喂小鸡]任务
 - 自动执行[签到领取话费充值金]任务
 - 自动执行[淘宝成就签到任务]
 - 自动执行[淘宝人生逛街领能量]掷色子任务 (需截图权限)
 - 自动执行[逛农场领免费水果]任务 (需截图权限)
 - 自动执行[蚂蚁森林]任务,收取好友能量 (需截图权限)
 - 自动执行[活力中心]任务,自动点击训练
 - 自动执行[淘宝通知权限任务]任务,自动点击训练（在华为机上测试通过）
 - 浏览任务完成立即返回，**无需额外等待**
 
# 更新日志

**v1.3.4** 2020年12月22日19:46:20
1. 淘金币新增[淘宝通知权限任务],开启后会再执行关闭 (默认在通知关闭下才有该任务,在华为机上测试通过)。**至此淘宝币全任务在P30Pro上测试通过**，当然不包含特定时间刷的任务和下单任务
2. 个人精力有限，今后只重点维护淘金币任务，因而把活力中心代码分离出来(huoli.js)

**v1.3.3** 2020年12月21日19:50:31
1. 用户可在文件开头中定义，需跳过不执行的简单浏览任务主题关键字
2. 用户可在文件开头中定义[去天猫APP领红包任务]是否执行
3. 解决活力中心[1000步换红包任务]执行失败问题
4. 发布[淘金币v1.3.3]apk版

**v1.3.2** 2020年12月20日11:44:35
1. 修复淘金币在任务列表中继续返回导致任务结束问题,
2. 淘宝人生掷色子任务中，添加了自动领取包裹和奖励，解决任务卡住问题

**v1.3.1** 2020年12月19日13:18:57
1. 淘金币任务列表新增[100淘金币夺宝任务]
2. 解决活力中心训练时无法单击关闭按钮问题

**v1.3.0** 2020年12月18日19:56:49
1. 应网友请求，附加**活力中心任务**(包括自动浏览任务和自动点击训练按钮),默认在淘金币完成后执行，若只执行活力中心任务,可在main函数注释掉taojinbi_task()这行
2. 整合特殊任务[逛直播间任务]到简单浏览任务中

**v1.2.3** 2020年12月17日20:50:41
1. 消消乐和蚂蚁森林任务中暂时隐藏终端,对应任务结束后再显示 (不隐藏可能收取不到全部能量)
2. 发布[淘金币v1.2.3]apk版


**v1.2.2** 2020年12月16日19:36:39
1. 新增蚂蚁森林任务，支持自定义'找能量'收取好友能量的次数
2. 解决'天猫领红包任务'，取消了'继续逛逛'按钮问题

**v1.2.1** 2020年12月14日19:57:06
1. 新增消消乐任务，需截图权限，目前在测试P30Pro上测试通过
2. 考虑到不同的机型，某些需截图权限的特殊任务可能会不兼容，启动时添加了可选的额外执行的任务： ['淘宝人生掷色子任务', '逛农场领免费水果任务', '消消乐任务']
3. 添加了APK发布版，用户可直接运行

**v1.2.0** 2020年12月13日20:52:53
1. 简化代码删减了双12的部分
2. 对需要截图功能的[淘宝人生逛街领能量]和[逛农场领免费水果] 设置了是否执行的全局变量，用户可选择是否执行该任务
3. 任务执行等待时间设置为全局变量，默认为15秒

**v1.1.4** 2020年12月12日21:04:28
1. 修复淘金币看直播任务，有时不能返回问题

**v1.1.3** 2020年12月11日20:13:13
1. 修复天猫app没安装，等待过长问题
2. 修复特殊任务后，新出简单浏览任务遗漏问题
3. 无法修复'双12红包兑现红包太少问题'

**v1.1.2** 2020年12月10日20:38:12
1. 解决淘金币执行过程中会返回到主页面问题(本质是按钮单击没有生效)
2. 把淘宝人生、逛好店任务、喂小鸡任务、逛直播间任务添加到特殊任务中
3. 解决芭芭农场双12任务后，淘金币没有肥料问题

**v1.1.1** 2020年12月9日19:36:44
1. 修复逛新加任务不能获取问题 
3. 某些任务(拍照识图)只在最新版淘宝中才存在,当前淘宝已换成最新版v9.16.0,经测试金币还是同样的奖励

**v1.1.0** 2020年12月8日19:51:51
1. 代码基本重构，为适应不同机型，添加了截图查找功能(**需授予截图权限**)
2. 添加任务运行选择功能，可单独执行任务

# 使用说明
## Auto.js中运行
1. 下载 [autojs4.1.1](https://share.weiyun.com/owu3tBNr)
2. 在电脑端下载taojinbi.js文件，使用电脑端qq或微信发给手机端
3. 导入js文件到autojs(可直接在微信/QQ/文件浏览中选择使用其他方式打开)
4. 在autojs中开启无障碍服务并点击运行导入的js文件

auto.js视频运行教程:https://www.bilibili.com/video/BV1Cy4y1S7qE


## 淘金币app运行
1. 在[release页面](https://github.com/JavisPeng/taojinbi/releases)下载taojinbi.apk并安装
2. 为淘金币开启无障碍服务和悬浮框权限(悬浮框权限在华为手机：设置->应用->应用功能->淘金币->显示在其他应用的上层->允许)

淘金币app视频运行教程：https://www.bilibili.com/video/BV1kp4y1q7CD/


# 免责声明
为本人Auto.js学习交流的开源非营利项目，仅作为程序员之间相互学习交流之用，使用需严格遵守开源许可协议。严禁用于商业用途，禁止使用进行任何盈利活动。对一切非法使用所产生的后果，本人概不负责。
