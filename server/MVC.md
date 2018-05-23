# 如何理解MVC
## 1.Model
负责从数据库中存取数据。

## 2.View
负责数据展示和用户交互

## 3.Controller
负责链接Model和View。用来处理业务逻辑

## 例子1：
用户提交一个表单，在View层填完数据点击提交按钮，Controller层获取到页面上所填的数据，并发送ajax请求，Module层将ajax传过来的数据存到数据库中。