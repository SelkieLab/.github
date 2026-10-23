<div align="center">

<img src="./assets/banner.svg" alt="SelkieLab" width="820">

### 小而完整的自托管工具

不追求大而全，只做能装在自己机器上、一个人也维护得动的东西。<br>
数据不出门，出问题能自己看代码修。

[![Repos](https://img.shields.io/badge/repos-2-6b8afd?style=flat-square)](https://github.com/orgs/SelkieLab/repositories)
[![License](https://img.shields.io/badge/license-MIT-3ddc97?style=flat-square)](https://github.com/SelkieLab/bot-panel/blob/main/LICENSE)
[![Stack](https://img.shields.io/badge/python-stdlib%20only-f7c948?style=flat-square)](#)

[官网](https://selkielab.github.io) · [项目](#项目) · [取向](#取向) · [上手](#上手)

</div>

---

## 项目

### [bot-panel](https://github.com/SelkieLab/bot-panel) · AstrBot + SnowLuma 控制面板

把 QQ 机器人的日常运维收进一个网页：容器状态、实时日志、插件市场、人格提示词、
扫码登录、知识库，全在一个界面里。

| | |
|---|---|
| **后端** | 单文件 `server.py`，纯 Python 标准库，零第三方依赖 |
| **前端** | MD3 单页应用，partials 分片加载，移动端可用，PWA 离线兜底 |
| **运维** | 2700+ 插件分页 / 分类 / 排序、安装卸载更新、SSE 实时日志 |
| **安全** | PBKDF2 口令、TOTP 两步验证、会话失效、审计日志、QQ / webhook 告警 |
| **部署** | systemd 非特权用户 + 只读文件系统 + 最小 syscall 集合 |
| **备份** | 每日自动，sqlite 在线快照，只备不可再生数据 |

```bash
git clone https://github.com/SelkieLab/bot-panel.git
cd bot-panel
PANEL_INIT_PASSWORD='你的密码' python3 server.py
```

<sub>[README](https://github.com/SelkieLab/bot-panel#readme) · [部署](https://github.com/SelkieLab/bot-panel/tree/main/deploy) · [改造记录](https://github.com/SelkieLab/bot-panel/blob/main/docs/CHANGELOG-2026-10-23.md)</sub>

---

## 取向

做东西时反复回到的几条判断，写下来免得自己忘：

| 取舍 | 选择 | 为什么 |
|---|---|---|
| 依赖 vs 可读 | **少依赖** | 标准库能写就不引包。三年后 `pip install` 挂了，代码还在 |
| 功能 vs 可懂 | **可懂优先** | 一个人读不完的架构，等于没人能维护 |
| 便利 vs 安全 | **安全不让步** | 面板这类东西一旦被拿了就是整台机器，别赌 |
| 通用 vs 合用 | **先合用** | 先解决自己的问题，抽象等第二次重写再说 |

## 上手

1. **准备环境** —— Python 3.8+ 与 Docker
2. **克隆并启动** —— 设一个初始口令，其余配置都在界面里填
3. **上 HTTPS** —— 面板可直载证书，也可放在 Nginx / Caddy 后面；裸 HTTP 暴露公网等于明文发密码
4. **收窄端口** —— 安全组只放行自己的 IP，顺手开两步验证

## 技术栈

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![systemd](https://img.shields.io/badge/systemd-000000?style=flat-square&logo=systemd&logoColor=white)

## 联系

* 提 issue、发 PR 都欢迎，先看对应仓库的 README 与 [CONTRIBUTING](https://github.com/SelkieLab/.github/blob/main/CONTRIBUTING.md)
* 安全相关问题请按 [SECURITY](https://github.com/SelkieLab/.github/blob/main/SECURITY.md) 的方式私下报告，别开公开 issue

<div align="center">
<sub>SelkieLab · 2026</sub>
</div>
