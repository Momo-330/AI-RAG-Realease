# AI-RAG 发布仓库

个人/企业知识库桌面端的公开下载与更新仓库。

当前版本：`2026.1018.01`

## 下载

- 最新安装包：<https://github.com/Momo-330/AI-RAG-Realease/releases/latest>
- 文件：`KB-Setup.exe`（per-user 安装，无需管理员权限）
- SHA256：见 `SHA256SUMS` 或 Release 说明

## 安装

1. 从 Releases 下载 `KB-Setup.exe`。
2. 运行安装包，默认安装到 `%LOCALAPPDATA%\KB`。
3. 首次启动进入个人空间，数据保存在本机。
4. 需要企业协作时，在「企业空间」填写企业服务器地址并登录。

> 当前安装包尚未代码签名，Windows 可能提示“未知发布者”，需要手动选择“仍要运行”。

## 自动更新

桌面端读取 `latest.json`：

```json
{
  "version": "0.1.0",
  "url": "https://github.com/Momo-330/AI-RAG-Realease/releases/download/v0.1.0/KB-Setup.exe",
  "sha256": "安装包 SHA256",
  "notes": "版本说明"
}
```

设置环境变量 `KB_UPDATE_URL` 指向本仓库的 `latest.json` 原始地址，然后在桌面端「帮助 → 检查更新」。
更新器会先校验 SHA256，再执行静默安装。

## 说明

- 源码仓库为私有仓库，不在此公开。
- 本仓库只放发布说明、更新清单和校验文件；安装包通过 GitHub Releases 分发。
