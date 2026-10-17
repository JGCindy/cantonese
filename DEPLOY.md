# 部署记录 · JGCindy/cantonese

## 已完成

- 仓库 `JGCindy/cantonese` 已存在（用户手动创建，Public）
- 已推送 `main` 分支，commit `9481281`
  - `index.html`（965,642 字节，来自 `粤语学习中心.html` 改名）
  - `README.md`

## 还差一步（必须手动，API 无权限）

GitHub 仓库 Pages 设置不能用 API 或 git 打开，只能在网页点：

1. 打开 https://github.com/JGCindy/cantonese/settings/pages
2. **Source** 选 `Deploy from a branch`
3. **Branch** 选 `main`，目录选 `/ (root)`
4. 点 **Save**
5. 等 30 秒～2 分钟，访问 https://jgcindy.github.io/cantonese/

## 以后更新页面的流程

```bash
cd "D:/Users/2026/WorkBuddy/2026-10-17-16-13-59/cantonese-deploy"
cp "D:/Users/2026/WorkBuddy/2026-10-11-16-10-05/粤语学习中心/粤语学习中心.html" index.html
git add -A
git commit -m "更新"
git push
```

推送后 Pages 会自动重建，等半分钟刷新即可。

## 注意

- **本机 git 凭证可用**，`git push` 无需登录。GitHub 连接器（GHToken）只有读权限，写入会 403，不要用连接器做写入操作。
- 音频未上传：`media/lshk/` 14759 个 mp3 共 181MB、`media/jc/` 416 个共 5.5MB。页面里 `DICT_DIR` 指向这两个目录，会 404。
- 若要启用真人发音词库，需另行处理音频托管（精简后入库 / 放对象存储 / CDN）。
