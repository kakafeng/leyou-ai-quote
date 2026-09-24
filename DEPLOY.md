# 部署说明（主公对外发布用）

## 方式 A：GitHub Pages（推荐，零成本）

1. 仓库建好后，进 `Settings → Pages → Source: Deploy from a branch → Branch: main / (root)`；
2. 等 1-2 分钟，访问 `https://<用户名>.github.io/leyou-ai-quote/`；
3. 该地址即为对外可分享的报价工具链接，自动 HTTPS（AES-GCM 加密功能即刻生效）。

## 方式 B：Vercel / Cloudflare Pages（域名自定义）

- 单文件静态站，拖 `leyou-ai-quote/` 文件夹进 Vercel Dashboard 的 "Import Project" 即可；
- 绑自有域名（如 `quote.leyou.cn`），CNAME 配置 5 分钟完成。

## 方式 C：绿联 NAS 自建

- 把 `index.html` 拷到 NAS 任意静态目录，配 nginx 或群晖/威联通 Web Station；
- 走内网或 Tailscale 分享。

## 注意事项

- 任何部署方式都必须 **HTTPS**（AES-GCM 加密需要 secure context）；
- 部署方**无需**配置任何后端 / 数据库 / 模型 API —— 用户自己填自己的 Key；
- 单文件 464KB，首屏加载 <1s（国内静态 CDN）。
