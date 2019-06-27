﻿# Use Cases（用例+活动图）

## 注册登录
### 简要说明
- 用例名称：注册登录
- 相关需求：注册时填写相关必要的信息，真实有效
- 参与者：用户
- 前置信息：在注册前未注册过，在登录前输入正确的登录信息
- 后置信息：用户成功登录或成功注册，随后登录

### 事件流
#### 主成功场景（或基本流程）：
1. 未登录情况下用户进入系统，默认初始切换为登录界面
2. 新用户点击注册跳转到注册页面注册
3. 选择个人用户注册还是机构注册
4. 输入注册必填信息及密码，信息要真实有效
5. 注册成功，跳转至登录页面登录系统
6. 输入账号及密码，匹配则成功登录进系统

#### 扩展（或替代流程）：
- 4a. 输入信息不符合注册要求致使注册失败
    1. 注册手机/邮箱重复或手机邮箱格式错误，更换其他未注册过的正确有效的信息注册
	2. 密码不符合格式要求及必填信息未填写，根据提示要求的格式输入完整正确的信息。

### 活动图
![](pictures/6.2.1.PNG)

## 发布任务
### 简要说明
- 用例名称：发布任务
- 相关需求：发布新任务供用户领取
- 参与者：用户、机构
- 前置信息：用户已成功登录
- 后置信息：成功发布任务并显示在待领取任务中

### 事件流
#### 主成功场景（或基本流程）：
1. 选择是发布快递任务或是发布问卷任务
2. 选择问卷任务，填写发布内容，如问卷题目、截止时间及报酬
3. 点击发布问卷成功发布

#### 扩展（或替代流程）：
- 2a. 选择发布快递任务
    1. 填写快递任务信息，如取送地址，联系方式，报酬
- 3a. 未点击发布前退出
	1. 之前填写信息不保存，任务发布失败，下次发布重新填写
	
### 活动图
![](pictures/6.2.2.PNG)

## 领取任务
### 简要说明
- 用例名称：领取任务
- 相关需求：从已发布任务中领取完成
- 参与者：用户
- 前置信息：用户已成功登录
- 后置信息：领取该任务完成后获得报酬

### 事件流
#### 主成功场景（或基本流程）：
1. 选择是领取快递任务或是领取问卷任务
2. 选择快递任务，通过搜索筛选部分快递任务
3. 点击卡片中快递详情按钮跳转至详情页面查看该项任务的具体信息
4. 在快递详情页了解相关信息后决定领取任务

#### 扩展（或替代流程）：
- 2a. 选择领取问卷任务
    1. 可通过筛选选择部分问卷任务
	2. 未输入搜索条件默认列出所有已发布任务
- 3a. 点击卡片中填写问卷可填写该问卷即为领取问卷任务
	1. 填写完成后获得报酬
- 4a. 进入详情后决定不领取该任务
	1. 返回键返回上一页面，重新选取或退出

### 活动图
![](pictures/6.2.3.PNG)

## 管理任务
### 简要说明
- 用例名称：管理任务
- 相关需求：管理已发布或已接受的任务
- 参与者：用户
- 前置信息：用户已成功登录，存在已发布或者已接受的任务
- 后置信息：进行查询或删除等操作

### 事件流
#### 主成功场景（或基本流程）：
1. 选择是管理快递任务或是管理问卷任务
2. 选择快递任务，默认显示当前用户已发布的快递任务列表
3. 点击已接受按钮显示当前用户已接受的所有快递任务
4. 点击新建快递任务按钮可转至发布快递任务界面
5. 点击列表项后下拉菜单选择查看详情
6. 转至快递详情页面，查看详情

#### 扩展（或替代流程）：
- 2a. 选择管理问卷任务
    1. 问卷部分只显示自己发布的问卷任务
- 3a. 点击已发布按钮
	1. 显示当前用户已发布的所有任务
- 5a. 点击列表项下拉菜单选择取消任务
	1. 放弃完成已领取的该任务
	2. 该快递任务可重新被其他人领取
- 5b. 点击列表项下拉菜单选择完成任务
	1. 该任务状态变成已完成
	2. 在所有快递任务列表中删除，已完成任务不能被再次领取
	3. 收到完成报酬

### 活动图
![](pictures/6.2.4.PNG)


## 管理个人信息
### 简要说明
- 用例名称：管理个人信息
- 相关需求：用户查询自己个人信息或更改信息及密码等
- 参与者：用户
- 前置信息：用户已成功登录，显示该用户信息
- 后置信息：显示更新后信息

### 事件流
#### 主成功场景（或基本流程）：
1. 进入个人信息界面查看当前个人信息
2. 点击修改个人信息输入要修改的信息
3. 点击提交信息，将修改内容提交
4. 提交后自动回到个人信息显示页面显示更新后信息
5. 点击修改密码进入修改界面
6. 输入当前登录密码
7. 若原密码正确，继续输入新密码并确认新密码
8. 点击提交密码修改登录密码

#### 扩展（或替代流程）：

- 3a. 填写待修改内容后点击取消
	1. 已填写的待修改内容不保存，下次进入重新填写
	2. 未能成功更新信息，返回个人信息显示界面，信息仍为最后一次修改成功的信息
- 6a. 输入当前密码错误
	1. 修改密码失败
	2. 重新输入正确原密码
- 7a. 新密码与确认密码不一致
	1. 修改密码失败
	2. 重新输入新密码并确认
- 8a. 填写修改内容后点击取消
	1. 修改密码失败，已填写内容不保存
	2. 返回个人信息显示界面

### 活动图
![](pictures/6.2.5.PNG)

以下为整个系统活动图
![](pictures/6.2.6.PNG)