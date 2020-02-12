## 简介
    Markdown 的语法全由一些符号所组成，易读易写。
    Markdown 语法的目标是：成为一种适用于网络的书写语言。
    Markdown 语法受到一些既有 text-to-HTML 格式的影响，包括 Setext、atx、Textile、      reStructuredText、Grutatext 和 EtText，而最大灵感来源其实是纯文本电子邮件的格式。
## 为什么选择Markdown
    方便、快捷、易读易写
## 语法
* *标题*
```
    有多种表示方法：

    1.  Html表达

            <h1>This is an H1</h1>
            <h2>This is an H2</h2>
    
    2. （推荐）类 Atx 形式则是在行首插入1到6 个#，对应到标题1到6阶，空格后加标题内容，为了美观可以在标题内容后再次加空格还有#

            # This is an H1
            ## This is an H2
            ### This is an H3 ###
            ###### This is an H6

    3.  类 Setext 形式是用底线的形式，利用 = （最高阶标题）和 - （第二阶标题）

            This is an H1
            =============
            This is an H2
            ---------------------
```
* *强调*
```
    Markdown 使用星号（*）和底线（_）作为标记强调字词的符号
    被 * 或 _ 包围的字词会被转成用 <em> 标签包围，用两个 * 或 _ 包起来的话，则会被转成 <strong>

    但是如果你的 * 和 _ 两边都有空白的话，它们就只会被当成普通的符号。

    如果要在文字前后直接插入普通的星号或底线，你可以用反斜线：
    \*this text is surrounded by literal asterisks\*
```

*  *引用*
```
    Markdown 标记区块引用是使用类似 email 中用 > 的引用方式。
    引用的区块内也可以使用其他的 Markdown 语法，包括标题、列表、代码区块等
    Markdown 也允许只在整个段落的第一行最前面加上 > 

    > ## 这是引用块标题
    >   有序列表
    >   1. 列表1
    >   2. 列表2
    > 
    >   无序列表
    >   * 列表3
    >   * 列表4
    > > 引用内的引用
    >
    > 代码块
    > ```
    >  System.out.println("Hello World!");
    > ```
```
效果如下
> ## 这是引用块标题
>   有序列表
>   1. 列表1
>   2. 列表2
> 
>   无序列表
>   * 列表3
>   * 列表4
> > 引用内的引用
>
> 代码块
> ```
>  System.out.println("Hello World!");
> ```
* *序列表*
```
    无序列表使用星号、加号或是减号作为列表标记，空格分隔：
    * 序列1
    * 序列2
    有序列表则使用数字接着一个英文句点，空格分隔：
    1. 序列3
    2. 序列4
    列表项目可以包含多个段落，每个项目下的段落都必须缩进 4 个空格或是 1 个制表符
    列表项目内也可以使用其他的 Markdown 语法，包括标题、列表、代码区块等
```
效果如下
 * 序列1
 * 序列2
1. aaa
2. bbb

* *代码块区*
```
    使用 四个缩进空格 或 ``` 表示代码块。
    代码区块中，一般的 Markdown 语法不会被转换，像是星号便只是星号，这表示你可以很容易地以      Markdown 语法撰写 Markdown 语法相关的文件。
```
* *行内代码块*
```
    使用 `包裹`  表示行内代码块。
```
  这是一个行内代码块，`System.out.println("Hello World!");`

* *分割线*
```
用三个以上的星号、减号、底线来建立一个分隔线，行内不能有其他东西
```
效果如下
***
* *链接*
```
    Markdown 支持两种形式的链接语法： 行内式和参考式两种形式。
    不管是哪一种，链接文字都是用 [方括号] 来标记。

    行内式：只要在方块括号后面紧接着圆括号并插入网址链接即可，如果你还想要加链接的 title 文字，只要在网址后面，用双引号把 title 文字包起来即可，例如：

            This is [an example](http://example.com/ "Title") inline link.
            [This link](http://example.net/) has no title attribute.

            如果你是要链接到同样主机的资源，你可以使用相对路径：
            See my [About](/about/) page for details.   

    参考式：方括号内既是描述也是id，

            This is [an example] reference-style link.

            接着，在文件的任意处，你可以把这个标记的链接内容定义出来
            [an example]: http://example.com/  "Optional Title Here"

            链接内容定义的形式为：
            方括号（前面可以选择性地加上至多三个空格来缩进），里面输入链接文字
            接着一个冒号
            接着一个以上的空格或制表符
            接着链接的网址
            选择性地接着 title 内容，可以用单引号、双引号或是括弧包着
            请注意：有一个已知的问题是 Markdown.pl 1.0.1 会忽略单引号包起来的链接 title。不建议使用

            I get 10 times more traffic from [Google]  than from [Yahoo]  or [MSN] .

            [Google]: http://google.com/        "Google"
            [Yahoo]: http://search.yahoo.com/  "Yahoo Search"
            [MSN]: http://search.msn.com/    "MSN Search"
```
效果如下

This is [an example](http://example.com/ "Title") inline link.
 [This link](http://example.net/) has no title attribute.

I get 10 times more traffic from [Google]  than from [Yahoo]  or [MSN] .

  [Google]: http://google.com/        "Google"
  [Yahoo]: http://search.yahoo.com/  "Yahoo Search"
  [MSN]: http://search.msn.com/    "MSN Search"

  * *图片*
  ```
        Markdown 使用一种和链接很相似的语法来标记图片，同样也允许两种样式： 行内式和参考式。
        行内式的图片语法看起来像是：
        ![Alt text](/path/to/img.jpg)

        ![Alt text](/path/to/img.jpg "Optional title")

        详细叙述如下：
            一个感叹号 !
            接着一个方括号，里面放上图片的替代文字
            接着一个普通括号，里面放上图片的网址
            最后还可以用引号包住并加上选择性的 'title' 文字。

            参考式的图片语法则长得像这样：
                   ![Alt text][id]
                   [id]是图片参考的名称，图片参考的定义方式则和链接参考一样：
                   [id]: url/to/image  "Optional title attribute"

  ```
* *自动链接*
```
    Markdown 支持以比较简短的自动链接形式来处理网址和电子邮件信箱，只要是用尖括号包起来， 
    Markdown 就会自动把它转成链接。一般网址的链接文字就和链接地址一样，例如：
    <http://example.com/>
```
  链接：<https://clongulin.website>

  邮箱：<abc@gmail.com>
* *反斜杠*
```
Markdown 可以利用反斜杠来插入一些在语法中有其它意义的符号
例如：如果你想要用星号加在文字旁边的方式来做出强调效果（但不用 <em> 标签）

Markdown 支持以下这些符号前面加上反斜杠来帮助插入普通的符号：
        \   反斜线
        `   反引号
        *   星号
        _   底线
        {}  花括号
        []  方括号
        ()  括弧
        #   井字号
        +   加号
```
  \*Good Bye\*
