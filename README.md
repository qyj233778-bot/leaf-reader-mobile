# Leaf 拾叶 · 独立手机版

免费静态网页，可部署到 GitHub Pages。与电脑版目录、服务、数据完全独立，电脑关机后仍可使用。

- 网页仅包含程序和 Leaf 原创双语示例，没有电脑里的期刊正文、学习记录或任何密钥。
- 手机点击“同步外刊”后，直接从原 GitHub 仓库下载 EPUB，在手机解析并用 IndexedDB 保存。网络或 GitHub 额度异常时，设置页会显示错误；也可导入自己下载的 EPUB。
- 点击单词查词、收藏单词、复习、文章收藏、进度、段落与整篇翻译均在手机运行。每天更换推荐；有新刊时请同步。
- MyMemory 翻译免费但有额度。DeepSeek 从手机直连官方 API，仍按自己的账户计费。密钥只保留在 sessionStorage 会话，不写进 IndexedDB 和备份。
- 学习记录只在当前浏览器。清理网站数据会丢失记录；请在设置中导出备份。可以合并导入手机版备份或电脑版 `library.json`；导入不会覆盖手机设置或带入电脑版密钥。
- 构建时生成 Service Worker，首次联网打开并完成缓存后可离线打开程序、阅读已下载内容。添加到主屏幕的入口由手机系统决定。新翻译、查词、下载和第一次打开仍需联网。
- EPUB 只提取纯文字，原始 HTML 不执行。网站不代理期刊、不提供付费翻译额度、不自动云同步个人记录。

## 本地运行

```sh
npm install
npm run build
npm run preview
```

## 免费发布

将 `dist/` 的内容发布到一个独立的公开 GitHub 仓库，保留 `.nojekyll`，然后在仓库 **Settings → Pages → Deploy from a branch** 选择 **main / (root)**。

不需要服务器、信用卡、域名、GitHub Token 或更改电脑版。GitHub Pages 和 GitHub 源文件的实际可访问性取决于手机网络。
