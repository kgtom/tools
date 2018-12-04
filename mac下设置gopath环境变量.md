

## 1.bash_profile
编辑当前用户目录下(cd ~)，vi ~/.bash_profile文件，添加以下代码
~~~
# tom @ tom-pc in ~ [17:52:47]
$ cd ~

# tom @ tom-pc in ~ [21:36:47]
$ vi ~/.bash_profile
~~~

~~~
export GOPATH=/Users/tom/goprojects
export GOBIN=$GOPATH/bin
export PATH=$PATH:$GOBIN
~~~

保存，然后source 则立即生效
~~~
source ~/.bash_profile
~~~

## 2.Zsh

编辑当前用户目录下(cd ~), vi ~/.zshrc文件，添加以下代码

~~~
export GOPATH=/Users/tom/goprojects
export GOBIN=$GOPATH/bin
export PATH=$PATH:$GOBIN
~~~

保存，然后source 则立即生效
~~~
source ~/.zshrc
~~~
