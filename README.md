# 同频 · 家长学习空间

面向自闭症家庭的中文家长学习网站，包含 6 节小课、主题筛选、家庭尝试建议和浏览器内的已读进度。

## 发布到你的 myweb 仓库

1. 解压交付包，将里面的文件放到 `myweb` 仓库的最外层。`index.html` 应直接出现在仓库首页，不能放在额外的 `myweb` 或 `dist` 文件夹里面。
2. 确认 `.github/workflows/deploy-pages.yml` 也已上传。`.github` 是隐藏文件夹；在 Mac 的访达中可按 `Command + Shift + .` 显示隐藏文件。
3. 打开仓库的 **Settings → Pages**，在 **Build and deployment → Source** 选择 **GitHub Actions**。
4. 提交到 `main` 或 `master` 分支后，网站会自动发布。如果文件已经提交，再改好 Pages 设置，可到 **Actions → Deploy website to GitHub Pages → Run workflow** 手动运行一次。
5. 等待发布任务成功，在 **Settings → Pages** 中点击显示的网站地址。

未设置自定义域名时，项目网站通常为：`https://你的GitHub用户名.github.io/myweb/`。请以仓库 Pages 页面显示的实际地址为准。

如果你的发布分支既不是 `main` 也不是 `master`，请把 `.github/workflows/deploy-pages.yml` 中的 `branches` 改为实际分支名。

## 文件说明

- `index.html`：完整网站，修改内容和样式后提交即可更新。
- `.github/workflows/deploy-pages.yml`：自动发布设置。
- `.nojekyll`：支持直接发布静态网页。
- `.gitignore`：排除临时文件。

页面的样式与交互都包含在 `index.html` 中，不依赖服务器、安装程序、账号密钥或第三方字体。页内导航使用相对锚点，可在 `/myweb/` 路径下运行。

发布时只上传网页文件，说明文件和工作流配置不会进入网站发布包。此前 Sites 平台的专用配置和版本记录未包含在交付包中。

## 注意事项

- 需要有仓库设置权限，并且账号套餐支持该仓库的 GitHub Pages。免费账号通常使用公开仓库。
- 普通 GitHub Pages 网站对外可访问；不要上传孩子个人信息或其他私密资料。
- 已读进度仅保存在访问者当前浏览器；更换设备、浏览器或网站地址不会自动同步。
- 本项目尚未在你的实际仓库运行发布任务，需要完成以上仓库设置后才能上线。
- 网站内容用于家庭学习与支持，不能替代诊断或专业评估。

官方说明：[GitHub Pages 发布设置](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)
