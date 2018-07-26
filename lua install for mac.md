
### 1.下载、编译：
~~~
curl -R -O http://www.lua.org/ftp/lua-5.3.1.tar.gz
tar zxf lua-5.3.1.tar.gz
cd lua-5.3.1
make macosx test

~~~

### 2.安装

~~~
sudo make install

~~~

要求输入本机密码，安装完成后如下：

~~~
Password:
cd src && mkdir -p /usr/local/bin /usr/local/include /usr/local/lib /usr/local/man/man1 /usr/local/share/lua/5.3 /usr/local/lib/lua/5.3
cd src && install -p -m 0755 lua luac /usr/local/bin
cd src && install -p -m 0644 lua.h luaconf.h lualib.h lauxlib.h lua.hpp /usr/local/include
cd src && install -p -m 0644 liblua.a /usr/local/lib
cd doc && install -p -m 0644 lua.1 luac.1 /usr/local/man/man1

~~~

### 3.测试是否安装成功

~~~
# tom @ tom-pc in ~/lua-5.3.1 [16:39:59]
$ lua -v
Lua 5.3.1  Copyright (C) 1994-2015 Lua.org, PUC-Rio

~~~
