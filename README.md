# Tipask问答系统开发日志

## 记录Tipask问答系统各种操作

项目地址：https://www.xszzr.com ( `业余时间折腾的工作用网站` `请各路大神发过小站` `谢谢`)

### tipask安装操作

* [Lnmp安装tipask-解决500问题-安装fileinfo扩展](https://www.baoxian.im/wiki/Lnmp安装tipask-解决500问题-安装fileinfo扩展)

* [Nginx+PHP框架laravel状态码500错误解决](https://blog.51cto.com/13155232/2073722)
### 后台设置

* [Tipask3.0用户登陆Oauth2.0整合教程](https://wenda.tipask.com/article/40)

**回调地址** QQ互联的后台 和 tipask后台 都是： http://你的问答域名/oauth/qq/callback

#### 安装xunsearch

cd /usr/local

sudo wget http://www.xunsearch.com/download/xunsearch-full-latest.tar.bz2

sudo tar -xjf xunsearch-full-latest.tar.bz2

ls

cd xunsearch-full-1.4.10

sudo sh setup.sh

配置开机启动

sudo vi /etc/rc.d/rc.local   //本地服务器才加sudo

/usr/local/xunsearch/bin/xs-ctl.sh restart  // 加入这一条命令到启动项

sudo chmod +x /etc/rc.d/rc.local   //权限

参看文章：http://www.liaofangping.com/69.html

## 缓存优化 ##

* config/session.php

'driver' => 'memcached',

/*20190809'driver' => env('SESSION_DRIVER', 'file'),*/

* config/cache.php

'default' => 'memcached',

/*20190809'default' => env('CACHE_DRIVER', 'file'),*/

参考文章：https://wenda.tipask.com/article/5168




