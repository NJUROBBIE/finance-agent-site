# 金融多智能体通信 · 研究简报

一个可直接用于 GitHub Pages 的中文静态网页，用于展示金融多智能体与信息传输研究构想。

## 文件

```text
index.html   网页正文、样式及少量交互（全部在一个文件中）
.nojekyll    跳过 Jekyll 处理
README.md   本说明
```

无框架、无构建步骤、无第三方字体或脚本依赖。正文离线可读；访问论文链接时需要网络。页面支持电脑与手机，手机端的对照表会改为纵向信息块。

## 本地打开

直接用浏览器打开 `index.html`。

也可以在当前文件夹执行以下命令，然后在浏览器访问 `http://localhost:8000`：

```bash
python -m http.server 8000
```

Windows 用户也可以使用 `py -m http.server 8000`。按 Ctrl+C 停止服务。

## 发布到 GitHub Pages

1. 新建一个 GitHub 仓库，例如 `finance-agent-research`。使用 GitHub Free 时，将仓库设为 **Public**。
2. 解压压缩包，把 **index.html 放在仓库根目录**，不要只上传压缩包，也不要让它藏在额外一层文件夹内。可以使用仓库页面的 **Add file → Upload files**；一并上传 README.md 与 .nojekyll，提交到 `main` 分支。
3. 打开仓库 **Settings → Pages**。
4. 在 **Build and deployment → Source** 选择 **Deploy from a branch**。
5. 选择分支 **main**、文件夹 **/ (root)**，点击 **Save**。
6. 部署成功后，在同一页面点击 **Visit site** 查看公开网址。若仓库名为 `finance-agent-research`，项目网站通常形如：

```text
https://你的GitHub用户名.github.io/finance-agent-research/
```

这是项目站点，不要求把仓库命名为 `用户名.github.io`。`.nojekyll` 是一个空的隐藏文件；上传界面没有显示它时，也可以在仓库中另建这个文件。对于本项目的普通 HTML，它不是阅读页面所必需的。

## 已发布站点

- 在线访问：https://njurobbie.github.io/finance-agent-site/
- GitHub 仓库：https://github.com/NJUROBBIE/finance-agent-site
- 发布源：`main` 分支的根目录。推送更新后，GitHub Pages 会自动重新部署。

仓库和网页均公开可见。

GitHub 官方说明（核对于 2026-09-22）：
- 创建站点：https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site
- 配置发布源：https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

## 修改内容

用文本编辑器打开 `index.html`，找到标注为 `01` 至 `04` 的 HTML 注释，即可修改对应章节。标题和简介在 `hero` 区域；文献在 `references` 区域；配色在页面开头的 `:root` 变量中。

正文与论文来源分开展示：原系统和通信方法均附原始论文链接；金融任务与通信形式的对应关系、研究路线及实验设计是拟议方案，不是已完成实验的结论。页面没有虚构成绩、统计图或收益率。

## 页面功能

- 顶部章节导航和阅读位置提示；
- 手机、平板和电脑的响应式排版；
- 文献区折叠与引用定位；
- 页脚“打印 / 保存为 PDF”调用浏览器打印功能；
- 无跟踪脚本、无登录、无后台、无外部页面资源请求。

关闭 JavaScript 后仍可阅读正文、使用锚点和访问论文；阅读位置提示与打印按钮属于可选增强功能。
