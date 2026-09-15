# Chunchun Chen 的学术主页

基于 [Marigoldwu 的主页源码](https://github.com/Marigoldwu/Marigoldwu.github.io)，沿用原来的 Jekyll 布局和样式。上游模板为 [RayeRen/acad-homepage](https://github.com/RayeRen/acad-homepage.github.io)。保留 MIT 许可证及原有版权声明。

## 当前状态

已设置姓名 Chunchun Chen（陈春春）、同济大学博士生身份、研究方向、邮箱、GitHub 和 Google Scholar 链接，并根据提供的 CV 整理了简介、论文和审稿经历。Education 已从页面和导航移除。头像仍为字母占位图，获奖信息待确认。原作者的个人图片、联系方式、统计配置和自动引用爬虫未带入本项目。页面使用英文。

## 修改内容

| 内容 | 文件 |
| --- | --- |
| 姓名、职位、研究方向、邮箱、社交链接 | `_config.yml` |
| 个人简介 | `_pages/includes/intro.md` |
| 最新动态、历史动态 | `_pages/includes/news.md` |
| 论文及项目 | `_pages/includes/pub.md` |
| 学术服务 | `_pages/includes/services.md` |
| 获奖经历 | `_pages/includes/honors.md` |
| 教育经历 | `_pages/includes/others.md` |
| 顶部导航 | `_data/navigation.yml` |
| 头像 | `images/avatar.png` |
| 论文配图 | `images/publication.png`，可新增其他文件 |

`_config.yml` 中 `null` 表示尚未设置，相关链接不会显示。请用真实资料替换占位文字后再发布。
`author.github` 只填用户名；`author.googlescholar`、`author.orcid` 填完整链接。
可复制 `pub.md` 中的 `paper-box` 区块新增论文；没有论文时可删除占位区块。

## 发布到 GitHub Pages

1. 在你的 GitHub 账号下创建公开仓库 `你的用户名.github.io`。
2. 将本目录的内容放到仓库根目录，包括以点开头的配置文件；不要把整个 `homepage` 文件夹再套一层。
3. 修改 `_config.yml` 中的 `url` 为 `https://你的用户名.github.io`，`repository` 为 `你的用户名/你的用户名.github.io`，`author.github` 为你的用户名，`baseurl` 保持空字符串。
4. 打开仓库 **Settings → Pages**，Source 选择 **Deploy from a branch**，分支选择 `main`，目录选择 `/ (root)`，保存。
5. 等待 GitHub Pages 构建完成，访问 `https://你的用户名.github.io/`。

GitHub Pages 会构建 Jekyll 源码。若仓库名称不是 `用户名.github.io`，请将 `baseurl` 改为 `/仓库名`。

## 本地开发

使用 Ruby 3.1 或更新版本与 Bundler：

```sh
bundle install
bundle exec jekyll serve --host 127.0.0.1 --port 4000
```

访问 http://127.0.0.1:4000 。修改 `_config.yml` 后需重新启动。

## 本次验证

已使用 Jekyll 3.9.5 成功构建，检查了导航锚点、图片、样式、脚本和关闭统计的配置。本机验证使用独立安装在工作目录的兼容依赖，未使用旧版 Gemfile.lock 完整安装 GitHub Pages 依赖包。
同级 `preview/index.html` 可直接在浏览器打开，是根据相同 Liquid、Markdown 和 Sass 模板生成的便携预览；编辑源码后它不会自动更新。正式发布请使用本目录中的 Jekyll 源码。

## 来源

参考仓库提交：`0f16ce62e337652ab67087d5723479973194b06e`。
本次只在本地生成文件，尚未创建远程仓库或发布网站。
