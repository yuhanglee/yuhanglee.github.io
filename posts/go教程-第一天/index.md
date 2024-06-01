# Go教程-第一天




借鉴[官方教程](http://docscn.studygolang.com/doc/tutorial/getting-started)，编写合适基础开发者的Go语言教程。



&lt;!--more--&gt;

作者是由 `C语言开发者` 入门 `Go语言`，中间是经历了一个语言的切换过程。事情的起由是需要一个嵌入式的配置平台，计划使用桌面开发框架 `Qt`/`Electron`/`.Net`之类的，之前也使用过这些编写过小工具，语言集成度，完善度都是不错的。但是，软件需要拷贝，每次升级之后，都需要在各个系统平台上进行测试，且面临着跨平台需求。所以，本次选用了`Web平台`，搭建到局域网内，每个用户只需要远程登陆网址就可以，减少团队内部更新软件不便，且只需要维护一个软件就可以完成跨平台操作。


好了，今天开始我们的第一章教程吧。


# Go 环境配置

Go环境配置包括 **安装GO** ， **配置环境变量**， **编写第一个程序**。

## 安装Go

安装Go要按照 [官方步骤](http://docscn.studygolang.com/doc/install) 进行安装。

## 使用Go

在安装完成之后，可以查看一下Go安装是否正常。

``` shell
C:\Users\admin&gt;go version
go version go1.21.5 windows/amd64

C:\Users\admin&gt;
```


接下来，就可以编写自己的程序了。我在 win10 下使用 VSCode 进行程序编写，你可以使用其他的编辑器或IDE。

1. 创建一个hello.go文件，用来编写示例代码。

```shell
&gt; mkdir hello
&gt; cd hello
```
2. 创建依赖项。

```shell
&gt; go mod init example.com/hello
go: creating new go.mod: module example.com/hello
```

3. 编写第一行go代码，输出`Hello, World!`。

```go
package main

import &#34;fmt&#34;

func main() {
    fmt.Println(&#34;Hello, World!&#34;)
}
```
4. 运行程序。
```shell
&gt; go run .
Hello, World!
```

## go 帮助文档

`go run`是我们开发`go`使用最多的公式之一。除了 `go run` 之外，`go`还支持其他的命令和参数，如我们刚才使用过的`mod`，`version`。其支持的命令和参数，可以使用 `go help`进行查看。

```shell
C:\Users\admin&gt;go help
Go is a tool for managing Go source code.

Usage:

        go &lt;command&gt; [arguments]

The commands are:

        bug         start a bug report
        build       compile packages and dependencies
        clean       remove object files and cached files
        doc         show documentation for package or symbol
        env         print Go environment information
        fix         update packages to use new APIs
        fmt         gofmt (reformat) package sources
        generate    generate Go files by processing source
        get         add dependencies to current module and install them
        install     compile and install packages and dependencies
        list        list packages or modules
        mod         module maintenance
        work        workspace maintenance
        run         compile and run Go program
        test        test packages
        tool        run specified go tool
        version     print Go version
        vet         report likely mistakes in packages

Use &#34;go help &lt;command&gt;&#34; for more information about a command.

Additional help topics:

        buildconstraint build constraints
        buildmode       build modes
        c               calling between Go and C
        cache           build and test caching
        environment     environment variables
        filetype        file types
        go.mod          the go.mod file
        gopath          GOPATH environment variable
        gopath-get      legacy GOPATH go get
        goproxy         module proxy protocol
        importpath      import path syntax
        modules         modules, module versions, and more
        module-get      module-aware go get
        module-auth     module authentication using go.sum
        packages        package lists and patterns
        private         configuration for downloading non-public code
        testflag        testing flags
        testfunc        testing functions
        vcs             controlling version control with GOVCS

Use &#34;go help &lt;topic&gt;&#34; for more information about that topic.
```




---

> 作者:   
> URL: https://yuhanglee.github.io/posts/go%E6%95%99%E7%A8%8B-%E7%AC%AC%E4%B8%80%E5%A4%A9/  

