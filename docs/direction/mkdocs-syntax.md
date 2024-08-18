# MkDocs 特殊语法

C1 Wiki 同时支持 Markdown 的常规语法和 MkDocs 的特殊语法。</br>
对于前者，你可以参照 [Markdown](./markdown)；</br>
而对于后者，如果你有一定的英文阅读能力，可以阅读官方文档：[MkDocs 语法官方文档](https://squidfunk.github.io/mkdocs-material/reference/)

如果你懒得读英文，那这个本页面会提供一些简单实用的语法供你学习。

## 约定

下文采用如下表达方式：

- `<xxx>`: 表示此处的参数的含义
- A/B: 表示两种选项

## 文本块 Admonitions

语法：

``` markdown title="Admonitions"

!!!/??? <type> "<title>"
    <content>

```

示例：

``` markdown title="Admonitions"

!!! success "成功"
    恭喜你，学会了一个新语法！

```

效果：

!!! success "成功"

    恭喜你，学会了一个新语法！

\* 注意：正文 `<content>` 部分，必须缩进四格（即在所有文字前加四个空格）。

`<type>` 支持下列几个参数：`note`, `abstract`, `info`, `tip`, `success`, `question`, `warning`, `failure`, `danger`, `bug`, `example`, `quote`。

## 博客

如果你此前从未在 C1 Wiki 上编辑过博客，你需要先在代码仓库中 `/docs/blog/.authors.yml` 为自己创建一个档案，格式为：

``` yaml title="_authors.yml"

authors:
  <name>: # 这里的 name 为调用用的
    name: <name_display> # 这里的 name 用于显示
    description: <description> # 随便写点
    avatar: <avatar> # 头像
    url: <personal_homepage_url> # 个人主页链接，可以是 GitHub 主页等

```

示例：

``` yaml title="_authors.yml"

authors:
  WillHou:
    name: WillHou
    description: Creator
    avatar: https://cdn.luogu.com.cn/upload/image_hosting/3afg4gyl.png
    url: https://github.com/WillHouMoe

```

配置好作者身份后，你就可以开始编辑正文了。在正文开头部分，你需要添加如下元数据：

``` markdown title="Metadata"

---
authors:
  - <author>
  - <coauthor_1>
  - <coauthor_2>
  - ...
categories:
  - <category_1>
  - <category_2>
  - ...
date:
  created: xxxx-xx-xx
  updated: xxxx-xx-xx
readtime: <read_time>
---

```

`<author>` 只需填写 `_author.yml` 文件中的 `<name>` 即可（注意：不是 `<name_display>`！</br>
`<category>` 可随便填，但建议形成习惯便于整理</br>
`<read_time>` 单位为分钟</br>
其它参数详见[官方文档](https://squidfunk.github.io/mkdocs-material/plugins/blog/#usage)。

示例：

``` markdown title="Metadata"

---
authors:
  - WillHou
categories:
  - diary
date:
  created: 2024-07-23
  updated: 2024-07-23
readtime: 3
---

```

效果见[这篇博客](./../../blog/2024/07/23/我的中考是怎样被毁掉的/)。

## 插件 glightbox 的使用

为了充分利用网页空间，我们有时候需要让图片嵌入文字显示。glightbox 插件为这项功能提供了支持。

``` markdown title="glightbox"

![<img-name>](<img-path-url>){ align=left/right(recommended) width=<width> }

```

只需这行代码即可。示例：

``` markdown title="glightbox"

![king-deer](./img/king-deer.png){ align=right width=400 }

```

效果见[这个页面](./../../meme/king-deer)