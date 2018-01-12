yigu-china.com-2018
=============

毅固防滑中文官网2018年版


域名绑定、301转向及nginx配置
-----

新建配置文件: ``sudo nano /etc/nginx/sites-available/yigu-china.com``

编辑配置文件及保存: 

    server {
        server_name yigu-china.com;
        return 301 http://www.yigu-china.com$request_uri;
    }
    server {
        server_name www.yigu-china.com;
        index index.html;
        root /srv/yigu-china.com-2018/_site;
        error_page 404 /Error.html;
    }

建立链接: ``sudo ln -s /etc/nginx/sites-available/yigu-china.com /etc/nginx/sites-enabled/``

重启nginx: ``sudo service nginx restart``


下载及生成网站
-----

1. 下载网站源码: ``git clone git://github.com/zackwong/yigu-china.com-2018.git``

2. 进入源码根目录: ``cd yigu-china.com-2018``

3. 生成网站: ``jekyll build``


开发者
---------

* Zack Wong &lt;hzzzoo@126.com&gt;

