**mac 环境下 debug配置**

### 一、项目代码在gopath/src下面

#### 1. setting.json设置
~~~~
{
    "go.gopath": "/Users/tom/g",
    "go.goroot": "/usr/local/go"
}

~~~

#### 2.launch.json 设置
~~~
{
    // Use IntelliSense to learn about possible attributes.
    // Hover to view descriptions of existing attributes.
    // For more information, visit: https://go.microsoft.com/fwlink/?linkid=830387
    "version": "0.2.0",
    "configurations": [
        
        {
            "name": "Launch",
            "type": "go",
            "request": "launch",
            "mode": "debug",
            "remotePath": "",
            "port": 2345,
            "host": "127.0.0.1",
            "program": "${file}",
            "env": {
                "GOPATH":"/Users/tom/go/"
            },
            "args": [],
            "showLog": true,
           
            
        }
    ]
}
~~~

### 二、项目代码b不在gopath/src目录下

#### 1.setting.json文件

~~~
{
    "go.gopath": "/Users/tom/demo",
    "go.testEnvVars": {
        "GOPATH": "/Users/tom/demo",
        "ENV_CONFIG_FILE": "/Users/tom/demo/config/config.yaml"
    },
    "go.testFlags": [
        "-v"
    ]
}
~~~
#### 4.launch.json

~~~
{
    // Use IntelliSense to learn about possible attributes.
    // Hover to view descriptions of existing attributes.
    // For more information, visit: https://go.microsoft.com/fwlink/?linkid=830387
    "version": "0.2.0",
    "configurations": [
        {
            "name": "Launch",
            "type": "go",
            "request": "launch",
            "mode": "auto",
            "program": "${fileDirname}",
            "env": {},
            "args": []
        }
    ]
}

~~~
