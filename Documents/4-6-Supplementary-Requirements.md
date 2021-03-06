# 补充规格说明

### 简介

本文档记录了 “LittleMiser” 未在用例中描述的需求

### 功能性

- **安全性**：每个用户需要使用手机号码/邮箱注册
- **任务管理**
  - 一个任务只属于快递分类/问卷分类，明确管理方式
  - 增加搜索功能，方便查询
- **任务发布**
  - 目前完成用户发布任务，设置相应的报酬，其他用户接受任务，在完成任务后获得报酬的功能实现

### 可用性

- 辅助功能

  - 重点信息突出，避免使用太多杂色
  - 颜色风格统一
- 输入限制
  - 注册，登录界面增加输入检测，防止不符合规范的、无意义的输入。
  - 问卷创建页面增加输入检测，防止空问卷的建立。
- 用户体验

  - 支持接受和发布多个任务

### 可靠性

- 性能：尽量减少页面的等待时间，加载资源应当尽量的少
- 应对大量数据的处理能力：在渲染问卷或是快递列表时，要检索的信息越来越多。目前我们不需要担心这个问题，但对这一潜在的问题有所警惕。

### 实现约束

- 客户端：选择使用Web端，一种基于网页的服务形式，用户省去安装App的时间，提高用户体验；能够实现组件化、单文件开发。
- 后端框架：基于技术和业务层面的考虑，选择JavaScript作为编程语言。

### 免费开源架构

一般而言我们建议在该项目中尽可能使用开源构件。尽管现在对最终的设计选择构件为时过早，但是我们建议采用

- MongDB

### 法律问题

注册需要用户的手机号，邮箱，学号，姓名等真实信息。本平台应保护个人信息不被泄露。

>**第四十条** 网络运营者应当对其收集的用户信息严格保密，并建立健全用户信息保护制度。
>
>*选自《中华人民共和国网络安全法》*	
