# SelkieLab 组织级文件

这个仓库不是一个项目，是组织的公共配置。GitHub 会把这里的文件当默认值，
任何没自己写对应文件的仓库都会继承下面这些。

## 里面有什么

| 文件 | 作用 |
|---|---|
| `profile/README.md` | 显示在 https://github.com/SelkieLab 的主页内容 |
| `profile/assets/banner.svg` | 主页顶部的横幅 |
| `CONTRIBUTING.md` | 全组织默认的贡献指南 |
| `SECURITY.md` | 全组织默认的漏洞报告方式 |
| `CODE_OF_CONDUCT.md` | 行为准则 |
| `SUPPORT.md` | 获取帮助的入口 |
| `GOVERNANCE.md` | 谁决定什么、什么会被拒 |
| `ROADMAP.md` | 正在做 / 想做 / 明确不做 |
| `.github/ISSUE_TEMPLATE/` | 没自己写模板的仓库继承这套表单 |
| `.github/pull_request_template.md` | 同上，PR 模板 |

## 改这些文件的影响范围

改 `profile/README.md` 立刻影响组织主页。
改 `CONTRIBUTING` / `SECURITY` 之类，只影响**没有自己写同名文件**的仓库。

比如 `bot-panel` 自己有一份更细的 `SECURITY.md`（带攻击面表格），
所以它不会继承这里的；但它没有 `CODE_OF_CONDUCT.md`，就继承这份。

## 维护

直接改，推 main。没有 CI，也不需要——这里只有文档。
