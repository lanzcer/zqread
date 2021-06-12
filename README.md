可以就填下我的邀请码：51767260

# actions-youth
- 中青看点极速版本
- 也可以node或githubaction运行
- 每天1元左右

~~~
2. 获取Cookie方法，可随时更新
 ① 进入app，进入任务中心或者签到一次,即可获取Cookie. 
 ② 阅读一篇文章，获取阅读请求body，获取200个body就可以了
 ③ 同时获取阅读时长，
 ④ 在阅读文章最下面有个惊喜红包，点击获取惊喜红包请求
3.增加转盘抽奖通知间隔，为了照顾新用户，前三次会有通知，以后默认每50次转盘抽奖通知一次，可自行修改❗️ 转盘完成后通知会一直开启
4.非专业人士制作，欢迎各位大佬提出宝贵意见和指导
5.增加每日打卡，打卡时间每日5:00-8:00❗️，请不要忘记设置运行时间，共4条Cookie，请全部获取，获取请注释
6. 支持Github Actions多账号运行，填写'YOUTH_HEADER'值多账号时用'#'号隔开，其余值均用'&'分割  ‼️，当转盘次数为50或者100并且余额大于10元时推送通知


============Quantumultx===============
[rewrite_local]
# 中青获取body
https:\/\/ios\.baertt\.com\/v5\/article\/complete.json url script-request-body https://raw.githubusercontent.com/songyangzz/QuantumultX/master/zqgetbody.js
# 中青看点极速版
https:\/\/\w+\.youth\.cn\/TaskCenter\/(sign|getSign) url script-request-header https://raw.githubusercontent.com/akuticlouds/actions-youth/main/youth.js
# 中青看点极速版
https?:\/\/ios\.baertt\.com\/v5\/article\/complete url script-request-body https://raw.githubusercontent.com/akuticlouds/actions-youth/main/youth.js
# 中青看点极速版
https:\/\/ios\.baertt\.com\/v5\/article\/red_packet url script-request-body https://raw.githubusercontent.com/akuticlouds/actions-youth/main/youth.js
# 中青看点极速版
https:\/\/ios\.baertt\.com\/v5\/user\/app_stay\.json url script-request-body https://raw.githubusercontent.com/akuticlouds/actions-youth/main/youth.js

主机名：*.youth.cn, ios.baertt.com

[task_local]
# 中青看点极速版
0 0/14 5-14 * * * https://raw.githubusercontent.com/akuticlouds/actions-youth/main/youth.js, tag=中青看点极速版, img-url=https://raw.githubusercontent.com/Orz-3/task/master/youth.png, enabled=true

# 中青看点极速版自动阅读
0 0 0-10/1 * * * https://raw.githubusercontent.com/akuticlouds/actions-youth/main/YOUTH_READ.js, tag=中青看点极速版自动阅读, img-url=https://raw.githubusercontent.com/Orz-3/task/master/youth.png, enabled=true


Surge 4.0 :
[Script]
中青看点 = type=cron,cronexp=35 5 0 * * *,script-path=https://raw.githubusercontent.com/akuticlouds/actions-youth/main/youth.js,script-update-interval=0
中青看点 = type=http-request,pattern=https:\/\/\w+\.youth\.cn\/TaskCenter\/(sign|getSign),script-path=https://raw.githubusercontent.com/akuticlouds/actions-youth/main/youth.js
中青看点 = type=http-request,pattern=https:\/\/ios\.baertt\.com\/v5\/article\/complete,script-path=https://raw.githubusercontent.com/akuticlouds/actions-youth/main/youth.js, requires-body=true
中青看点 = type=http-request,pattern=https:\/\/ios\.baertt\.com\/v5\/article\/red_packet,script-pathhttps://raw.githubusercontent.com/akuticlouds/actions-youth/main/youth.js, requires-body=true
中青看点 = type=http-request,pattern=https:\/\/ios\.baertt\.com\/v5\/user\/app_stay\.json,script-pathhttps://raw.githubusercontent.com/akuticlouds/actions-youth/main/youth.js, requires-body=true


Loon 2.1.0+
[Script]
# 本地脚本
cron "04 00 * * *" script-path=https://raw.githubusercontent.com/akuticlouds/actions-youth/main/youth.js, enabled=true, tag=中青看点
http-request https:\/\/\w+\.youth\.cn\/TaskCenter\/(sign|getSign) script-path=https://raw.githubusercontent.com/akuticlouds/actions-youth/main/youth.js
http-request https:\/\/ios\.baertt\.com\/v5\/article\/complete script-path=https://raw.githubusercontent.com/akuticlouds/actions-youth/main/youth.js, requires-body=true
http-request https:\/\/ios\.baertt\.com\/v5\/article\/red_packet script-path=https://raw.githubusercontent.com/akuticlouds/actions-youth/main/youth.js, requires-body=true
http-request https:\/\/ios\.baertt\.com\/v5\/user\/app_stay\.json script-path=https://raw.githubusercontent.com/akuticlouds/actions-youth/main/youth.js, requires-body=true
-----------------

[MITM]
hostname = *.youth.cn, ios.baertt.com 


~~~

githubAction
在创建的setting里的Secrets增加下面值就可以 
YOUTH_HEADER
YOUTH_END
YOUTH_HEADER
YOUTH_READ
YOUTH_REDBODY
YOUTH_START
YOUTH_TIME
