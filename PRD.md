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
- 需求 Requirements: ![Aaron Swartz](https://raw.githubusercontent.com/paihsinLi/API_ML_AI/master/%E7%BB%93%E6%9E%84%E5%9B%BE/%E9%9C%80%E6%B1%82.png)
   - 所对映的标题：菜谱识别
   - 重要程度：重要
   - 笔记：百度图像识别API请求回应  
- 问题 Questions: 帮助不会做菜甚至想学做菜的人也能学会做菜，甚至知道如何搭配菜式，并且可以和志同道合的人一起交流想法。
- 不做 Not doing: 有些特殊菜式和部分网红菜式不做探讨
## 产品结构
#### 产品结构图
![Aaron Swartz](https://raw.githubusercontent.com/paihsinLi/API_ML_AI/master/%E7%BB%93%E6%9E%84%E5%9B%BE/%E4%BA%A7%E5%93%81%E7%BB%93%E6%9E%84%E5%9B%BE.png)
#### 产品信息结构图
![Aaron Swartz](https://raw.githubusercontent.com/paihsinLi/API_ML_AI/master/%E7%BB%93%E6%9E%84%E5%9B%BE/%E4%BA%A7%E5%93%81%E4%BF%A1%E6%81%AF%E7%BB%93%E6%9E%84%E5%9B%BE.png)
## 功能阐述
#### 功能权限
- 未登录状态: 未登录状态下可查看菜谱
- 已登录状态: 已登录状态下可执行所有操作
#### 键盘说明
- 点击手机注册/手机登陆输入框时弹出数字键盘
- 点击其他输入框时弹出字母键盘
