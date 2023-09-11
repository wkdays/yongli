# Obsidian_MkDocs_Vercel

如果你，用 Obsidian 记笔记， 用vercel+mkdocs 做个人网站，用git做链接同步obsidian笔记和个人网站之间。
## 极简步骤

1. 点击 `use this template`，生成你自己的 GitHub 仓库。
2. 在 [**Vercel**](https://vercel.com/) 部署，新建项目new project，框架选择 `other`，起个网站名字如：upbu，其他不用选，默认完成。（如果还没注册 Vercel 账号，可以直接用 GitHub 账户创建一个）
3. 此刻你有个网站了，比如[http://upbu.vercel.com](https://upbu.vercel.app/)
4. <img width="1130" alt="image" src="https://github.com/squarewang007/yongli/assets/28798102/dccf01ad-62d1-4c8c-98b7-09f62402c06d">
6. 下载 Obsidian 软件，在设置里，设置库（Vault）的位置为git clone到本地的docs文件夹，这个文件夹就是网站首页的目录，也是obsidian的库文件目录。
7. 还要解决一个问题，安装obsidian git插件，这样可以自动同步到git上。然后从git上同步到vercel网站上。安装后用ssh-key来链接git，否则每次都要输入密码或者链接不上。国内的网络似乎也是个问题。
8. 测试ssh git 的链接https://docs.github.com/zh/authentication/connecting-to-github-with-ssh/testing-your-ssh-connection
9. 这都是折腾为了免费。
10. 每次更新后推到 GitHub，Vercel 就会自动拉取更新，并部署网站。

## 开发者区域

根目录下各文件属性：

- `requirements.txt`：Vercel 在部署的时候会查看这个文件，检查需要的 Python 依赖并下载它们。
- `package.json`：里面包含了 MkDocs 的构建命令、要使用的 MkDocs 的版本号（默认为最新），Vercel 会用这些参数进行部署。
- `mkdocs.yml`：文件样式

## 参考与致谢

- [jobindj/obsidian-publish-mkdocs](https://github.com/jobindj/obsidian-publish-mkdocs)
- [MkDocs Material](https://squidfunk.github.io/mkdocs-material/)
