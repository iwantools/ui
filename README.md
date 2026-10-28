# iwantools/ui

iwantools UI 组件 registry 的**自动生成产物仓**：源码事实源在 [iwan-admin](https://github.com/iwantools/iwan-admin)，
本仓只接收 `scripts/publish-registry.mjs` 的构建产物，禁止手改（ADR-0011）。

## 消费（任选其一）

```bash
# ① 命名空间（推荐）：components.json 的 registries 注册一次（见下方 URL 模板），之后短名安装
pnpm dlx shadcn add registry @iwantools=https://iwantools.github.io/ui/v1-dev/r/{name}.json
pnpm dlx shadcn add @iwantools/pattern-feedback @iwantools/command

# ② 单件直拉（GitHub Pages 主通道）
pnpm dlx shadcn add https://iwantools.github.io/ui/v1-dev/r/pattern-feedback.json

# 备用通道（tag 不可变，三通道内容一致）
#   jsDelivr: https://cdn.jsdelivr.net/gh/iwantools/ui@v1-dev/r/<item>.json
#   raw:      https://raw.githubusercontent.com/iwantools/ui/v1-dev/r/<item>.json
```

item 清单见各版本目录的 `registry.json`（ui 原件 + `pattern-*` 组合件 + fork 件 + hooks/lib）。
组件源码随 `shadcn add` 落进你的工程并归你所有——不是 npm 运行时依赖。

## 版本

| 目录 | 来源 |
| --- | --- |
| v1-dev | iwan-admin（本次发布；正式版以基座发行 tag 命名） |
