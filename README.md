<div align="center">
    <h1>LSPilot</h1>
    <p>手机端的 AI 逆向分析与动态插件调试工具</p>

[![Telegram](https://img.shields.io/static/v1?label=Telegram&message=Channel&color=0088cc)](https://t.me/LSPilot)
[![GitHub release (latest SemVer)](https://img.shields.io/github/v/release/Xposed-Modules-Repo/me.yun.lspilot)](https://github.com/Xposed-Modules-Repo/me.yun.lspilot/releases)
[![Platform](https://img.shields.io/badge/Android-14%2B-3DDC84?style=flat-square&logo=android)](https://developer.android.com/about/versions/14)
[![Xposed](https://img.shields.io/badge/Xposed-LSPosed-blue)](https://github.com/LSPosed/LSPosed)
[![GitHub stars](https://img.shields.io/github/stars/Xposed-Modules-Repo/me.yun.lspilot?label=Stars)](https://github.com/Xposed-Modules-Repo/me.yun.lspilot/stargazers)
[![GitHub download](https://img.shields.io/github/downloads/Xposed-Modules-Repo/me.yun.lspilot/total?label=%E4%B8%8B%E8%BD%BD%E9%87%8F)](https://github.com/Xposed-Modules-Repo/me.yun.lspilot/releases)
</div>

---

## UI 预览

![功能预览](docs/screenshots/features.png)

---

## 模块介绍

LSPilot是一个基于 AI 驱动的动态逆向分析与自动化助手。通过编写基于规则的Xposed脚本，您可以轻松在目标应用内实现动态分析与自动化执行，专为 LSPosed 框架打造的智能逆向领航员。

它旨在将传统复杂、枯燥、高门槛的安卓逆向分析流程，简化为“一句话的事”。无论你是想破解某个应用的会员功能，还是逆向追踪关键构造函数的调用链，LSPilot 都能像经验丰富的领航员一样，带你穿越混淆代码的迷雾。

核心工作流：
当你提出需求（如：“帮我Hook掉这个会员校验”），AI 会解析意图，通过 内置工具 (functioncalling) 自动定位目标类和方法。随后，AI 会为你生成可直接运行的示例代码和清晰的逆向思路，最后通过 LSPosed 框架一键动态注入脚本，实时验证结果。

LSPilot 要解决的三大痛点：

1. 为小白而生：不懂 Smali、看不懂混淆？你只需用大白话描述想干什么，LSPilot 帮你把“查找、分析、写脚本、注入”全链路自动化。
2. 为效率而生：逆向工程师不再需要手撸繁琐的 findAndHook 样板代码，AI 还能直接生成精准的 Hook 逻辑。
3. 为动态而生：通过内置的脚本引擎，支持在运行时动态下发和执行修复逻辑，无需反复编译模块。

---

## 功能介绍

### 逆向分析

| 功能 | 描述 |
|------|------|
| jadx 反编译 | 在手机上直接反编译 APK/DEX 文件，查看 Java 源码 |
| DexKit 搜索 | 高性能 DEX 字节码搜索，支持类/方法/字段链式查询 |
| Dex 搜索器 | 基于 smali/baksmali 的 DEX 文件分析与搜索 |
| 资源读取器 | 解析和查看 Android 资源文件 (ARSC) |
| 类型签名解析 | 解析 Java 类型签名，辅助方法查找 |
| 字符串分析器 | 分析和定位 DEX 中的字符串引用 |

### 插件引擎

| 功能 | 描述 |
|------|------|
| BeanShell (Java) | 兼容 Java 语法，可直接调用 Android API |
---

## 安装说明

### 环境要求

- **Xposed 框架**: LSPosed
- **Android 版本**: Android 14.0 及以上
- **架构**: arm64-v8a

### 安装步骤

1. 确保已安装 LSPosed 框架
2. 下载最新版本的 APK 文件
3. 在 LSPosed 中激活 LSPilot 模块
4. 选择目标应用为作用域
5. 重启目标应用即可生效

### 下载地址

- [GitHub Releases](https://github.com/Xposed-Modules-Repo/me.yun.lspilot/releases)
- [Telegram 频道](https://t.me/LSPilot)

---

## 常见问题

**Q: 插件脚本如何编写？**
> 插件存储在 `Android/media/<包名>/LSPilot/Plugin/` 目录下，支持 Java、Lua、JS 三种语言。创建插件后可直接在应用内编辑运行，API 文档 lspilot.fun。

**Q: 某些功能无法使用？**
> 部分功能依赖于目标应用的版本和系统环境，请确保模块已正确激活并选择了适当的作用域。

---

## 反馈与支持

- Telegram 频道: [LSPilot](https://t.me/LSPilot)
- QQ 群聊: [加入群聊](https://qun.qq.com/universal-share/share?ac=1&authKey=1y82uRJ0yDCI1h%2ButTYOnQCHjUM0XTNK2msja%2F7fhJDHRDnrbJ87aM365RTUpNwm&busi_data=eyJncm91cENvZGUiOiIyNTM0NjE5OTciLCJ0b2tlbiI6Im1yQ0J1MGROUVBrSjI5am5PYTVnMEtYYUR1bS9QNzFkM05FM2hSK1BxeTNXTk4ybjJqYUFDcXArRVNrNC9HN2giLCJ1aW4iOiIzNDQ5NDk2NjUzIn0%3D&data=csdW7tAjnP1NfSlcJ4rQHoDv7I7wYdMAVNWHCHQL-wMr6oCo-PTswODqSC63KJkKuROfjRKGqwbbAujcCPgFCw&svctype=4&tempid=h5_group_info)
