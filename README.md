# 圣诞·星光许愿树（GitHub Pages 独立版）

2400 粒子金色圣诞树 + 摄像头手势互动：握拳聚成树、伸出 1–4 指唤出一张照片、张开五指围成爱心照片墙。支持多张照片上传、只认单只操作手（另一只手拿手机入镜也不会误触）。

## 怎么放到 GitHub Pages 上

1. 在 GitHub 新建一个仓库（比如叫 `christmas-tree`）。
2. 把本文件夹里的全部内容原样上传到仓库根目录（`index.html`、`assets/` 文件夹、`.nojekyll` 都要，文件夹结构不要改）。
3. 仓库页面点 **Settings → Pages**，Source 选 **Deploy from a branch**，分支选 `main`、目录选 `/ (root)`，保存。
4. 等一两分钟，页面会给出网址，形如 `https://你的用户名.github.io/christmas-tree/`，用这个 https 网址打开就能玩。

## 使用注意

- **必须用 Pages 给的 https 网址打开**：浏览器只允许 https 页面申请摄像头；用 `http://IP` 或直接双击本地文件打开，摄像头都会被拒绝（页面逻辑和按钮、鼠标操作不受影响）。
- 推荐 Chrome / Edge 打开；点「开启摄像头」后在浏览器弹窗里选「允许」。
- 照片只在你自己的浏览器里处理，不会上传到任何地方。

## 文件说明

- `index.html` — 页面全部内容（样式和逻辑都在这一个文件里）。
- `assets/three.min.js` — Three.js（粒子渲染），本地引用。
- `assets/mediapipe/` — MediaPipe Hands 手势识别的全套文件（JS、WASM 引擎、模型）。页面运行时优先从公开 CDN（jsDelivr，`@mediapipe/hands@0.4.1675469240`）加载这些资源，CDN 连不上时自动改用包里这份本地文件，所以整包拷到任何静态托管上都能独立工作。
- `.nojekyll` — 让 GitHub Pages 原样发布 `assets/` 里的文件，不要删。
