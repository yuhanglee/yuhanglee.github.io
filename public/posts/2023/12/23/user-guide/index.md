# 用户指南


FixIt 支持的Markdown语法。


<!--more-->



# 普通标题

共分为6个等级，可以进行调节。`#`的等级最高，`######`的等级最低。可以按照标题位置，生成目录。需要打开 `toc: true` 功能。

``` c

# h1 标题
## h2 标题
### h3 标题
#### h4 标题
##### h5 标题
###### h6 标题
```

# h1 标题
## h2 标题
### h3 标题
#### h4 标题
##### h5 标题
###### h6 标题

# 水平线

可以使用以下几种方式进行，符号为英文状态下的半角字符：
- `<br>`: 原生 `HTML` 方式
- `___` : 三个连续下划线
- `---` : 三个连续短横线
- `***` : 三个连续的星号

### `<br>`
<br>

### `___`
___

### `---`
---

### `***`
***


# 加粗
带有较粗字体的文本片段

```markdoen

**粗体**

__粗体__

```

> 需要注意的是，星号/下划线和文本之间是没有空格的

输出： 

**粗体**

__粗体__




# 斜体

```markdoen

*斜体*

_斜体_

```

> 需要注意的是，星号/下划线和文本之间是没有空格的

输出： 

*斜体*

_斜体_


# 删除线

```markdown
~~这段文本带有删除线。~~
```


呈现的输出效果如下：

~~这段文本带有删除线。~~



# 任务列表

```markdown
- [x] Write the press release
- [ ] Update the website
- [ ] Contact the media
```


- [x] Write the press release
- [ ] Update the website
- [ ] Contact the media



# 表格

```markdown
| Option | Description |
| ------ | ----------- |
| data   | path to data files to supply the data that will be passed into templates. |
| engine | engine to be used for processing templates. Handlebars is the default. |
| ext    | extension to be used for dest files. |
```

> 注意，竖线不需要垂直对齐。

| Option | Description |
| ------ | ----------- |
| data   | path to data files to supply the data that will be passed into templates. |
| engine | engine to be used for processing templates. Handlebars is the default. |
| ext    | extension to be used for dest files. |


# 链接

```markdown
<hhtp://www.baidu.com>
<123456@qq.com>
[百度](http://www.baidu.com)
[百度](http://www.baidu.com "这是一个标题")
```

<hhtp://www.baidu.com>

<123456@qq.com>

[百度](http://www.baidu.com)

[百度](http://www.baidu.com "这是一个标题")


# 图片

```markdown

![Minion](https://octodex.github.com/images/minion.png)

![Alt text](https://octodex.github.com/images/stormtroopocat.jpg "The Stormtroopocat")

```

![Minion](https://octodex.github.com/images/minion.png)

![Alt text](https://octodex.github.com/images/stormtroopocat.jpg "The Stormtroopocat")



**以下是markdown的扩展语法**


# Emoji支持

```markdown
去露营啦！:tent: 很快就回来。

真开心！:joy:

```

输出效果

去露营啦！:tent: 很快就回来。

真开心！:joy:


> 全部 Emoji 表情，可以参考 [FixIt 支持的 Emoji 表情](https://fixit.lruihao.cn/zh-cn/guides/emoji-support/#%E8%A1%A8%E6%83%85%E4%B8%8E%E6%83%85%E6%84%9F)


# 数学公式

FixIt 支持 [KaTeX](https://katex.org/) 数学公式。

有一份 KaTeX中支持的 [KaTex函数](https://katex.org/docs/supported.html) 清单。


## 行内公式

```markdown
{{< raw >}}行内公式：\(\mathbf{E}=\sum_{i} \mathbf{E}_{i}=\mathbf{E}_{1}+\mathbf{E}_{2}+\mathbf{E}_{3}+\cdots\){{< /raw >}}

{{< raw >}}
公式块：
\[ a=b+c \\ d+e=f \]
{{< /raw >}}
```
{{< raw >}}行内公式：\(\mathbf{E}=\sum_{i} \mathbf{E}_{i}=\mathbf{E}_{1}+\mathbf{E}_{2}+\mathbf{E}_{3}+\cdots\){{< /raw >}}

{{< raw >}}
公式块：
\[ a=b+c \\ d+e=f \]
{{< /raw >}}



# 内置ShortCodes

Hugo 提供了多个内置的 Shortcodes, 以方便作者保持 Markdown 内容的整洁。

Hugo 使用 Markdown 为其简单的内容格式。但是，Markdown 在很多方面都无法很好地支持。你可以使用纯 HTML 来扩展可能性。

但这恰好是一个坏主意。大家使用 Markdown, 正是因为它即使不经过渲染也可以轻松阅读。应该尽可能避免使用 HTML 以保持内容简洁。

为了避免这种限制，Hugo 创建了 shortcodes。 shortcode 是一个简单代码段，可以生成合理的 HTML 代码，并且符合 Markdown 的设计哲学。

Hugo 附带了一组预定义的 shortcodes, 它们实现了一些非常常见的用法。 提供这些 shortcodes 是为了方便保持你的 Markdown 内容简洁。


<!-- 
{{< gist spf13 7896402 >}} -->

{{< highlight html >}}
<section id="main">
    <div>
        <h1 id="title">{{ .Title }}</h1>
        {{ range .Pages }}
            {{ .Render "summary"}}
        {{ end }}
    </div>
</section>
{{< /highlight >}}


## style

``` markdown
\{\{\< style "text-align:right; strong{color:#00b1ff;}" \>\}\}
This is a **right-aligned** paragraph.
\{\{\< /style \>\}\}
```


{{< style "text-align:right; strong{color:#00b1ff;}" >}}
This is a **right-aligned** paragraph.
{{< /style >}}



## link

卡片式链接

``` markdown raw
\{\{\< link href="https://github.com/hugo-fixit/FixIt" content="FixIt Theme" title="source of FixIt Theme" card=true \>\}\}
```

{{< link href="https://github.com/hugo-fixit/FixIt" content="FixIt Theme" title="source of FixIt Theme" card=true >}}


## admonition

> 用法
> \{\{\< admonition type [title] [open] \>\}\}

{{< admonition type=tip title="This is a tip" open=false >}}
一个 **技巧** 横幅
{{< /admonition >}}
或者
{{< admonition tip "This is a tip" false >}}
一个 **技巧** 横幅
{{< /admonition >}}


## Echarts


``` TOML

\{\{\< echarts \>\}\}
[title]
text = "折线统计图"
top = "2%"
left = "center"

[tooltip]
trigger = "axis"

[legend]
data = [
  "邮件营销",
  "联盟广告",
  "视频广告",
  "直接访问",
  "搜索引擎"
]
top = "10%"

[grid]
left = "5%"
right = "5%"
bottom = "5%"
top = "20%"
containLabel = true

[toolbox]
[toolbox.feature]
[toolbox.feature.saveAsImage]
title = "保存为图片"

[xAxis]
type = "category"
boundaryGap = false
data = [
  "周一",
  "周二",
  "周三",
  "周四",
  "周五",
  "周六",
  "周日"
]

[yAxis]
type = "value"

[[series]]
name = "邮件营销"
type = "line"
stack = "总量"
data = [
  120.0,
  132.0,
  101.0,
  134.0,
  90.0,
  230.0,
  210.0
]

[[series]]
name = "联盟广告"
type = "line"
stack = "总量"
data = [
  220.0,
  182.0,
  191.0,
  234.0,
  290.0,
  330.0,
  310.0
]

[[series]]
name = "视频广告"
type = "line"
stack = "总量"
data = [
  150.0,
  232.0,
  201.0,
  154.0,
  190.0,
  330.0,
  410.0
]

[[series]]
name = "直接访问"
type = "line"
stack = "总量"
data = [
  320.0,
  332.0,
  301.0,
  334.0,
  390.0,
  330.0,
  320.0
]

[[series]]
name = "搜索引擎"
type = "line"
stack = "总量"
data = [
  820.0,
  932.0,
  901.0,
  934.0,
  1290.0,
  1330.0,
  1320.0
]
\{\{\< /echarts \>\}\}
```

{{< echarts >}}
[title]
text = "折线统计图"
top = "2%"
left = "center"

[tooltip]
trigger = "axis"

[legend]
data = [
  "邮件营销",
  "联盟广告",
  "视频广告",
  "直接访问",
  "搜索引擎"
]
top = "10%"

[grid]
left = "5%"
right = "5%"
bottom = "5%"
top = "20%"
containLabel = true

[toolbox]
[toolbox.feature]
[toolbox.feature.saveAsImage]
title = "保存为图片"

[xAxis]
type = "category"
boundaryGap = false
data = [
  "周一",
  "周二",
  "周三",
  "周四",
  "周五",
  "周六",
  "周日"
]

[yAxis]
type = "value"

[[series]]
name = "邮件营销"
type = "line"
stack = "总量"
data = [
  120.0,
  132.0,
  101.0,
  134.0,
  90.0,
  230.0,
  210.0
]

[[series]]
name = "联盟广告"
type = "line"
stack = "总量"
data = [
  220.0,
  182.0,
  191.0,
  234.0,
  290.0,
  330.0,
  310.0
]

[[series]]
name = "视频广告"
type = "line"
stack = "总量"
data = [
  150.0,
  232.0,
  201.0,
  154.0,
  190.0,
  330.0,
  410.0
]

[[series]]
name = "直接访问"
type = "line"
stack = "总量"
data = [
  320.0,
  332.0,
  301.0,
  334.0,
  390.0,
  330.0,
  320.0
]

[[series]]
name = "搜索引擎"
type = "line"
stack = "总量"
data = [
  820.0,
  932.0,
  901.0,
  934.0,
  1290.0,
  1330.0,
  1320.0
]
{{< /echarts >}}


## mapbox

``` TOML
\{\{\< mapbox lng=113.953277 lat=22.559102 zoom=11 \>\}\}
```

呈现的输出效果如下：
{{< mapbox lng=-122.252 lat=37.453 zoom=10 marked=false light-style="mapbox://styles/mapbox/streets-zh-v1" >}}


## MUSIC

```
music auto="https://music.163.com/#/playlist?id=60198"
```
{{< music auto="https://music.163.com/#/playlist?id=60198" >}}


## bilibili

```
https://www.bilibili.com/video/BV1Sx411T7QQ

bilibili id=BV1Sx411T7QQ
```
{{< bilibili id=BV1Sx411T7QQ >}}

---

> 作者: <no value>  
> URL: https://yuhanglee.github.io/posts/2023/12/23/user-guide/  

