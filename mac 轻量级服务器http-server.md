### 1.  安装NodeJS
brew install node
测试是否安装成功：
~~~
# tom @ tom-pc in ~ [22:17:30]
$ node -v
v9.3.0
~~~
### 2. 安装http-server
   sudo npm install http-server -g
### 3. 在允许网站目录下，输入http-server
~~~
# tom @ tom-pc in ~/goprojects/src/fs/smw_website on git:master x [22:30:32]
$ http-server
Starting up http-server, serving ./
Available on:
  http://127.0.0.1:8080
  http://192.168.31.60:8080
  http://169.254.213.95:8080
Hit CTRL-C to stop the server
~~~

### 4.访问 http://127.0.0.1:8080 即可。
