# AI Skills 私有技能库

本仓库用于长期沉淀个人/团队可复用 AI 工作技能。当前仅初始化两个核心技能：

1. `customer-ready-document`：客户正式文档 Skill
2. `ppt-visual-page`：PPT 图片页 Skill

## 设计原则

- 每一个 Skill 独立成目录，不合并到一个大文档。
- 每一个 Skill 单独维护 `SKILL.md`、`references/`、`CHANGELOG.md` 与 `archive/`。
- 更新时只更新对应 Skill，不影响其他 Skill。
- 所有重要调整通过 Git commit 记录，必要时可回退。
- 长期规则沉淀到 Skill；一次性项目要求放在项目资料中，不写入长期 Skill。

## 当前 Skills

| Skill | 用途 |
|---|---|
| `customer-ready-document` | 客户方案、可研报告、建设方案、产品介绍、拜访话术等客户可直接阅读的正式文档 |
| `ppt-visual-page` | 客户汇报、产品介绍、项目进度、渠道合作、领导宣讲类 PPT 图片页 |

## 使用方式

在开始某类任务前，把对应 Skill 的 `SKILL.md` 提供给模型，或者在支持 Skills 的平台中将对应目录上传为 Skill。

例如：

- 写客户方案、可研报告、建设方案、拜访话术：使用 `customer-ready-document`。
- 做客户汇报 PPT 图片页、产品介绍图、项目汇报图：使用 `ppt-visual-page`。

## 更新方式

更新时不要合并所有 Skill，只修改对应目录。例如：

- 客户文档表达规则变化：只更新 `skills/customer-ready-document/SKILL.md`。
- PPT 标题、字号、版式规则变化：只更新 `skills/ppt-visual-page/SKILL.md`。

每次更新建议同时修改对应 Skill 的 `CHANGELOG.md`。

## 回退方式

Git 本身支持版本回退。推荐策略：

1. 每次更新一个 Skill 单独提交一次 commit。
2. commit message 写清楚更新的 Skill 和规则。
3. 如果更新效果不好，可通过 GitHub 的历史记录恢复某个文件旧版本，或使用 Git 命令回退。

详细说明见 `ROLLBACK_GUIDE.md`。
