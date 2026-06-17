# Skills 更新指南

## 一、什么时候应该更新 Skill？

只有长期可复用的规则才应该写入 Skill。建议满足以下任一条件再更新：

1. 同一类要求重复出现 3 次以上。
2. 某个规则明显影响交付质量。
3. 某个规则适用于多个项目，而不是只适用于当前项目。
4. 某个错误多次出现，需要用 Skill 固化防错。

## 二、什么时候不应该更新 Skill？

以下内容不建议写入长期 Skill：

- 某个客户的临时要求
- 某一页 PPT 的单次排版要求
- 某个项目的金额、时间、人员、编号
- 只适用于一次任务的表达方式
- 尚未验证有效的个人想法

## 三、更新流程

每次更新建议按以下格式执行：

```text
1. 先判断本次规则是否长期复用。
2. 确定更新哪个 Skill。
3. 只修改对应 Skill 的 SKILL.md 或 references 文件。
4. 更新该 Skill 的 CHANGELOG.md。
5. 单独提交一次 commit。
6. 使用一两个真实任务验证效果。
```

## 四、推荐提交信息

```text
update(customer-ready-document): refine client-facing wording rules
update(ppt-visual-page): add title alignment and typo checking rules
```

## 五、更新后检查

- 是否只影响对应 Skill？
- 是否和已有规则冲突？
- 是否写得太宽泛？
- 是否有正例和反例？
- 是否便于模型执行？
