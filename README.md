# Mower 自动构建

这个仓库每天自动从 [ArkMowers/arknights-mower](https://github.com/ArkMowers/arknights-mower) 拉取最新代码，编译为 Windows x64 的可执行程序并发布到 Releases。

## Downloads

| 分支 | Release | 说明 |
|------|---------|------|
| `main` | [mower-main-win64](https://github.com/citydirector/arkmower-builds/releases/tag/mower-main-win64) | 稳定版 |
| `dev` | [mower-dev-win64](https://github.com/citydirector/arkmower-builds/releases/tag/mower-dev-win64) | 预览版，包含最新功能但可能不稳定 |

下载 zip 解压后直接运行 `mower.exe` 即可。

## 构建频率

- **每天 UTC 6:00（北京时间 14:00）** 自动构建一次
- 也可以在 Actions 页面点 **Run workflow** 手动触发

## 构建流程

```
拉取上游代码 → 构建前端 (npm) → 安装 Python 依赖 → PyInstaller 打包 → 发布到 Releases
```

## 技术栈

- Windows Server 2022 (GitHub Actions)
- Python 3.12 + PyInstaller
- Node.js 22
