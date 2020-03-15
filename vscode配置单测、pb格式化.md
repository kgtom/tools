* 1.配置单元测试

setting—workspace Settings 里面 搜索 gopath ,找到 GoPath 选择 Edit in settings.json

~~~
{
    "go.gopath": "/Users/tom/devspace/demo",
    "go.testEnvVars": {
        "GOPATH": "/Users/tom/devspace/demo",
        "ENV_CONFIG_FILE": "/Users/tom/devspace/demo/src/apps/front/config.yaml"
    },
    "go.testFlags": [
        "-v"
        "-count=1" //禁用cached

    ]
}
~~~

* 2.配置 proto文件保存时自动格式化


第一步： brew install clang-format 或者在 vscode 安装clang-format插件
第二步：在vscode 安装 vscode-proto3 

第三步：在 setting—user Setting 里面搜索gopath ,选择 Edit in settings.json
 ~~~

{
    "workbench.colorTheme": "Visual Studio Dark",
    "go.formatTool": "gofmt",
    "go.gopath": "/Users/tom/go",
    "go.toolsGopath": "/Users/tom/go",
    "go.testTimeout": "300s",
    "window.zoomLevel": 0,
    "clang-format.executable": "/usr/local/Cellar/clang-format/2018-10-04/bin/clang-format",
    "clang-format.style": "{BasedOnStyle: WebKit, AlignConsecutiveAssignments: true}",
    "editor.formatOnSave": true,
    "extensions.ignoreRecommendations": true
}

~~~
ps： 注意查找/usr/local/Cellar/clang-format路径，确认是否是该路径2018-10-04
* 3.配置单测默认300s超时时间

在左下角 setting—>workspace setting 中输入 timeout，找到 Go configuration 修改Test timeout 值即可。
