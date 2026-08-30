# BookAI 官网（GitHub Pages）

纯静态营销站：落地页 + 隐私政策 + 用户协议。零构建、零依赖，改完直接传。

```
website/
├── index.html      落地页（功能 / 定价 / FAQ / 下载）
├── privacy.html    隐私政策
├── terms.html      用户协议
└── css/style.css   全站样式
```

## 本地预览

双击 `index.html` 在浏览器打开即可（无需任何服务）。

## 部署到 GitHub Pages（二选一）

### 方式 A：命令行（推荐）

1. 在 GitHub 网页上点 **New repository**，仓库名填 **`<你的用户名>.github.io`**
   （用这个名字，Pages 会自动开启，访问域名就是 `https://<用户名>.github.io`）。
   先建空仓库，不要勾选任何初始化文件。
2. 本地把 `website/` 的内容推上去：

```bash
cd website
git init
git add .
git commit -m "BookAI 官网"
git branch -M main
git remote add origin https://github.com/<用户名>/<用户名>.github.io.git
git push -u origin main
```

3. 等 1–2 分钟，访问 `https://<用户名>.github.io` 即可。

> 如果仓库名**不是** `.github.io`：建库后在
> **Settings → Pages → Source: Deploy from a branch → Branch: main / (root) → Save** 开启。

### 方式 B：GitHub Desktop（不会命令行就用这个）

1. 装 [GitHub Desktop](https://desktop.github.com)，登录账号。
2. **File → New repository**，名字填 `<你的用户名>.github.io`，本地路径选 `website` 所在位置。
3. 把 `website/` 下的文件拖进仓库目录，写个 Commit，点 **Publish repository**。
4. 同样访问 `https://<用户名>.github.io`。

## 想用自定义域名（可选）

在仓库根目录放一个 `CNAME` 文件，内容写你的域名（如 `bookai.app`），
再到域名商把该域名加一条 **CNAME 记录指向 `<用户名>.github.io`**。
注意：GitHub Pages 服务器在海外，国内访问可能偏慢，且无需（也无法）ICP 备案。

## 上架商店时

- 隐私政策 URL → `https://<你的域名>/privacy.html`
- 用户协议 URL → `https://<你的域名>/terms.html`
- 目前支持邮箱 `support@bookai.app` 是占位，上线前替换成真实邮箱
  （`index.html`、`privacy.html`、`terms.html` 各有一处）。
