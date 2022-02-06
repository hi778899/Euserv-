# Euserv-
Euserv自动续期
# ********注意********
EUserv加入了邮箱验证，可以使用项目eu_ex进行部署
# 说明
自动获取账号内所有的VPS项目，并检测是否需要续期，需要续期会自动续期。
# 使用说明
### 登录
```
USERNAME: 你的EUserv账户邮箱或Customer ID 第二个账户
PASSWORD: 第一个账户密码 第二个账户密码
```
###
```
USERID = 'arun56'
APIKEY = 'wMjXmBIcHcdYqO2RrsVN'
```
APIKEY 每天有 100 次免费搜索
采用 TrueCaptcha API 处理验证码识别，代码默认使用 demo apikey，最好去 https://apitruecaptcha.org 注册，然后使用自己的 apikey
### Server酱的推送
```
SCKEY: (可选)这里填Server酱的key，无需推送可不填
```
### 邮件推送
```
msg_from:发送方邮箱
passwd:填入发送方邮箱的授权码
msg_to:收件人邮箱
smtp:SMTP服务器地址
port:SMTP服务器端口
```
# 本脚本支持Fork
**如需Fork需点击你的仓库右上角的 Settings，找到 Secrets 这一项，添加两个秘密环境变量`USERNAME`和`PASSWORD`。如需推送需添加其余变量。支持同时添加多个帐户，数据之间用单个空格 ` ` 隔开即可，帐户名和帐户密码需一一对应。**
但由于github的关心，取消了yml文件的设置
如果想要form本仓库，请将action.yml加入到工作流
最后在你这个 Fork 的仓库内修改一下```.github/workflows/action.yml ```文件（这个本项目的Workflow的配置文件）。请见这一段落：

```
schedule:
  - cron: '50 1 * * 0,3'
```

这一Cron表达式规定了本脚本的执行时间，即默认每周日、每周三1:50 UTC执行脚本。请修改这一文件否则脚本可能无法正常工作。

如果你在Github上编辑此文件，Github会为你提供即时的注释，即类似“Runs at 01:50 UTC on Sun and Wed”，请根据这一注释自行设置脚本执行时间。
# 注意
德鸡加入了验证码登录，本脚本已更新。
增加 登录重试机制，默认为 5 次
