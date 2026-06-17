# Skills 回退指南

## 一、为什么要支持回退？

Skill 是长期工作标准。如果某次更新后模型表现变差，例如输出风格不自然、规则过多导致执行僵硬、或者和原本工作流程不一致，就需要回退。

## 二、推荐回退方式

### 方式 1：GitHub 页面恢复单个文件

适合不熟悉命令行的情况。

操作路径：

```text
进入文件 → History → 找到旧版本 → View file → Copy raw contents → 覆盖当前文件
```

然后提交一个新 commit，例如：

```text
revert(ppt-visual-page): restore previous title layout rules
```

### 方式 2：Git 命令恢复单个文件

```bash
git checkout <commit_id> -- skills/ppt-visual-page/SKILL.md
git add skills/ppt-visual-page/SKILL.md
git commit -m "revert(ppt-visual-page): restore previous skill version"
git push
```

### 方式 3：整体回退到某个版本

不推荐经常使用，因为可能影响其他 Skill。

```bash
git revert <commit_id>
git push
```

## 三、回退原则

- 能回退单个 Skill，就不要回退整个仓库。
- 能回退单个文件，就不要回退整个目录。
- 回退前先确认是哪条规则导致效果变差。
- 回退后在 `CHANGELOG.md` 中记录原因。

## 四、建议保留 archive 目录

如果某个 Skill 版本不再使用，但以后可能参考，可以移动到：

```text
skills/<skill-name>/archive/
```

不要直接删除有价值的旧规则。
