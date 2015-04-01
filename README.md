
注：《nodejs 开发指南》pdf 下载地址： http://download.csdn.net/download/therbetter/5126235

原教程将 db.js post.js  user.js settings.js放 node_modules， 对于上传至github不妥， 已将其路径改为：“public/js/dao”，
而 node_modules 内容， 下载该代码后， 请自行 npm install 之。


PS:
1.安装 Mongodb后，运行代码前 需要cmd 启动数据库服务。

2.可视化操作Mongodb， 建议使用 “MongoVUe”。

=====
#### 本地部署（win7 64bit为例）：

* 确保本地已安装 git 以及 node 环境，在某文件夹 右键-》“git bash” 运行:
```Bash
git clone https://github.com/wteam-xq/microBlog.git`
```
* 运行cmd 进入“microBlog”文件夹， 运行 `npm install`安装依赖模块
* 安装mongodb（最好配置成window服务），生成globalDb数据库、生成users表
  * 手动安装mongodb, 下载地址： [mongodb下载](http://pan.baidu.com/s/1qWG5Lr2)
  * mongodb 配置以及设置成windows服务：[配置mongodb](http://blog.csdn.net/liusong0605/article/details/10574863)
  * mongodb shell 控制台使用: [mongodb 基本命令](http://www.cnblogs.com/xusir/archive/2012/12/24/2830957.html)
```Bash
mongo
MongoDB shell version: 2.6.5
connecting to: test

use microblog
switched to db microblog

db.createCollection("users")
{ "ok" : 1}

```
* 进入 “microBlog”文件夹启动项目: cmd运行 `npm start` (或 进入bin `node www`)
* 打开浏览器（建议 chrome）输入： `localhost:300`(端口号在 bin/www 文件中设置)

