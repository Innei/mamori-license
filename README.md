# Mamori Source License

守り（mamori）：一份面向 AI 时代的 source-available 许可证。源码公开，但不允许被平台方收编、被商业转售，也不允许借 AI 改写一遍就绕开。

> 它**不是** OSI 定义的开源许可证。对外请称为 source-available。

## 文件

| 文件 | 用途 |
| --- | --- |
| [LICENSE.md](LICENSE.md) | 许可证正文（英文，以此为准） |
| [LICENSE.zh-CN.md](LICENSE.zh-CN.md) | 中文参考译本 |
| [CLA.md](CLA.md) | 贡献者授权协议，签一次对所有项目生效 |
| [template/](template/) | 新项目直接复制的文件 |

## 一眼看懂

| 场景 | 可以吗 |
| --- | --- |
| 个人使用、学习、自部署 | ✅ |
| 公司内部使用（不对外提供） | ✅ |
| 提 PR 贡献 | ✅ 需签 CLA |
| 非商业 fork，保留署名、沿用本许可证、公开完整源码 | ✅ |
| 改了代码后对外提供网络服务（非商业） | ✅ 但必须在界面里给出完整源码链接 |
| 原样部署、不改代码 | ✅ 无需公开源码 |
| 做成商业竞品，或付费转售 | ❌ 需事先书面授权 |
| 项目对接的平台方把它并入自家产品（开源也不行） | ❌ 需事先书面授权 |
| 拿源码喂给 AI 重写一个同功能产品 | 视为衍生作品，受同样约束 |
| 拿源码训练模型 | ❌ |
| 用 Copilot / Claude Code 帮你改自己的 fork | ✅ |
| 没看过源码，独立做一个同类产品 | 不受本许可证约束 |

## 新项目接入

1. 复制 `template/` 下所有文件（含 `.github/`）到新项目根目录
2. 替换 `LICENSE` 里的 `<YEAR>`、`<PROJECT NAME>`、`<PROJECT URL>`、`<CONTACT>`（授权申请邮箱）
3. 在 GitHub 创建私有仓库 `Innei/cla-signatures`（只需一次），再给新项目添加仓库 secret `CLA_SIGNATURES_TOKEN`：一个对 `cla-signatures` 有 Contents 读写权限的 fine-grained PAT
4. README 的 License 段落写：`Source-available under the [Mamori Source License 1.0](LICENSE).`

## 已知限制

- 第 4.3 条（平台方条款）和第 5 条（AI 衍生）目前在中美都没有判例，执行力度不确定。正式使用前建议找律师审一遍。
- 许可证只约束接触过源码的人。只看产品、不看代码的独立复刻，需要靠商标和产品迭代来应对。
- 已经用其他许可证（如 AGPL）发布的旧版本，不受本许可证追溯约束。
- 第 8 条（网络使用）借鉴 AGPL-3.0 第 13 条的思路，但 Mamori **不兼容** GPL / AGPL：GPL 系代码不能并入 Mamori 项目，Mamori 代码也不能并入 GPL 系项目。
- CLA 签署使用 [contributor-assistant/github-action](https://github.com/contributor-assistant/github-action)，上游已归档，模板里固定在 v2.6.1 的 commit SHA。哪天失效了，换成维护中的 fork 即可。

## 致谢

条款结构参考了 [FSL-1.1](https://fsl.software)（竞争性使用、允许用途、专利条款的思路）、[PolyForm](https://polyformproject.org)（关联方定义、首次违约纠正期）、[AGPL-3.0](https://www.gnu.org/licenses/agpl-3.0.html)（网络使用须公开源码）和 Apache ICLA（CLA 结构）。正文为独立撰写，未复制上述文本。
