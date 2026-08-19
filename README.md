# CGW · Cursor Gateway

CGW 是 Cursor 的本机网关客户端：**默认走你已登录的 Cursor 账号**，需要时可**无感切换**到按需号池或自建网关线路。

本仓库只放安装包与发行目录，不含源码。

---

## 下载

打开 **[最新 Release](https://github.com/007AMOS/cgw-releases/releases/latest)**，只需下载下面两项：

| | 文件 | 说明 |
| --- | --- | --- |
| **Cursor 插件** | [`cgw-agent.vsix`](https://github.com/007AMOS/cgw-releases/releases/latest/download/cgw-agent.vsix) | 装进 Cursor / VS Code，负责线路切换与用量查看 |
| **桌面管理工具** | [`cgw-desktop-win32-x64.exe`](https://github.com/007AMOS/cgw-releases/releases/latest/download/cgw-desktop-win32-x64.exe) 等 | 安装插件与本机服务、管理账号与状态 |

> 其他平台请在 Release 页选择对应的 `cgw-desktop-<平台>` 文件。  
> macOS 为 `.app.zip`，Linux / macOS Intel / Apple Silicon 文件名后缀不同。

**本机服务无需手动下载** — 安装插件或打开桌面工具后会自动拉取并常驻本机，负责转发流量。

---

## 它能做什么

- **双槽分流切号**：在本机 Cursor 账号与按需号池之间切换，过程尽量无感，不用反复登录
- **本机优先**：默认使用你电脑上已登录的 Cursor 账号，不依赖远端 Token
- **按需接网关**：只有要用按需号池、计费或远程转发时，才连到自建网关
- **用量可见**：在插件侧栏或桌面工具里查看当前线路与消耗

桌面管理工具**只负责安装、状态与账号**，不承载业务流量。关掉窗口后，本机服务仍在后台转发。

---

## 安装步骤

1. 下载并安装 **Cursor 插件**（`.vsix`：在 Cursor 中选择「从 VSIX 安装」）
2. 可选：下载 **桌面管理工具**，用于一键安装插件、查看本机服务状态
3. 打开 Cursor，插件会自动拉起本机服务；首次使用按提示选择线路即可

---

## 访问 GitHub 不通时

在桌面工具 **设置** 或插件 **设置** 里填写「发行源代理」，例如 `http://127.0.0.1:7890`。

这只影响下载安装包和读取发行目录，**不影响**连接你自己的网关。留空则跟随系统代理，再没有则直连。

---

## 交流社区

使用问题、版本更新、经验交流，请进 QQ 群 **AI 交流社区**：

- 群号：`1092395668`
- [点击链接加入群聊](https://qm.qq.com/q/5maq5v53Ta)
