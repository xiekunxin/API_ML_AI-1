- Target release: 2018年11月25日
- Epic: 厨房大师APP
- Document Status: 进行中
- Document owner: 李佰芯
- Designer: 李佰芯
- Developer: 李佰芯
- QA: 李佰芯
- Goals: 识别菜谱，提供美食烹饪方法，技巧学习、交流指导。
- Background and strategic fit: 在朋友圈和微博上看到许多转发的美食却不知道菜名和做法，可是又十分想尝试。
- Assumptions: 用户使用此主要功能时，主要是在想尝试识别这道菜与其做法或分享自己做菜的过程和想法。
- 需求 Requirements: 

| 序号 | 使用场景 | 问题需求 | 对应功能 |
| ------ | ------ | ------ | ------ |
| 1 | 想做饭给对象吃，但是不知道如何下手 | 想获取全头到尾的全套指导 | 菜品搭配，菜谱功能 |
| 2 | 突然想吃某道菜，但是之前从来没有做过 | 想获得某道菜的制作方式 | 识别菜式 |
| 3 | 做了一道新菜，分享给对做菜感兴趣的人 | UGC段视频分享 | 用户分享功能,点赞和转发功能 |
   - 所对映的标题：菜谱识别
   - 重要程度：重要
   - 笔记：百度图像识别API请求回应  
- 问题 Questions: 帮助不会做菜甚至想学做菜的人也能学会做菜，甚至知道如何搭配菜式，并且可以和志同道合的人一起交流想法。
- 不做 Not doing: （语音识别）用户通过语音询问得到菜式在百度百科上的相关信息
## 产品结构
#### 1.产品结构图
![Aaron Swartz](https://github.com/paihsinLi/API_ML_AI/blob/master/结构图/产品结构图.png)
#### 2.产品信息结构图
![Aaron Swartz](https://github.com/paihsinLi/API_ML_AI/blob/master/结构图/产品信息结构图.png)
## 功能阐述
#### 1.功能权限
- 未登录状态: 未登录状态下可查看菜谱
- 已登录状态: 已登录状态下可执行所有操作
#### 2.键盘说明
- 点击手机注册/手机登陆输入框时弹出数字键盘
- 点击其他输入框时弹出字母键盘
#### 3.登录页面/用户注册页面
- 当文本框没有字符的时候，登录按钮不可点击，灰色状态；当帐号和密码输入后，按钮亮起，可以点击，登录成功后，进入首页，否则Toast提示“帐号或密码错误”
- 入口：点击登录页面的注册按钮
#### 4.分享功能
- 入口：点击设置页面的“分享”按钮
- 当点击设置页面的“分享”按钮，从底部滑出弹框，点击图标跳入该图标的第三页面
- 分享成功跳转回原页面，提示“分享成功”
- 分享取消跳转回原页面，无提示
- 分享失败跳转回原页面，提示“很遗憾，分享失败”
#### 5.设置页面
- 点击“清理缓存”按钮，自动清理APP缓存
- 点击“喜好设置”按钮，进入喜好设置页面
- 点击“鼓励一下”按钮，进入appstore为爱厨房评分
- 点击“修改密码”按钮，进入修改密码页面
## API图像识别
- 首先进入到百度AI的官网，找到图像识别需要的API
- 接下来就是代码调用部分了，要使用API，我们需要得到一个叫“access_token”。它需要“API Key”和“Secret Key”来获取。
- 把Api Key和Secret Key提交给https://aip.baidubce.com/oauth/2.0/token?grant_type=client_credentials
- 然后它就会把access_token返回给你，读取下来，然后因为是json格式，所以用json.load()转成字典
- 然后复制access_token那行代码，组合并调用，打开本地相册文件（要识别的美食）
- 再把处理好的img和刚获得的access_token扔进一个字典里面，然后把字典提交给网址(https://aip.baidubce.com/rest/2.0/image-classify/v2/advanced_general)，它会以json格式返回一个分析结果给我们。（得到我们想要的菜式）
## 交互过程
#### 1.界面识别
![Aaron Swartz](https://github.com/paihsinLi/API_ML_AI/blob/master/结构图/界面识别.png)
#### 2.识别模块
![Aaron Swartz](https://github.com/paihsinLi/API_ML_AI/blob/master/结构图/识别模块.png)
#### 3.拍照模块
![Aaron Swartz](https://github.com/paihsinLi/API_ML_AI/blob/master/结构图/拍照模块.png)
#### 4.菜谱模块
![Aaron Swartz](https://github.com/paihsinLi/API_ML_AI/blob/master/结构图/菜谱模块.png)
## 产品原型链接
<https://paihsinli.github.io/API_ML_AI/%E4%BA%A7%E5%93%81%E5%8E%9F%E5%9E%8B/#g=1&p=智能菜谱识别>
## 产品结构图链接
<https://github.com/paihsinLi/API_ML_AI/blob/master/结构图/产品结构图.png>
## 产品信息结构图链接
<https://github.com/paihsinLi/API_ML_AI/blob/master/结构图/产品信息结构图.png>
## 界面识别
<https://github.com/paihsinLi/API_ML_AI/blob/master/结构图/界面识别.png>
## 识别模块
<https://github.com/paihsinLi/API_ML_AI/blob/master/结构图/识别模块.png>
## 拍照模块
<https://github.com/paihsinLi/API_ML_AI/blob/master/结构图/拍照模块.png>
## 菜谱模块
<https://github.com/paihsinLi/API_ML_AI/blob/master/结构图/菜谱模块.png>
