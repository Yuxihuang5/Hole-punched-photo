# 小Pen设计-打孔机照片

这是可直接部署到 GitHub Pages 的完整静态网站包。无需 Python、Node 或后端服务。

## 上传与发布

1. 解压 ZIP，把包内文件上传到 GitHub 仓库根目录。根目录应直接看到 `index.html` 和 `assets`，不要再多套一层文件夹。
2. 一并上传 `.github/workflows/pages.yml` 与 `.nojekyll`。点开文件夹看不到 `.github` 时，macOS 可按 `Command + Shift + .` 显示隐藏文件。
3. 打开仓库 **Settings → Pages → Build and deployment → Source**，选择 **GitHub Actions**。
4. 提交到 `main` 分支后，打开 **Actions** 查看部署进度；成功后在 **Settings → Pages** 里打开网站地址。

不使用自动工作流也可以：在 Pages 设置里选 **Deploy from a branch → main → /(root)**，保存。网站无需构建，直接发布根目录即可。

## 使用

- 右上角上传照片；点击作品重新随机布局、大小、底色与英文词。
- 图片下方可选择圆形、星星、心形、雨滴、月亮和狗爪。
- 右上角保存会先播放打印机出纸动画，结束后下载 PNG；手机拦截自动下载时，可点“未开始下载？点此保存”。
- 手机按竖版 3:4 居中显示，左右保留较宽留白。
- 只有确认居中人物或动物时才尝试主体轮廓重组；其他图片和识别不确定的情况随机取样。
- 图片处理全部在浏览器进行，照片不会上传；首次识别会加载随包提供的模型和运行组件，旧手机可能需要等候片刻。
- JPG、PNG、WebP 可直接上传；附有 HEIC 转换组件。少数手机照片编码仍可能不受支持，可先转为 JPG。

## 本地预览

不要直接双击 `index.html`：识别组件需要通过 HTTP 加载。在本目录执行 `python3 -m http.server 8000`，浏览器打开 `http://127.0.0.1:8000/`。

## 文件

- `index.html`：界面、形状、随机排版和打印保存动画。
- `assets/browser-ai.js`：浏览器内的人物动物检测、主体分离及照片格式转换。
- `assets/models/`：已附检测与分离模型，无需自行下载。
- `assets/runtime/`：已附浏览器推理组件与 HEIC 转换组件。
- `.github/workflows/pages.yml`：GitHub Pages 自动发布流程。

第三方组件说明见 `THIRD_PARTY.md`。本包不包含用户上传的照片、预览截图、账号信息或本机运行环境。
