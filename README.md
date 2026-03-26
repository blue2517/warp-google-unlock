## ✨ 功能特点

1.  **系统级路由接管 (Zero Config)**
    * 脚本直接修改 Linux 内核路由表 (`ip route`)。
    * **无论你使用 Xray, Sing-box, Hysteria2, TUIC 还是 SSH**，无需任何配置，流量在系统底层自动分流。
2.  **RackNerd / 纯 IPv4 专用修复**
    * 自动识别并剔除配置文件中的 IPv6 地址，防止启动报错。
    * **强制锁定 IPv4 Endpoint** (162.159.192.1)，解决因 DNS 解析到 IPv6 导致的握手失败 (Handshake=0) 问题。
3.  **精细化分流模式 (独家)**
    * **模式 1 (推荐)：** 仅代理 Google 搜索/Gemini/商店。**保留 YouTube 直连**（享受送中 IP 无广告福利）。
    * **模式 2：** 代理 Google 全家桶（含 YouTube）。适合 IP 彻底被送中无法看视频的情况。
    * **模式 3：** 包含 Netflix、Disney+、OpenAI 等流媒体规则。
4.  **极致稳定**
    * 内置 `PersistentKeepalive` 心跳保活，防止 WARP 隧道空闲断连。
    * 采用 `wgcf` 官方接口注册，纯净 WireGuard 协议。

## 🛠️ 一键安装

支持系统：Ubuntu / Debian / CentOS / AlmaLinux
要求：Root 权限

```bash
bash <(curl -sL https://raw.githubusercontent.com/blue2517/warp-google-unlock/refs/heads/main/warp-google.sh)
