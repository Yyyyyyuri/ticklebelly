# 挠挠胃袋

用绿色餐馆卡片和随机抽选，决定下一顿吃什么。

## 使用

在此目录启动静态 HTTP 服务，例如：

```sh
python -m http.server 8000
```

打开 http://localhost:8000 。页面打开时自动读取同目录的 `restaurants.json`，请勿直接以 `file://` 打开 HTML。

点击餐馆卡片切换是否参与抽选，或使用「全选 / 取消全选」，然后点击「挠一下」。每家选中的餐馆被抽中的概率相同。

## 修改餐馆

编辑 `restaurants.json`，保存后刷新网页：

```json
[
  "餐馆 A",
  "餐馆 B"
]
```

名称不能留空，最后一项后不要加逗号。名单在每次打开页面时重新加载。

## 部署

这是无需构建的静态网站，可部署到 GitHub Pages 等静态托管服务。`index.html` 与 `restaurants.json` 需保持在同一目录。
