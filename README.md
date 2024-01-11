## 一、前言

### [全平台国际化话翻译解决方案](https://github.com/MZCretin/Eva-Translate)
项目国际化翻译解决方案，支持Android、iOS、Flutter、前端Vue、后端PHP等等，点几下按钮就能实现翻译内容的自动抓取和翻译后文件的自动生成，适合各类场景下的国际化需求。

------------

几年前我开发了一个应用《段子乐》，并在当时也达到了日活7000左右的高峰，不过因为资金的问题（短视频太烧钱），在当时选择了停运项目，直到后面用户都散去之后才重启项目。虽然说项目进行了几次大的改版，现在已经3.0.0了，但是日活却只剩百十来个了。

在朋友的建议下，我决定做一个更有意义的事情，将项目接口和数据进行对外开放，让爱折腾的朋友可以用这些接口做一个自己的应用，当然包括但不仅限于开发一个 Android App，iOS App，小程序，H5应用，Flutter应用等等。

我的个人主页为：https://www.mxnzp.com ，如果你想联系我，在这里可以找到我的联系方式。如果你希望对接此接口，那么你一定会遇到很多问题，所以你可以联系我加群，一起讨论。

## 更新日志

+ **2022年05月26日13:57:15**

  新增 [4.3.3.2 获取指定用户喜欢的段子列表](https://github.com/MZCretin/duanzile-open-api#4332-%E8%8E%B7%E5%8F%96%E6%8C%87%E5%AE%9A%E7%94%A8%E6%88%B7%E5%96%9C%E6%AC%A2%E7%9A%84%E6%AE%B5%E5%AD%90%E5%88%97%E8%A1%A8) 和 [4.3.3.3 获取指定用户段子列表](https://github.com/MZCretin/duanzile-open-api#4333-%E8%8E%B7%E5%8F%96%E6%8C%87%E5%AE%9A%E7%94%A8%E6%88%B7%E6%AE%B5%E5%AD%90%E5%88%97%E8%A1%A8) 两个接口。

## 二、接口开放简介

《段子乐》本身是一个类似《内涵段子》的应用，主要包含以下功能：

+ 纯文，图片和短视频类型的段子
+ 对段子内容的点赞，评论，收藏和分享
+ 实现类似抖音一样划一划浏览短视频内容
+ 发布纯文，图片和短视频段子
+ 用户关注，粉丝体系
+ 消息系统，对接了极光IM和推送
+ 乐豆系统，积分抽奖等等
+ ...

本次开放除了一些特殊功能包括IM消息相关，第三方QQ微信登录和一键登录之外，其他功能所对应的接口都开放，所以理论上你完全可是实现一个另一个自己的《段子乐》（注：IM和推送你可以自己对接，不让后端介入）。

先大致展示下一些主要的页面：

<div align=center background=red>
  <img style="margin-right: 10px;margin-bottom: 10px; " width="30%" height="100%" src="./img/3.png" alt="我的页面" />
  <img style="margin-right: 10px;margin-bottom: 10px; " width="30%" height="100%" src="./img/page1.png" alt="首页"/>
  <img style="margin-right: 10px;margin-bottom: 10px; " width="30%" height="100%" src="./img/19.png" alt="我的页面"/>
  <img style="margin-right: 10px;margin-bottom: 10px; " width="30%" height="100%" src="./img/25.png" alt="我的页面"/>
  <img style="margin-right: 10px;margin-bottom: 10px; " width="30%" height="100%" src="./img/26.png" alt="我的页面"/>
  <img style="margin-right: 10px;margin-bottom: 10px; " width="30%" height="100%" src="./img/2.png" alt="我的页面"/>
  <img style="margin-right: 10px;margin-bottom: 10px; " width="30%" height="100%" src="./img/page2.png" alt="划一划"/>
  <img style="margin-right: 10px;margin-bottom: 10px; " width="30%" height="100%" src="./img/24.png" alt="我的页面"/>
  <img style="margin-right: 10px;margin-bottom: 10px; " width="30%" height="100%" src="./img/page3.png" alt="消息页面"/>
  <img style="margin-right: 10px;margin-bottom: 10px; " width="30%" height="100%" src="./img/13.png" alt="我的页面"/>
  <img style="margin-right: 10px;margin-bottom: 10px; " width="30%" height="100%" src="./img/page4.png" alt="我的页面"/>
  <img style="margin-right: 10px;margin-bottom: 10px; " width="30%" height="100%" src="./img/1.png" alt="我的页面"/>
  <img style="margin-right: 10px;margin-bottom: 10px; " width="30%" height="100%" src="./img/4.png" alt="我的页面"/>
  <img style="margin-right: 10px;margin-bottom: 10px; " width="30%" height="100%" src="./img/5.png" alt="我的页面"/>
  <img style="margin-right: 10px;margin-bottom: 10px; " width="30%" height="100%" src="./img/6.png" alt="我的页面"/>
  <img style="margin-right: 10px;margin-bottom: 10px; " width="30%" height="100%" src="./img/7.png" alt="我的页面"/>
  <img style="margin-right: 10px;margin-bottom: 10px; " width="30%" height="100%" src="./img/8.png" alt="我的页面"/>
  <img style="margin-right: 10px;margin-bottom: 10px; " width="30%" height="100%" src="./img/9.png" alt="我的页面"/>
  <img style="margin-right: 10px;margin-bottom: 10px; " width="30%" height="100%" src="./img/10.png" alt="我的页面"/>
  <img style="margin-right: 10px;margin-bottom: 10px; " width="30%" height="100%" src="./img/11.png" alt="我的页面"/>
  <img style="margin-right: 10px;margin-bottom: 10px; " width="30%" height="100%" src="./img/12.png" alt="我的页面"/>
  <img style="margin-right: 10px;margin-bottom: 10px; " width="30%" height="100%" src="./img/14.png" alt="我的页面"/>
  <img style="margin-right: 10px;margin-bottom: 10px; " width="30%" height="100%" src="./img/15.png" alt="我的页面"/>
  <img style="margin-right: 10px;margin-bottom: 10px; " width="30%" height="100%" src="./img/16.png" alt="我的页面"/>
  <img style="margin-right: 10px;margin-bottom: 10px; " width="30%" height="100%" src="./img/17.png" alt="我的页面"/>
  <img style="margin-right: 10px;margin-bottom: 10px; " width="30%" height="100%" src="./img/18.png" alt="我的页面"/>
  <img style="margin-right: 10px;margin-bottom: 10px; " width="30%" height="100%" src="./img/20.png" alt="我的页面"/>
  <img style="margin-right: 10px;margin-bottom: 10px; " width="30%" height="100%" src="./img/21.png" alt="我的页面"/>
  <img style="margin-right: 10px;margin-bottom: 10px; " width="30%" height="100%" src="./img/22.png" alt="我的页面"/>
  <img style="margin-right: 10px;margin-bottom: 10px; " width="30%" height="100%" src="./img/23.png" alt="我的页面"/>

</div>



具体体验一下什么是《段子乐》，请点击：https://www.pgyer.com/rmjK ，也可以给你一个页面跳转的参考，如果对接完所有接口，你可以大致开发出这么一个APP。

## 三、对接之前

对接接口之前，有些约定要提前告知。开放接口文档已托管到github，后续肯定会有很多新增和修改，将会同步在github上，而不会更新此文章，所以请提前收藏该地址，你甚至可以点个star：https://github.com/MZCretin/duanzile-open-api

### 3.1 请求接口的HOST地址

请求接口的HOST地址为：http://tools.cretinzp.com/jokes

### 3.2 获取开放API接口调用凭证

此项目对外开放只针对自己人，所以你需要是RollApi的用户，搜索微信小程序【Roll地盘】，点击我的页面，选择【做个段子应用】，可获取到一个专属的project_token（如果你之前没有绑定过手机号，需要先绑定手机号），获取到这个凭证之后，请妥善保管，并在每次调用任意开放api接口的时候，在请求头中加入一个key-value，key为project_token，value为你刚刚申请的值。

### 3.3 调用接口通用的请求头

在你调用的每个接口中，请包含如下请求头信息【必须，后台会强校验】：

| 请求头KEY | 请求头VALUE                                                  | 请求头含义       |
| --------- | ------------------------------------------------------------ | ---------------- |
| token     | 登录成功之后接口会返回token，你需要存储在本地，每次请求带上  | 用户凭证信息     |
| uk        | 设备的唯一id，请尽量保证针对设备唯一，长度32以内             | 用户设备唯一标识 |
| channel   | 请直接填写cretin_open_api                                    | 渠道来源         |
| app       | 拼接版本号版本标识和系统版本，用;分开，例如 1.0.0;1;10，代表版本号1.0.0，版本标识1，系统为Android 10，其他也类似 | app信息          |
| device    | 拼接版本设备信息，设备品牌和设备型号，用;分开，例如HUAWEI;CDY-AN00 | 设备信息         |

### 3.4 接口返回数据的格式

接口返回的数据结构如下，后台能保证只要是请求到了后端，每个接口都会返回这种格式：

+ 其中code代表接口返回的状态码，当code=200，标识此接口请求成功，当code=202代表用户登录状态过期，也就代表你本地的token过期了，此时你需要清除本地的登录状态，让用户重新登录。
+ msg是当code不为200时候的错误信息，你可以将此信息提示给用户。
+ data是该请求的实体数据，具体返回什么格式取决于每个接口本身。

```json
{
  "data": null,
  "msg": "数据返回成功",
  "code": 200
}
```

### 3.5 其他的一些说明

+ **1、如何查看发送成功的验证码**

  接口中有发验证码的接口，当然我没有真的给你的手机号发送一条验证码，否则我短信费也顶不住。当你调用接口发送成功之后，你可以进入【Roll地盘】小程序，然后点击《我的》，然后点击《做个段子应用》，然后点击《查看短信验证码》，就可以查看近期发送的所有验证码信息了；另外一种方式，你可以关注《Cretin的开发之路》公众号，然后输入#13即可查看对应手机号的验证码信息了。

+ **2、项目中发布功能用的图片和视频怎么处理**

  项目中所用到的图片和视频资源均上传到七牛云上面，所以你需要集成七牛云的SDK，上传文件的时候，请调用相关接口获取到七牛云上传token：

  http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E5%B7%A5%E5%85%B7Helper%E6%8E%A5%E5%8F%A3/getTokenUsingPOST 

  然后再进行上传文件。具体操作可参考链接（这个是Andorid的使用链接，其他端请自行查询）：

  https://developer.qiniu.com/kodo/1236/android

+ **3、接口中返回的视频和图片链接进行了加密，如何解密**

  链接使用了简单的对称加密，请联系我或者加入交流群，我会告知大家加密方式和加密秘钥，解析完即可获取真实的视频链接。

+ **4、...**

## 四、开放接口说明

接口文档已经上传，可直接查看在线接口文档，包含65个API接口。这里对每个页面需要的接口进行一个阐述，接口地址为：http://tools.cretinzp.com/jokes/doc.html

### 4.1、首页类接口（7个）

#### 4.1.1 主页-推荐

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/APP%E9%A6%96%E9%A1%B5%E6%8E%A5%E5%8F%A3/homeRecommendListUsingPOST

#### 4.1.2 主页-新鲜

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/APP%E9%A6%96%E9%A1%B5%E6%8E%A5%E5%8F%A3/homeLatestListUsingPOST

#### 4.1.3 主页-纯文

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/APP%E9%A6%96%E9%A1%B5%E6%8E%A5%E5%8F%A3/homeTextListUsingPOST

#### 4.1.4 主页-趣图

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/APP%E9%A6%96%E9%A1%B5%E6%8E%A5%E5%8F%A3/homePicListUsingPOST

#### 4.1.5 主页-关注

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/APP%E9%A6%96%E9%A1%B5%E6%8E%A5%E5%8F%A3/getAttentionUserJokesUsingPOST

#### 4.1.6 主页-搜索

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/APP%E9%A6%96%E9%A1%B5%E6%8E%A5%E5%8F%A3/searchJokesUsingPOST

#### 4.1.7 主页-关注-推荐关注

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/APP%E9%A6%96%E9%A1%B5%E6%8E%A5%E5%8F%A3/recommendAttentionUsingPOST

### 4.2、工具类接口（8个）

#### 4.2.1 主页-搜索-热搜关键词

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E5%B7%A5%E5%85%B7Helper%E6%8E%A5%E5%8F%A3/getHotSearchUsingPOST

#### 4.2.2 获取分享段子的数据

点击任意段子的更多按钮，选择分享到平台前调用接口，获取分享数据

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E5%B7%A5%E5%85%B7Helper%E6%8E%A5%E5%8F%A3/getJokeShareUsingPOST

#### 4.2.3 获取分享用户的内容

点击【我的】，点击分享给朋友，在分享到平台前，调用此接口获取你的信息进行分享

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E5%B7%A5%E5%85%B7Helper%E6%8E%A5%E5%8F%A3/getUserShareUsingPOST

#### 4.2.4 分享段子成功计数

段子分享成功之后调用此接口进行分享次数计数

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E5%B7%A5%E5%85%B7Helper%E6%8E%A5%E5%8F%A3/jokeShareCountUsingPOST

#### 4.2.5 获取qq群信息

点击【我的】，点击我的客服，调用此接口获取qq群信息，打开qq群聊页面。

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E5%B7%A5%E5%85%B7Helper%E6%8E%A5%E5%8F%A3/getQQServiceUsingPOST

#### 4.2.6 获取七牛云token

在应用内上传头像，上传图片，上传视频等需要先获取七牛云的token，再使用sdk上传内容。

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E5%B7%A5%E5%85%B7Helper%E6%8E%A5%E5%8F%A3/getTokenUsingPOST

#### 4.2.7 举报内容

点击某一个段子的更多按钮，可以举报内容，或者点击某个用户头像，右上角也有举报的入口。

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E5%B7%A5%E5%85%B7Helper%E6%8E%A5%E5%8F%A3/reportUsingPOST

#### 4.2.8 意见反馈

点击【我的】，点击意见反馈

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E5%B7%A5%E5%85%B7Helper%E6%8E%A5%E5%8F%A3/feedbackUsingPOST

### 4.3 段子相关接口（23个）

#### 4.3.1.1 发布段子

发布段子之前，如果有视频和图片，需要先上传到七牛云，具体请看4.2.6条。

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E6%AE%B5%E5%AD%90%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/postJokesUsingPOST

#### 4.3.1.2 删除段子

仅自己可以删除自己的段子。

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E6%AE%B5%E5%AD%90%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/deleteJokesUsingPOST

#### 4.3.1.3 评论段子-一级评论

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E6%AE%B5%E5%AD%90%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/commentUsingPOST

#### 4.3.1.4 删除一级评论

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E6%AE%B5%E5%AD%90%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/commentDeleteUsingPOST

#### 4.3.1.5 添加子评论

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E6%AE%B5%E5%AD%90%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/commentChildUsingPOST

#### 4.3.1.6 删除子评论

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E6%AE%B5%E5%AD%90%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/itemCommentDeleteUsingPOST

#### 4.3.1.7 给主评论点赞/取消点赞 

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E6%AE%B5%E5%AD%90%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/commentLikeUsingPOST

#### 4.3.1.8 给段子点赞/取消点赞 

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E6%AE%B5%E5%AD%90%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/likeUsingPOST

#### 4.3.1.9 收藏/取消收藏 段子

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E6%AE%B5%E5%AD%90%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/collectJokesUsingPOST

#### 4.3.2.0 获取段子评论列表

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E6%AE%B5%E5%AD%90%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/commentListUsingPOST

#### 4.3.2.1 获取某一个评论的子评论列表

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E6%AE%B5%E5%AD%90%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/commentItemListUsingPOST

#### 4.3.2.2 获取对某个段子收藏状态

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E6%AE%B5%E5%AD%90%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/isCollectJokesUsingPOST

#### 4.3.2.3 获取段子的点赞列表

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E6%AE%B5%E5%AD%90%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/getTargetLikeListUsingPOST

#### 4.3.2.4 获取段子详情

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E6%AE%B5%E5%AD%90%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/getTargetJokesUsingPOST

#### 4.3.2.5 获取指定用户点赞的图文段子列表

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E6%AE%B5%E5%AD%90%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/getTargetUserLikePicTextJokesListUsingPOST

#### 4.3.2.6 获取指定用户点赞的视频段子列表

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E6%AE%B5%E5%AD%90%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/getTargetUserLikeVideoListUsingPOST

#### 4.3.2.7 获取指定用户自己的视频段子列表

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E6%AE%B5%E5%AD%90%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/getTargetUserVideoListUsingPOST

#### 4.3.2.8 获取指定用户自己的图文段子列表

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E6%AE%B5%E5%AD%90%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/getTargetUserPicTextJokesListUsingPOST

#### 4.3.2.9 获取指定视频段子id列表的视频列表

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E6%AE%B5%E5%AD%90%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/getTargetIdsVideoListUsingPOST

#### 4.3.3.0 获取正在审核的段子列表

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E6%AE%B5%E5%AD%90%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/getAuditJokesListUsingPOST

#### 4.3.3.1 给段子 踩/取消踩

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E6%AE%B5%E5%AD%90%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/unlikeUsingPOST

#### 4.3.3.2 获取指定用户喜欢的段子列表

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E6%AE%B5%E5%AD%90%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/getTargetUserLikeWholeJokesListUsingPOST

#### 4.3.3.3 获取指定用户段子列表

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E6%AE%B5%E5%AD%90%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/getTargetUserJokesListUsingPOST

### 4.4 用户相关接口（28个）

#### 4.4.1.1 用户关注

点击关注按钮触发的操作

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E7%94%A8%E6%88%B7%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/userAttentionUsingPOST

#### 4.4.1.2 获取指定用户关注列表

点击某个用户头像，点击他的关注，进入关注列表。

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E7%94%A8%E6%88%B7%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/getUserAttentionListUsingPOST

#### 4.4.1.3 绑定邀请码

点击【我的】，点击【设置】，点击【用户信息】，最下面，绑定邀请码。

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E7%94%A8%E6%88%B7%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/bindInviteCodeUsingPOST

#### 4.4.1.4 检查视频下载权限

点击任意视频段子，点击更多，点击下载，下载前调用此接口判断能否下载视频。

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E7%94%A8%E6%88%B7%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/checkUserDownloadPermissionUsingPOST

#### 4.4.1.5注销账户

点击【我的】，点击【设置】，点击【账号与安全】，最下面，注销账户。

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E7%94%A8%E6%88%B7%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/closeAccountUsingPOST

#### 4.4.1.6 获取当前登录用户收藏列表

点击【我的】，点击顶部用户昵称，切换tab到收藏。

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E7%94%A8%E6%88%B7%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/getUserCollectListUsingPOST

#### 4.4.1.7 获取指定用户评论列表

点击【我的】，点击顶部用户昵称，切换tab到评论。

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E7%94%A8%E6%88%B7%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/getTargetCommentListUsingPOST

#### 4.4.1.8 获取指定用户粉丝列表

点击【我的】，点击顶部用户昵称，点击粉丝

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E7%94%A8%E6%88%B7%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/getUserFansListUsingPOST

#### 4.4.1.9 获取当前登录的用户信息

点击【我的】，会获取当前用户信息

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E7%94%A8%E6%88%B7%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/getUserInfoUsingPOST

#### 4.4.2.0 获取指定用户的用户信息

点击用户头像，进入个人主页，会调用此接口。

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E7%94%A8%E6%88%B7%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/getTargetUserInfoUsingPOST

#### 4.4.2.1 更新当前用户的用户信息

点击【我的】，点击顶部昵称，进入我的主页，点击编辑信息。

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E7%94%A8%E6%88%B7%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/updateUserInfoUsingPOST

#### 4.4.2.2 获取当前用户的段子列表

点击【我的】，点击顶部用户昵称，切换tab到作品。

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E7%94%A8%E6%88%B7%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/getUserJokesListUsingPOST

#### 4.4.2.3 获取当前登录用户的积分信息

点击【我的】，点击顶部【乐豆】，顶部信息

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E7%94%A8%E6%88%B7%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/getLedouInfoUsingPOST

#### 4.4.2.4 获取当前登录用户的积分列表信息

点击【我的】，点击顶部【乐豆】，列表数据

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E7%94%A8%E6%88%B7%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/getLedouListUsingPOST

#### 4.4.2.5 当前用户抽奖

点击【我的】，点击顶部【乐豆】，点击【乐豆抽奖】

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E7%94%A8%E6%88%B7%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/userLotteryUsingPOST

#### 4.4.2.6 当前用户抽奖列表

点击【我的】，点击顶部【乐豆】，点击【乐豆抽奖】，点击抽奖记录

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E7%94%A8%E6%88%B7%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/userLotteryListUsingPOST

#### 4.4.2.7 获取当前用户喜欢的段子列表

点击【我的】，点击顶部用户昵称，切换tab到喜欢。

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E7%94%A8%E6%88%B7%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/getUserLikeListUsingPOST

#### 4.4.2.8 验证码登录

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E7%94%A8%E6%88%B7%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/loginByCodeUsingPOST

#### 4.4.2.9 获取登录验证码

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E7%94%A8%E6%88%B7%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/loginGetCodeUsingPOST

#### 4.4.3.0 账号密码登录

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E7%94%A8%E6%88%B7%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/loginByPswUsingPOST

#### 4.4.3.1 获取当前用户的消息列表

点击【消息】，点击顶部消息入口。

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E7%94%A8%E6%88%B7%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/getTargetMsgListUsingPOST

#### 4.4.3.2 获取当前登录用户系统消息列表

点击【消息】，点击列表中的系统消息item

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E7%94%A8%E6%88%B7%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/getSystemMessageListUsingPOST

#### 4.4.3.3 获取当前登录用户的未读消息数

点击【消息】，获取消息未读数，显示在顶部

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E7%94%A8%E6%88%B7%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/getTargetMsgUnReadUsingPOST

#### 4.4.3.4 修改密码

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E7%94%A8%E6%88%B7%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/changePswUsingPOST

#### 4.4.3.5 重置密码

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E7%94%A8%E6%88%B7%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/resetPswUsingPOST

#### 4.4.3.6 重置密码获取验证码

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E7%94%A8%E6%88%B7%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/resetPswGetCodeUsingPOST

#### 4.4.3.7 搜索用户

点击【消息】，点击右上角搜索按钮。

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E7%94%A8%E6%88%B7%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/searchUserUsingPOST

#### 4.4.3.8 当前用户签到

进入首页自动调用此接口，发放积分。

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E7%94%A8%E6%88%B7%E7%9B%B8%E5%85%B3%E6%8E%A5%E5%8F%A3/userSigninUsingPOST

### 4.5 仿抖音划一划（1个）

#### 4.5.1 获取划一划页面的推荐列表数据

点击【划一划】，列表数据获取

http://tools.cretinzp.com/jokes/doc.html#/3.0.0/%E9%A6%96%E9%A1%B5%E4%BB%BF%E6%8A%96%E9%9F%B3%E5%88%97%E8%A1%A8/homeListForTypeUsingPOST
