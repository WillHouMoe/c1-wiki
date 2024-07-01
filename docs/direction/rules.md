# 编写规则

本文介绍了为本站编写内容的流程和注意事项。

由于经费不足，我们无法使用云服务器搭建网站，只能使用免费的 GitHub Actions。这意味着更繁琐的编辑流程和更慢的访问速度（因为众所周知的原因）。当然，你可以使用一些 magic 来解决后者，但是后果自负 :upside_down_face:。

## 编辑方式 1: GitHub 直接编辑

1. 在所有页面的右上角都有一个编辑图标 :material-file-edit-outline:，单击该图标。

2. 如果你从未使用过 GitHub，它会先让你注册，按照流程走就行。

3. 注册好之后，再次点击编辑图标，跳转到 GitHub。点击 `Fork this repository`。

4. 在线更改内容

5. 单击右上角绿色图标 Commit changes，填写 Commit message（即修改概要），下面的 Extended Description 选填，最下面选择 `Commit directly to the master branch`

6. 点击 Create Pull Request

7. 再填入 Pull Request 信息即可，点击 Create Pull Request 即可。之后等待被 merge 后，你编辑的内容就会被显示在网站上。

!!! tip
    如果长时间没有被 merge 可以私信通知我(WillHou)...

如果想要创建文件：

1. 找到对应的文件夹，点击 Add file > Create new file(或者 Upload files 也行，取决于你习惯 online edit 还是 offline)

2. (以 Create new file 为例) 输入文件名（一定用**英文**，一定加上文件后缀 `.md`！！！），文件内容首行用一级标题打头。

3. 编辑好躯体内容后，点右上角 Commit Changes 即可.

4. 点击 Create pull request，后续步骤同上 6-7.

## 编辑方式 2: 人工编辑 :unamused:

实在不行的话直接按照格式发文件给我吧......