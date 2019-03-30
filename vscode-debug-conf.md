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
