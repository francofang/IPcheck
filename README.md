# IPcheck - Streaming Media Unlock Test

Fork from [yeahwu/check](https://github.com/yeahwu/check)，增加了代理支持。

## 快速使用

### 直接运行（不走代理）

```bash
wget -qO- https://github.com/francofang/IPcheck/raw/main/check.sh | bash
```

或者：

```bash
curl -fsSL https://github.com/francofang/IPcheck/raw/main/check.sh | bash
```

### 通过代理运行

先下载脚本，再指定代理执行：

```bash
# 下载脚本
wget -O check.sh https://github.com/francofang/IPcheck/raw/main/check.sh

# 通过 SOCKS5 代理运行
bash check.sh -p socks5h://代理地址:端口

# 示例
bash check.sh -p socks5h://127.0.0.1:1080
bash check.sh --proxy socks5h://192.168.1.100:7890
```

### 代理格式

- SOCKS5 代理：`socks5h://host:port`（推荐，DNS 也走代理）
- SOCKS5 代理：`socks5://host:port`（DNS 本地解析）
- HTTP 代理：`http://host:port`

> 💡 `socks5h` 中的 `h` 表示 DNS 解析也通过代理进行，检测结果更准确。

## 检测项目

- Netflix
- YouTube Premium
- BiliBili（大陆/港澳台/台湾）
- TikTok
- iQIYI International
- ChatGPT

## 截图示例

![](https://user-images.githubusercontent.com/13328328/226191175-2294d103-18d6-4931-8f53-6d1f8b918b81.png)

## 参考

- 原项目：https://github.com/yeahwu/check
- VPS Deals：https://hostalk.net/deals.html
