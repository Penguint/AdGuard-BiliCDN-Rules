# AdGuard-BiliCDN-Rules
**屏蔽 Bilibili 低质量 PCDN/MCDN，强制使用高速镜像 CDN！**  

通过 DNS/代理规则过滤 B 站的低质量 PCDN（如 `mcdn.bilivideo.cn`）和京东云 MCDN，自动选择阿里云、腾讯云等优质 CDN 节点，提升视频加载速度和稳定性。  

👉 **适用于**：AdGuard Home / DNS 服务器 / 代理工具（Clash、Surge）  

---

## 📦 功能特性  
- ✅ 屏蔽所有已知 B 站 PCDN 域名（`mcdn.bilivideo.cn`, `szbdyd.com` 等）  
- ✅ 保留高质量 Mirror CDN（阿里云、腾讯云、华为云节点）  
- ✅ 可选支持京东云 MCDN 屏蔽  
- ✅ 兼容 IPv6 环境优化  
- 📌 基于社区实测数据，持续更新规则  

---

## 🛠️ 快速使用  
### 1. AdGuard Home 用户  
在 AdGuard Home 的 DNS 黑名单中添加以下自定义订阅链接：
```plaintext
https://raw.githubusercontent.com/Penguint/AdGuard-BiliCDN-Rules/refs/heads/codex/custom-rules/adguard.txt
```

本分支额外屏蔽以下 CDN：
- 视频：`upos-hz-mirrorakam.akamaized.net`
- 音频：`upos-sz-mirrorcosov.bilivideo.com`

更新订阅后，清除 AdGuard Home 和设备的 DNS 缓存，再重新加载视频。可在 AdGuard Home 查询日志中确认这两个域名被拦截。屏蔽会阻止连接这些 CDN，是否能切换到其他节点取决于 Bilibili 播放器的回退行为。
