<div align="center">


<h1 align="center">


wechat-public-account-push


</h1>


[![GitHub Stars](https://img.shields.io/github/stars/wangxinleo/wechat-public-account-push?style=flat-square)](https://github.com/wangxinleo/wechat-public-account-push/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/wangxinleo/wechat-public-account-push?style=flat-square)](https://github.com/wangxinleo/wechat-public-account-push/network/members)
[![GitHub Issues](https://img.shields.io/github/issues/wangxinleo/wechat-public-account-push?style=flat-square)](https://github.com/wangxinleo/wechat-public-account-push/issues)
[![GitHub Contributors](https://img.shields.io/github/contributors/wangxinleo/wechat-public-account-push?style=flat-square)](https://github.com/wangxinleo/wechat-public-account-push/graphs/contributors)
[![GitHub License](https://img.shields.io/github/license/wangxinleo/wechat-public-account-push?style=flat-square)](https://github.com/wangxinleo/wechat-public-account-push/blob/master/LICENSE)
![Unit Test](https://github.com/wangxinleo/wechat-public-account-push/actions/workflows/unit-test.yml/badge.svg)


</div>

**wechat-public-account-push
是一个用于微信公众号/微信测试号给用户执行微信推送的脚本，改编自目前小红书/知乎突然火起来的【给女朋友的七夕浪漫，微信自动推送消息】，用Nodejs实现而成。**

**如果这个项目很有意思，帮忙右上角点个 star✨ 支持我们 ❤❤**

**如果有任何需要帮助可以联系wangxin.leo@outlook.com ❤❤**

[>>> 点这里获取更新公告✨](https://github.com/wangxinleo/wechat-public-account-push/discussions/categories/announcements)

详细功能如下：

- **支持多个收件人设置成不同的测试号模板，专属定制更贴心**
- **推送每日天气**
- **各类文案集锦**
- **支持农历生日提醒**
- **每日/明日/每周/每年星座运势**
- **大学生课程表**
- **前N个值得纪念的日子**
- **推送回执**
- **自定义出参，模板定制更个性**
- **网页自动生成配置插件**
- **支持gitee go / github actions 不需要拥有服务器，白嫖actions执行，每天定时发送**
- **支持本地化部署每天定时发送**
- **理论上支持所有远端的日志推送（目前仅支持测试号，没时间做）**

---
[目录]

<!-- TOC depthFrom:2 -->

- [1. 如何使用](#1-如何使用以测试号为例)
    - [1.1. 第一步：注册一个微信公众测试号](#11-第一步注册一个微信公众测试号)
    - [1.2. 第二步：进行模板配置](#12-第二步进行模板配置)
    - [1.3. 第三步：完成配置文件，并运行 wechat-public-account-push](#13-第三步完成配置文件并运行wechat-public-account-push)
        - [1.3.1. 方式一：使用网页工具自动生成Github-Action配置(不准时，排队执行，胜在免费)](#131-方式一使用网页工具自动生成Github-Action配置不准时排队执行胜在免费)
        - [1.3.2. 方式二：使用Github-Action(不准时，排队执行，胜在免费)](#132-方式二使用Github-Action不准时排队执行胜在免费)
        - [1.3.3. 方式三：使用Gitee-go(定时任务收费，前200分钟免费，非常准时)](#133-方式三使用Gitee-go定时任务收费前200分钟免费非常准时)
        - [1.3.4. 方式四：下载程序包到本地或服务器运行(需要有自己的服务器，使用系统的定时任务非常准时)](#134-方式四下载程序包到本地或服务器运行需要有自己的服务器使用系统的定时任务非常准时)
        - [1.3.5. 方式五：使用云函数运行（需要使用运营商提供的 __付费__ 云函数功能，非常准时)](#135-方式五使用云函数运行需要使用运营商提供的-付费-云函数功能非常准时)
- [2. 公众号模板参数说明](#2-公众号模板参数说明)
- [3. config参数说明](#3-config参数说明)
- [4. 常用的推送模板样例](#4-常用的推送模板样例)
- [5. GitHub/Gitee 如何更改自动执行时间](#5-githubgitee-如何更改自动执行时间)
    - [5.1. github action如何更改自动执行时间](#51-github-action如何更改自动执行时间)
    - [5.2. gitee go如何更改自动执行时间](#52-gitee-go如何更改自动执行时间)
- [6. 常见问题](#6-常见问题)
- [7. 版本发布及更新](#7-版本发布及更新)
- [8. 成为开源贡献成员](#8-成为开源贡献成员)
    - [8.1. 贡献代码](#81-贡献代码)
    - [8.2. 贡献文档](#82-贡献文档)
- [9. 致谢](#9-致谢)
- [10. wechat-public-account-push 答疑群](#10-wechat\-public\-account\-push答疑群)
- [11. 其他](#11-其他)

<!-- /TOC -->


**Github 仓库地址：[wangxinleo/wechat-public-account-push](https://github.com/wangxinleo/wechat-public-account-push)**

**Github
镜像仓库地址（国内备用01）：[wangxinleo/wechat-public-account-push](https://hub.fastgit.xyz/wangxinleo/wechat-public-account-push)**

**Github
镜像仓库地址（国内备用02）：[wangxinleo/wechat-public-account-push](https://hub.njuu.cf/wangxinleo/wechat-public-account-push)**

**Gitee
仓库地址：[wangxinleo/wechat-public-account-push](https://gitee.com/wangxin_leo/wechat-public-account-push)**

**注意：**

- **本仓库开源的初衷是看不下去营销号用这么一个简单的脚本刻意在网络上肆意要求加群/关注微信公众号才能获取源码的行为**
- **本应用仅用于学习和测试，作者本人并不对其负责，请于运行测试完成后自行删除，请勿滥用！**
- **所有代码都是开源且透明的，任何人均可查看，程序不会保存或滥用任何用户的个人信息**
- **请仔细阅读配置文档，自己对自己的配置负责**

运行图示：

![图片无法查看请移步顶部访问 国内备用仓库地址](img/run-img.jpg)

![图片无法查看请移步顶部访问 国内备用仓库地址)](img/run-img-2.jpg)

## 1. 如何使用(以测试号为例)

wechat-public-account-push 实现自消息推送的原理，是通过调用一系列开放的api实现的, 所以也非常适合初学者学习。

**要使用 wechat-public-account-push, 我们只需要做拥有自己的公众号, 得到相关配置信息进行配置即可**

### 1.1. 第一步：注册一个微信公众测试号

- 浏览器打开并登录 [微信公众测试号](https://mp.weixin.qq.com/debug/cgi-bin/sandbox?t=sandbox/login)

- 登录成功后, 就可以生成微信公众测试号的appID和appsecret这两串数字, 记下备用

![图片无法查看请移步顶部访问 国内备用仓库地址](img/wx-test-id.png)

- 扫描测试号二维码关注测试号, 扫描之后, 右边就会出现相应的已关注人员id, 记下备用

![图片无法查看请移步顶部访问 国内备用仓库地址](img/wx-test-follow.png)

### 1.2. 第二步：进行模板配置

新增测试模板, 点击 `新增测试模板` , 进行以下设置


> 这里面的每一个{{***.DATA}}都对应相应的数据，需要就保留，不需要就删掉


> **更多模板** 请查看上方更新内容


模板标题: 自定义，例如: `亲爱的，早上好!`

模板内容:

```
{{date.DATA}}  
城市：{{city.DATA}}  
天气：{{weather.DATA}}  
最低气温: {{min_temperature.DATA}}  
最高气温: {{max_temperature.DATA}}  
今天是我们恋爱的第{{love_day.DATA}}天
今天是我们结婚的第{{marry_day.DATA}}天

{{birthday_message.DATA}}

{{one_talk.DATA}} -- {{talk_from.DATA}}

{{note_en.DATA}}  
{{note_ch.DATA}}
```

模板标题: `推送完成提醒`

模板内容:

```
服务器信息：{{post_time_zone.DATA}} {{post_time.DATA}}

共推送 {{need_post_num.DATA}}  人
成功: {{success_post_num.DATA}} | 失败: {{fail_post_num.DATA}}
成功用户: {{success_post_ids.DATA}}
失败用户: {{fail_post_ids.DATA}}
```

记下模板代码

![图片无法查看请移步顶部访问 国内备用仓库地址](img/wx-test-tmp.png)

### 1.3. 第三步：完成配置文件，并运行wechat-public-account-push

#### 1.3.1 方式一：使用网页工具自动生成Github-Action配置(不准时，排队执行，胜在免费)

> 以下为@shuangxunian ShuangxuNian大佬 提供的网页配置插件
>
> 使用时请详细参考其提供的具体文档
>
> 感谢 ShuangxuNian大佬 的贡献

[✨配置自动生成 传送门 >>>](https://shuangxunian.github.io/wechat-form/)

[❓配置自动生成 教程 >>>](https://github.com/shuangxunian/wechat-form)

#### 1.3.2 方式二：使用Github-Action(不准时，排队执行，胜在免费)
> 世界上最大的同性交友平台(不是)，需要一定的英语基础，**编辑的时候请不要使用网页的自动翻译**

[❓Github-Action部署教程 >>>](./docs/github-actions.md)

#### 1.3.3 方式三：使用Gitee-go(定时任务收费，前200分钟免费，非常准时)
> 国产代码仓库，和github逻辑基本一致。全中文，对萌新友好。

[❓Gitee-Go部署教程 >>>](./docs/gitee-go.md)

#### 1.3.4 方式四：下载程序包到本地或服务器运行(需要有自己的服务器，使用系统的定时任务非常准时)
> 如果是 Nodejs 开发者，直接 Clone 源码，然后 VS 打开后即可直接本地进行运行和调试。
>
> 对于不是开发者的朋友，可以通过以下教程到本地或任意服务器运行

[❓本地或在线服务器部署教程 >>>](./docs/run-in-server.md)


#### 1.3.5 方式五：使用云函数运行（需要使用运营商提供的 __付费__ 云函数功能，非常准时)
>由 @ZzqiZQute zz 大佬提供代码迁移及教程编辑

[❓云函数部署教程 >>>](./docs/cloud-function.md)

## 2. 公众号模板参数说明

以下参数可以被微信公众号的模板消息`{{xxx.DATA}}`捕获，用来自定义小伙伴们需要的信息。

目前可被推送模板获取的字段如下：

> ~~删除线~~ 为已废除的参数

**基础类**

| 参数                     | 详细             | 示例             |
|------------------------|----------------|----------------|
| to_name.DATA        | 收件人姓名          | 老婆3            |
| date.DATA              | YYYY-MM-DD 星期d | 2022-08-26 星期五 |
| province.DATA       | 省份             |  广东            |
| city.DATA              | 城市             |  惠州            |

**天气类**

| 参数                   | 详细     | 示例                                 |
|----------------------|--------|------------------------------------|
| weather.DATA         | 天气     | 阵雨转多云                              |
| min_temperature.DATA | 最低气温   | 25℃                                |
| max_temperature.DATA | 最高气温   | 25℃                                |
| wind_direction.DATA  | 风向     | 持续东南风                              |
| wind_scale.DATA      | 风级     | <3级                                |
| shidu.DATA           | 湿度     | 50%                                |
| pm25.DATA            | PM2.5  | 36                                 |
| pm10.DATA            | PM1.0  | 54                                 |
| sunrise.DATA         | 日出时间   | 06:20                              |
| sunset.DATA          | 日落时间   | 06:20                              |
| aqi.DATA             | 空气质量指数 | 40                                 |
| ganmao.DATA          | 预防感冒提醒 | 儿童、老年人及心脏、呼吸系统疾病患者人群应减少长时间或高强度户外锻炼 |
| notice.DATA          | 天气温馨语  | 雨虽小，注意保暖别感冒                        |

**节假日**
| 参数 | 详细 | 示例 |
|------------------------|----------------|----------------|
| holidaytts.DATA | 下一休息日综合提醒 | 还有3天就周六了，好好工作吧！距离国庆还有18天，早着呢 |

**每日N句**

| 参数                       | 详细        | 示例                                                    |
|--------------------------|-----------|-------------------------------------------------------|
| note_en.DATA             | 金山每日一句-英文 | Nothing in this world that's worth having comes easy. |
| note_ch.DATA             | 金山每日一句-中文 | 这世界上凡是值得拥有的东西，都不易获得。                                  |
| one_talk.DATA            | 每日一言-内容   | 愿你遍布祖国山河，觉得人生也值得                                      |
| talk_from.DATA           | 每日一言-来源   | 晓良                                                    |
| earthy_love_words.DATA   | 土味情话(彩虹屁) | 我今晚会很忙，忙着跟你过日子                                        |
| moment_copyrighting.DATA | 朋友圈文案     | 错过太阳就不要再错过月亮了                                         |
| poison_chicken_soup.DATA | 毒鸡汤       | 我从不以强凌弱，我欺负他之前，真不晓得他比我弱。                              |
| poetry_content.DATA      | 古诗古文-内容   | 举头望明月，低头思故乡。                                          |
| poetry_title.DATA        | 古诗古文-标题   | 静夜思                                                   |
| poetry_author.DATA       | 古诗古文-作者   | 李白                                                    |
| poetry_dynasty.DATA      | 古诗古文-朝代   | 唐代                                                    |

**星座运势**

| 参数                           | 详细   | 示例                |
|------------------------------|------|-------------------|
| comprehensive_horoscope.DATA | 综合运势 | 太多了，不示例了，自己调用查看效果 |
| love_horoscope.DATA          | 爱情运势 | 太多了，不示例了，自己调用查看效果 |
| career_horoscope.DATA        | 事业学业 | 太多了，不示例了，自己调用查看效果 |
| wealth_horoscope.DATA        | 财富运势 | 太多了，不示例了，自己调用查看效果 |
| healthy_horoscope.DATA       | 健康运势 | 太多了，不示例了，自己调用查看效果 |

**计时类**

| 参数                    | 详细                        | 示例                                                            |
|-----------------------|---------------------------|---------------------------------------------------------------|
| ~~love_day.DATA~~     | 已预置, 但是可以删掉, 在配置中自定义, 见下文 | 2674                                                          |
| ~~marry_day.DATA~~    | 已预置, 但是可以删掉, 在配置中自定义, 见下文 | 965                                                           |
| birthday_message.DATA | 生日消息和节日消息                 | 距离 宝贝 的生日还有122天，距离 中秋节还有30天                                   |
| course_schedule.DATA  | 每日的课表                     | 08:00-09:35 高等数学<br/> 09:35-10:35 大学语文 <br/> 10:35-11:35 大学英语 |

**推送回执(特有, 仅在其他模板发送完成后才能获取)**

| 参数                       | 详细        | 示例                  |
|--------------------------|-----------|---------------------|
| post_time_zone.DATA   | 服务器时区     | Asia/Shanghai       |
| post_time.DATA        | 服务器执行脚本时间 | 2022-08-31 19:41:57 |
| need_post_num.DATA    | 共需推送N人    | 4                   |
| success_post_num.DATA | 成功推送N人    | 1                   |
| fail_post_num.DATA    | 推送失败N人    | 3                   |
| success_post_ids.DATA | 推送成功的用户   | 老婆0                 |
| fail_post_ids.DATA    | 推送失败的用户   | 老婆1,老婆2,老婆3         |

**自定义计时及自定义文本插槽**

小伙伴在只要在`CUSTOMIZED_DATE_LIST` 和 `SLOT_LIST` 中按格式填写相应内容

微信测试模板即可获取到你配置中设置好的内容了。

例如，您可以在配置文件中设置一个 `love_day`, 然后在【微信模型消息】中就可以用`{{love_day.DATA}}` 获取到内容了。

```
么么哒！
今天是我们在一起的的第{{love_day.DATA}}天

爱你！
```

> 大概的实现原理类似于下图标注的这样：
> 
> ![图片无法查看请移步顶部访问 国内备用仓库地址](img/self-keyword.png)
> 
> 但是有以下情况需要注意，不要占用表中已有的关键字，会发生不可预料的状况噢！
> 
> ![图片无法查看请移步顶部访问 国内备用仓库地址](img/self-keyword-2.png)

## 3. config参数说明
> 配置文件的详细说明，使用旧配置的小伙伴可以对照此文档增加新的配置

[❓config参数说明 >>>](./docs/config-demo.md)

## 4. 常用的推送模板样例
> 收录一些常用好看的模板消息

[❓常用的推送模板样例 >>>](./docs/default-model.md)


## 5. GitHub/Gitee 如何更改自动执行时间

### 5.1 github action如何更改自动执行时间

这里的脚本使用的是 github 的 workflow 定时任务, 具体脚本文件放置在:

```
wechat-public-account-push/.github/workflows/weixin-push-on-time.yml
```

这里简单说明一下如何更改自动执行时间

目前脚本默认执行时间为 **每天的 北京时间上午 07:30**

如果想要变更脚本定时任务执行时间,可以更改以下代码段

```
on:
  workflow_dispatch:
  schedule:
    # 每天国际时间2:10 运行, 即北京时间 10:10 运行
    - cron: '30 23 * * *'
```

**推荐设置: `30 22 * * *` 或 `30 23 * * *` 等冷门时间，拥堵率低**

**定时任务注意尽量避免设置在 `utc 0:00, XX:00` 这类高拥堵时段。**

**定时任务注意尽量避免设置在 `utc 0:00, XX:00` 这类高拥堵时段。**

**定时任务注意尽量避免设置在 `utc 0:00, XX:00` 这类高拥堵时段。**

![图片无法查看请移步顶部访问 国内备用仓库地址](img/action-cron.png)

或使用[https://crontab.guru](https://crontab.guru)帮助配置

### 5.2 gitee go如何更改自动执行时间

![图片无法查看请移步顶部访问 国内备用仓库地址](img/gitee/gitee-workflow10.png)

![图片无法查看请移步顶部访问 国内备用仓库地址](img/gitee/gitee-workflow11.png)

## 6. 常见问题

[关于获取accessToken:请求失败invalid appsecret rid xxxxx](https://github.com/wangxinleo/wechat-public-account-push/discussions/68)

[关于推送失败，报40001- 4000X](https://github.com/wangxinleo/wechat-public-account-push/discussions/39)

[关于目前仅支持测试号的问题](https://github.com/wangxinleo/wechat-public-account-push/discussions/23)

[关于定时任务好像没有自动执行（?）](https://github.com/wangxinleo/wechat-public-account-push/discussions/20)

[Issues（议题）](https://github.com/wangxinleo/wechat-public-account-push/issues)板块可以用来提交**Bug**和**建议**；

[Discussions（讨论）](https://github.com/wangxinleo/wechat-public-account-push/discussions)板块可以用来**提问**和**讨论**。

所以如果你有疑问，

* 请先确认是否可以通过升级到最新版本解决
* 然后搜索文档（特别是配置说明文档和常见问题文档）查看是否已有解决方案

如果确认还未解决，可以自己提交 Issue，我会尽快确认并解决。

## 7. 版本发布及更新

关于新版本发布后，如何同步最新的内容到自己 Fork 的仓库

### 7.1 重新fork

**删掉后重新Fork会导致之前配置过的GitHub Secrets和提交的代码更改全部丢掉，只能重新部署。**

### 7.2 GitHub Fetch Upstream Branch

- 在自己的项目仓库中选择 "Sync fork"

- 点击 "Update branch" 完成

![图片无法查看请移步顶部访问 国内备用仓库地址](img/pr-1.png)

可能会遇到 **因为冲突需要你们删除你们已经更改的记录**

如果只是纯粹更改配置，放心大胆的点删除, 然后更新最新代码仓库就好了。

如果**你更改了源代码进行了部分定制**, 请注意备份代码段。

### 7.3 actions 脚本自动

**以后会考虑加入actions 脚本每周自动更新fork仓库，但是目前精力不足，只能采用上述保守方案**

建议每个人先看看更新的内容是否是自己需要的再进行更新。

也建议把右上角的 Star 点一下，这样有重要更新时就会有邮件推送了。

## 8. 成为开源贡献成员

### 8.1 贡献代码

如果你有好的想法，欢迎向仓库贡献你的代码，贡献步骤：

* 搜索查看 Issue，确定是否已有人提过同类问题或者有新的想法


* 确认没有同类 Issue 后，自己可新建 Issue，描述问题或建议


* 如果想自己解决，请 Fork 仓库后，在**develop 分支**进行编码开发，完成后**提交 PR 到 develop 分支**，并标注解决的 Issue 编号

我会尽快进行代码审核，测试成功后会合并入 main 主分支，提前感谢您的贡献。

### 8.2 贡献文档

文档部分由于我个人精力有限（写文档比写代码累多了），所以有些地方写的很简略，甚至有遗漏和错别字，不能贡献代码的朋友也欢迎来一起维护文档，欢迎
PR 来纠正我，一样都算是对开源做贡献了。

## 9. 致谢

### 贡献/参与者

@LordonCN Lordon

@ZzqiZQute zz

@shuangxunian ShuangxuNian

感谢那些默默支持我, 鼓励我继续更新这个小玩具的朋友。

感谢所有参与到开发/测试中的朋友们，是大家的帮助让 TA 越来越好！ (*´▽｀)ノノ

## 10. wechat-public-account-push答疑群

不管文档写得多详细，还是会有人不会呐！还是建个群答疑吧!

群我隐藏在文档里了哼哼，不仔细看文档可找不到加群的地方哦！

2022-09-10 算啦还是不隐藏了，你们来尽情问吧。

![图片无法查看请移步顶部访问 国内备用仓库地址](img/wechat-public-account-push.png)

<a target="_blank" href="https://qm.qq.com/cgi-bin/qm/qr?k=y0plwm9zhOI35EwlOdRh372g4KWbqMSt&jump_from=webapi"><img border="0" src="https://pub.idqqimg.com/wpa/images/group.png" alt="wechat-public-account-push 交流群" title="wechat-public-account-push 交流群"></a>

## 11. 其他

时区查询: [https://www.zeitverschiebung.net/cn/all-time-zones.html](https://www.zeitverschiebung.net/cn/all-time-zones.html)

<!-- ## 11. 叨叨两句

**这个仓库只能算是重复实现一下别人的想法, 主要是了解到了这个想法却一直找不到原作者的源码很是苦恼, 结果还遇到了要求加关注的情况**

**真的非常不喜欢目前国内论坛/某乎/某书/某字母站的博主在分享一些有趣的项目后,甚至是分享了教程之后却不提供源码链接,要求关注公众号或QQ群才进行分享**

**虽然我无权谴责这些流量变现的做法, 但是我认为作者既然开源自己的作品, 那就是希望其他人能一起体会coding的喜悦, 请部分博主尊重作者意愿, 尊重开源协议**

![图片无法查看请移步顶部访问 国内备用仓库地址](img/dis.png)

![图片无法查看请移步顶部访问 国内备用仓库地址](img/dis-2.png) -->
