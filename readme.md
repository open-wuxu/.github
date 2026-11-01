# open-wuxu/.github

`open-wuxu` GitHub 组织的配置仓库，用于维护组织的公开主页。

> 组织主页内容见 [profile/README.md](profile/README.md) 与 [profile/README.zh-CN.md](profile/README.zh-CN.md)。
> 本文件是给开发者和协作者看的仓库说明，不会显示在组织主页上。

## 这个仓库是什么

GitHub 会读取 `.github` 仓库中 `profile/README.md` 的内容，并把它渲染为组织主页
（https://github.com/open-wuxu ）。修改该文件并推送到默认分支，即可更新对外的组织介绍。

仓库默认分支为 **`master`**。

## 目录结构

```text
.
├── profile/
│   ├── README.md         # 组织主页（英文，GitHub 实际渲染的文件）
│   ├── README.zh-CN.md   # 组织主页中文版
│   └── assets/           # 主页使用的图片
├── draft/
│   └── prd.md            # 产品愿景与定位草稿（内部讨论稿，非最终产品承诺）
├── readme.md             # 本文件：仓库说明
└── .gitignore
```

## 修改组织主页

1. 编辑 `profile/README.md`（英文）和 `profile/README.zh-CN.md`（中文），保持两版内容同步。
2. 新增图片放到 `profile/assets/`，在 README 中用**相对路径**引用：

   ```html
   <img src="assets/banner.jpg" alt="..." width="100%" />
   ```

3. 提交并推送到 `master`。
4. 等待几分钟（GitHub CDN 缓存），刷新组织主页确认效果。

## 注意事项

- **图片不要写死完整 URL。** 不要使用 `https://raw.githubusercontent.com/open-wuxu/.github/<分支名>/...`
  这类地址：仓库默认分支是 `master`，写成分支名不一致或分支后续改名时，图片会直接返回 404，
  页面只会显示 alt 文本。
- 相对路径的解析基准是 README 所在目录，即 `profile/`，因此写成 `assets/banner.jpg` 即可。
- `draft/` 下是内部草稿，其中的内容不构成对外承诺；对外表述以 `profile/README.md` 为准。
