# selkielab.github.io

SelkieLab 组织落地页。纯静态单页，无构建步骤、无外部依赖、无 CDN —— 双击就能看。

https://selkielab.github.io

## 改什么

只有一个文件：`index.html`。样式、脚本、文案全在里面，按区块注释分区：

| 区块 | 内容 |
|---|---|
| `MD3 颜色角色` | primary / surface-container 分级 / outline-variant，改 `:root` 换整套外观；浅色主题在 `html[data-theme=light]` |
| `顶栏` / `Hero` | 导航与首屏 |
| `区块` / `项目卡` | 卡片与项目展示的通用样式 |
| `入场动效` | `.reveal` 错峰淡入，系统开了「减少动效」会自动关掉 |

## 本地预览

```bash
python3 -m http.server 8000
# 打开 http://127.0.0.1:8000
```

直接双击 `index.html` 也能看，只是剪贴板功能在某些浏览器下会受限。

## 已包含

* MD3 色板与形状令牌，深色 / 浅色主题跟随系统、可手动切换（记在 localStorage）
* 按钮 / 卡片 / chips / list item 按 M3 规范，带 ripple 与 state layer
* 移动端优先，窄屏自动收起导航
* 语义化标签 + aria 标签，键盘可达
* `prefers-reduced-motion` 尊重系统设置
* 命令块一键复制

## 部署

仓库 `main` 分支根目录 → GitHub Pages（Settings → Pages → Deploy from a branch → main / root）。
推上去一两分钟生效。
