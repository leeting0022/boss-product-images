# bos-product-images

博斯服饰货品图片图床（GitHub + jsDelivr CDN）。

## 目录结构

```
2022-2025/   2022–2025 年秋冬货品图片（.jpg，共 1071 张）
2026/        2026 年秋冬货品图片（.jpg，共 227 张）
manifest.json  全部图片的 jsDelivr 直链清单（id -> url 映射）
```

文件名即货品数字 ID（如 `10323979084022.jpg`），与商品资料编码对应。

## 通过 jsDelivr 引用图片

公开仓库，任意图片均可经 jsDelivr 直接访问：

```
https://cdn.jsdelivr.net/gh/<USERNAME>/bos-product-images@main/2022-2025/10323979084022.jpg
https://cdn.jsdelivr.net/gh/<USERNAME>/bos-product-images@main/2026/14311321198124.jpg
```

在 HTML 中使用：

```html
<img src="https://cdn.jsdelivr.net/gh/<USERNAME>/bos-product-images@main/2026/14311321198124.jpg" alt="货品 14311321198124">
```

## 说明

- 仓库必须保持 **public**，jsDelivr 才能代理。
- 首次推送后 CDN 通常有数秒～1 分钟缓存预热。
- `manifest.json` 提供 `id -> url` 映射，便于在前端按货品 ID 取图。
- 如需更新图片：替换文件后重新推送；强制刷新 CDN 可在 URL 后加 `?v=时间戳` 或发布新的 release tag 并引用 `@版本`。
