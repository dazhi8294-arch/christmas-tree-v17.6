# Christmas Tree v17.6

一棵会用 Canvas 旋转的粒子圣诞树，纯单文件 HTML，**不需要任何图片、字体或依赖**，双击 `index.html` 即可运行，也能直接扔到 GitHub Pages。

## 效果



![preview](preview.png)

## 特性



* 约 3000 个粒子构成的锥形树体，按俯仰角实时 3D 投影、逐帧按深度排序（前亮后暗）

* 金色螺旋灯带 + 5 色可变光护士球，带呼吸闪烁

* 树顶五角星 + 光晕脉动

* 星空、飘雪、地面光晕、暗角

* 鼠标移动可加速 / 反向旋转；点击画面会炸出一把星光

* 右下角「暂停 / 播放」

* 自适应桌面、平板、手机竖屏；支持 `devicePixelRatio` 高清屏渲染

## 本地预览

直接双击 `index.html`，或在本目录起个静态服务：



```
python -m http.server 8000
# 然后访问 http://localhost:8000
```

## 部署到 GitHub Pages

### 方式一：网页上传（最简单）



1. 打开 [https://github.com/new](https://github.com/new) ，仓库名填 `christmas-tree-v17.6`，选 **Public**，不要勾选 README /.gitignore，创建。

2. 进入仓库 → `Add file` → `Upload files`，把 `index.html` 拖进去，Commit。

3. 仓库 → `Settings` → 左侧 `Pages` → Source 选 **Deploy from a branch** → 分支 `main`，目录 `/ (root)` → `Save`。

4. 等 30 秒～2 分钟，访问：



```
https://<你的用户名>.github.io/christmas-tree-v17.6/
```

### 方式二：命令行推送



```
cd christmas-tree-v17.6
git init
git add index.html README.md preview.png
git commit -m "Christmas Tree v17.6"
git branch -M main
git remote add origin https://github.com/<你的用户名>/christmas-tree-v17.6.git
git push -u origin main
```

推送后同样去 `Settings → Pages` 选 `main` / `root` 并 Save。

### 注意



* 仓库必须是 **Public**（免费账号的 Pages 不支持私有仓库）。

* 入口文件必须叫 `index.html`，放在仓库根目录（或 `/docs` 目录，并在 Pages 里选 `/docs`）。

* 首次发布有 1～2 分钟生效时间，期间 404 属正常。

* 想换自定义域名：`Settings → Pages → Custom domain`，同时在域名商处加 CNAME 记录。