# 公开 Skill 正本

每个 Skill 单独放在仓库根目录的 `<name>/` 下。目录名使用英文短横线命名，与 `SKILL.md` 的 `name` 一致。

```text
<name>/
├── SKILL.md       # 指令文件；description 说明触发条件
├── scripts/       # 可选：脚本
└── templates/     # 可选：模板
```

此仓库是公开的，不放私有 Skill 或秘密（包括提交历史）。私有提示词收录集只登记 Skill 的位置、用途和安装方法，不复制正本。正本更新后记得更新收录集里的索引版本和日期。

## 安装到 Claude Code

先把仓库克隆到一个长期保留的位置，阅读待安装的 Skill 和脚本，确认可信后再链接。把下面的 `<name>` 替换为实际目录名：

```sh
git clone https://github.com/FiringJ/skills.git "$HOME/firingj-skills"
mkdir -p "$HOME/.claude/skills"
ln -s "$HOME/firingj-skills/<name>" "$HOME/.claude/skills/<name>"
```

其他工具用同样的方式链接到各自约定的目录；安装前查阅该工具的当前文档。ChatGPT 网页版没有本机 Skill 安装目录，可按需把指令用作 GPT 或项目指令。从克隆目录执行 `git pull` 即可更新软链接指向的正本。
