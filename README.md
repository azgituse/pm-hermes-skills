# PM Hermes Skills

产品经理专属的 Hermes Agent 技能集合，用于低代码平台营销活动玩法组件的产品需求文档编写。

## 技能列表

| 技能名称 | 描述 | 路径 |
|---------|------|------|
| prd-document-creation | 创建PRD文档，包括原型设计和飞书文档生成 | `skills/prd-document-creation/` |

## 安装方式

### 方式一：一键安装脚本（推荐）

在 Hermes Agent 对话中复制执行以下命令：

```bash
# 一键安装 PRD 文档创建技能
bash -c '
REPO_URL="git@github.com:azgituse/pm-hermes-skills.git"
SKILL_NAME="prd-document-creation"
SKILL_DIR="$HOME/.hermes/skills/productivity/$SKILL_NAME"
TEMP_DIR="$(mktemp -d)"

echo "正在安装技能: $SKILL_NAME..."

# 克隆到临时目录
git clone --depth 1 "$REPO_URL" "$TEMP_DIR/repo" 2>/dev/null

# 创建技能目录并复制文件
mkdir -p "$SKILL_DIR"
cp "$TEMP_DIR/repo/skills/$SKILL_NAME/SKILL.md" "$SKILL_DIR/"

# 清理临时目录
rm -rf "$TEMP_DIR"

echo "✅ 技能安装完成: $SKILL_NAME"
echo "使用方法: skill_view(\"$SKILL_NAME\")"
'
```

### 方式二：分步手动安装

如果一键脚本执行失败，可以分步执行：

```bash
# 1. 克隆仓库到临时目录
cd /tmp && git clone git@github.com:azgituse/pm-hermes-skills.git

# 2. 创建技能目录
mkdir -p ~/.hermes/skills/productivity/prd-document-creation

# 3. 复制技能文件
cp /tmp/pm-hermes-skills/skills/prd-document-creation/SKILL.md ~/.hermes/skills/productivity/prd-document-creation/

# 4. 清理临时文件
rm -rf /tmp/pm-hermes-skills
```

安装完成后即可使用：
```
skill_view("prd-document-creation")
```

### 方式三：批量安装所有技能

```bash
# 1. 克隆仓库
git clone git@github.com:azgituse/pm-hermes-skills.git ~/pm-hermes-skills

# 2. 复制所有技能到 Hermes 目录
cp -r ~/pm-hermes-skills/skills/* ~/.hermes/skills/productivity/

# 3. 验证安装
ls ~/.hermes/skills/productivity/
```

## 目录结构

```
pm-hermes-skills/
├── README.md              # 本文件
├── skills/                # 技能目录
│   └── prd-document-creation/
│       ├── SKILL.md       # 技能主文件（必须）
│       ├── references/    # 参考资料（可选）
│       ├── templates/     # 模板文件（可选）
│       └── scripts/       # 辅助脚本（可选）
└── docs/                  # 文档（可选）
```

**注意：** Hermes Agent 只识别 `SKILL.md` 文件，其他目录都是可选的辅助资料。

## 技能详情

### prd-document-creation

用于创建低代码平台营销活动玩法组件的PRD文档。

**功能：**
- 创建4个原型文件（C端交互稿、B端配置界面、玩法配置弹窗、数据统计页面）
- 生成符合规范的PRD飞书文档
- 支持多种玩法类型（抽奖、报名、集卡等）

**使用方法：**
```
加载技能：skill_view("prd-document-creation")
```

## 更新记录

- 2025-04-23: 初始化仓库，添加第一个技能 prd-document-creation

## 贡献指南

1. 新增技能时，在 `skills/` 目录下创建新文件夹
2. 必须包含 `SKILL.md` 文件，遵循技能编写规范
3. 更新本 README.md 的技能列表
4. 提交 PR 或联系仓库维护者

## 作者

产品经理 @ 低代码平台团队
