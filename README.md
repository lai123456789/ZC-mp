# 成氏商城小程序备注

### 开发框架
[WePY](https://tencent.github.io/wepy/)

<<<<<<< HEAD
### 小程序框架wepy 使用手册：
=======
### 使用
>>>>>>> e6f43a271270e992ccd8557dd85f9e9f1a72bfef
```js
# 如果电脑未安装node环境，必须先安装配置（vue也适用）
> 安装链接：https://www.cnblogs.com/lgx5/p/10732016.html

# install dependencies（安装依赖使用以下命令）
> npm install

# dev（运行项目调试使用以下命令）
> wepy build --watch

# build（调试完成后打包，可以使用如下命令。ps：这一步可以忽略，小程序代码无需打包发布服务器）
> wepy build

```

### 错误积累
- 'wechat.code.expire': 小程序没有绑定公众平台
http://mjx-wx.natapp1.cc/swagger-ui.html#!/
http://mjx-wx.natapp1.cc

固定永久token：026ecc8e63cc47d1acbc6567f520b001
请求头格式：{Authorization:026ecc8e63cc47d1acbc6567f520b001}

### 提交小程序版本审核的问题积累总结
每次提交小程序版本之前，先自测看下即将发布提审的这个版本各个功能是否正常页面
是否正常显示：如
> 1、首页、分类、C+、购物车、我的 查看页面是否正常显示
> 2、主要测试支付功能，是否能正常下单调起支付控件完成支付
> 3、连接的地址是否为#正式地址#

#####（代码版本管理工具推荐：SourceTree或者Git Extensions，都是可视化的图形管理界面）
### 版本开发规范
##### 1.基于版本规范制定的开发分支规范。master为稳定的主版本，一旦master发布一个稳定版本后打一个tag 基于master 平行拉取出dev分支(该分支作为功能版本分支，发布后y版本升级)，并由dev分支拉取出特定的功能分支，如feature/integration-1.0分支和feature/marketing-1.o, 两个feature分支独立开发，按照既定版本进行发布并升级。feature分支开发完后，合并到dev，然后合并到master。
##### 2.基于master拉取bug分支hotfix(如当前稳定版本为1.0.0-RELASE),拉取出1.0.1,发布完成后版本升级至1.0.1。然后合并到dev和对应的feature分支 如果feature/integration-1.0开发完成发布后版本升为1.1.0。
