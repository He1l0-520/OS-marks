# Markdown练习

## 标题语法

井号接空格接标题文字即可，越多标题字号越小，层级越深。

## 段落语法

用空白行分割段落，并不要使用制表符和空格缩进。

## 换行语法

回车就行了🤔。

## 强调语法

### 粗体

**两星号包括即可**

### 斜体

*单星号包括即可*

### 粗斜体

***三个星号包括即可***

## 列表语法

### 有序列表

1. 有序列表这样写

2. 没错，就这样写

### 无序列表

- 无序列表这样写

- 没错，就这样写

## 引用语法

> 在段落前使用>符号
> 
> 一行空白>可以引用多行
> 
> > 多加一个>可以嵌套
> 
> #### 引用里也可以带格式
> 
> - 无序列表没问题
> - **粗体**和*斜体*也可以

## 代码语法

`使用反引号包括即可表示为代码`

``两个`反引号`可以将其转义``

    每一行都缩进4个空格以表示代码块

## 分隔线语法

空白行轻划，

---

三个连字符分界，

___

分隔线生焉。

## 链接语法

### 普通链接

[Markdown 链接语法 | Markdown 教程](https://markdown.com.cn/basic-syntax/links.html "引号里的字可以在鼠标悬停时显示")

### 网址与Email

<https://markdown.com.cn>

<fake@example.com>

### 带格式的链接

可以用粗体**[Markdown 链接语法 | Markdown 教程](https://markdown.com.cn/basic-syntax/links.html)**

可以用斜体*[Markdown 链接语法 | Markdown 教程](https://markdown.com.cn/basic-syntax/links.html)*

也可以用反引号`[Markdown 链接语法 | Markdown 教程](https://markdown.com.cn/basic-syntax/links.html)`

嘶——，这编辑器好像不支持，真可以么？🤔

### 引用链接

要显示的部分 [1]

[1]: https://markdown.com.cn/basic-syntax/links.html

## 图片语法

![这是图片](../assets/9c3cecea1a6af74c7931d88cd6b8834c2697851e.jpg "可以设置悬停文字")

[![链接图片](../assets/822b66c591c2d2e5e5965577805a1efe2cf0647c.png)](https://markdown.com.cn/basic-syntax/images.html#%E9%93%BE%E6%8E%A5%E5%9B%BE%E7%89%87 "图片也支持链接")

## 转义字符

用反斜线将格式化字符转义。

\**不用反斜线，这句话将是粗体**

## 内嵌HTML标签

有一说一，markdown虽然支持html写法，但是实在是复杂且杂糅，不太支持这么写。

## 表格

| 用三个连字符                                                                                                                                      | 创建   | 表头       |
|:------------------------------------------------------------------------------------------------------------------------------------------- |:----:| --------:|
| 用管道符                                                                                                                                        | 分隔   | 每列       |
| 连字符左右加冒号                                                                                                                                    | 进行   | 对齐       |
| [链接](https://markdown.com.cn/extended-syntax/tables.html#%E6%A0%BC%E5%BC%8F%E5%8C%96%E8%A1%A8%E6%A0%BC%E4%B8%AD%E7%9A%84%E6%96%87%E5%AD%97) | `代码` | ***强调*** |
| 用`&#124;`                                                                                                                                   | 表示   | 竖线（存疑）   |

## 围栏式代码块

```c
printf("三个反引号可以创建围栏式代码块，在反引号旁指定语言后还能显示语法高亮\n")
```

## 脚注

方括号里添加尖号与标识符[^标识符]

[^标识符]: 可以将另一个有冒号的连接起来

## 标题编号

### 这样写 {#custom-id}

[可以用这样的链接跳转到对应的标题](Markdown练习.md#custom-id)

## 定义列表

这个列表
: 干什么用的
这个写法
: 没看懂
: 好像编辑器也不支持

## 删除线

~~不会写删除线。~~用两个波浪线包括即可。

## 任务列表

- [ ] 先写无序列表

- [ ] 再在前面写中括号

- [ ] 括号里面加空格

- [ ] 括号后面加空格

- [ ] 最后写事项

- [x] 完成后把括号里的空格换成叉

## Emoji

➡️✍️😄

直接写就行

## 禁止自动链接

`http://www.example.com`
