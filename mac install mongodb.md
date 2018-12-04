1.安装
brew install mongodb
安装默认目录：/usr/local/Cellar/mongodb
2.在根目录下，创建默认db
~~~
cd /
sudo mkdir -p /data/db
~~~
当前目录给当前用户(tom)加权限
~~~
sudo chown -R tom /data
~~~

3.修改环境变量
把mongodb / bin加入$ PATH，以免我们每次输入sudo monogd，变成直接monogd
~~~
cd ~
vim .base_profile
~~~
内容如下：
~~~
export MONGO_PATH=/usr/local/Cellar/mongodb
export PATH=$PATH:$MONGO_PATH/bin
~~~

4.启动的MongoDB服务端

~~~
# tom @ tom-pc in ~ [15:54:04]
$ mongod
~~~
5.启动客户端shell

~~~
# tom @ tom-pc in ~ [15:46:37]
$ mongo
MongoDB shell version v4.0.4
connecting to: mongodb://127.0.0.1:27017
~~~
测试:
~~~

> show dbs
admin   0.000GB
config  0.000GB
local   0.000GB
>
~~~


总结：
mongod：用来连接到mongodb数据库服务器的，即服务器端
mongo：是用来启动MongoDB shell，是mongodb的命令行客户端。
