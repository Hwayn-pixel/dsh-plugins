# DSH 插件 · 路线图

三个 [DeepSeek Harness](https://github.com/deepseek-ai) 插件的演进路线：从哪里来，要往哪去。

| 插件 | 作用 | 仓库 |
|---|---|---|
| `dsh-image-skin` | 皮肤与染色：区域贴图、壁纸取色、视频壁纸 | [Hwayn-pixel/dsh-image-skin](https://github.com/Hwayn-pixel/dsh-image-skin) |
| `dsh-prompt-desk` | 提示词工作台：看清 / 写下 / 体检 system prompt | [Hwayn-pixel/dsh-prompt-desk](https://github.com/Hwayn-pixel/dsh-prompt-desk) |
| `dsh-touchstone` | 试金石：改提示词之前的评测与对账 | [Hwayn-pixel/dsh-touchstone](https://github.com/Hwayn-pixel/dsh-touchstone) |

## 看

直接打开 `index.html`（单文件、无依赖、可离线）。或访问 GitHub Pages。

## 图例

- **已发布**：已经发出去的版本，内容来自各自的 CHANGELOG
- **这一轮**：2026-11-22 这批改动
- **候选**：想到但还没排期的东西，不是承诺

## 更新

改 `index.html` 里对应的泳道格子即可；每格上方有自己的时间标签，窄屏会自动改成纵向堆叠。

## 三条铁律

写在页面底部，因为它们都是真踩过才写下的：

1. 插件导出 `Config` schema，才有设置命名空间；只调 `settings.register()` 在 0.2 上是静默无效的。
2. 要写的字段必须标 `.volatile()`，否则整次写入被拒，且不抛异常。
3. `describe()` 返回的 `namespaces` 是**数组**，不是字典。
