# wilddog-weapp
野狗(wilddog)微信小程序客户端 (preview)

注意：
* 由于微信没有正式公开小程序，所以此版本为预览版，请不要用于正式生产环境

已知问题:
* 在微信开发者工具中会出现一定概率的不能连接野狗服务器现象
* 目前只支持数据同步部分功能，auth和用户管理相关功能并没有做支持

## 引入野狗客户端

1. 将wilddog-weapp-all.js 直接放到微信小程序的项目中
2. 使用commonjs引入
```
var wilddog = require('wilddog-weapp-all')
```
3. 初始化

```
var config = {
    syncURL:<your-app-url>
}
wilddog.initializeApp(config)
```

4. 使用 `on`，`once`,`set`,`push`,`update` 等API进行数据同步操作。
具体参考 https://docs.wilddog.com/api/sync/web/api.html
支持 Wilddog.sync 下所有的API

## DEMO

目前只写了一个粗糙的demo
https://github.com/stackOverMind/wilddog-weapp-demotodo

## contribute

非常欢迎各种形式的issue，和代码。
