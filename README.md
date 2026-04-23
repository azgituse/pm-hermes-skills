# PM Hermes Skills

产品经理专属的 Hermes Agent 技能集合，用于低代码平台营销活动玩法组件的产品需求文档编写。

## 技能列表

| 技能名称 | 描述 | 路径 |
|---------|------|------|
| prd-document-creation | 创建PRD文档，包括原型设计和飞书文档生成 | `skills/prd-document-creation/` |

## 安装方式

### 方式一：使用 Hermes 内置命令（推荐）

在 Hermes Agent 对话中直接执行：

```bash
# 克隆仓库到本地
cd ~ && git clone git@github.com:azgituse/pm-hermes-skills.git

# 安装指定技能（以 prd-document-creation 为例）
cp -r ~/pm-hermes-skills/skills/prd-document-creation ~/.hermes/skills/productivity/
```

然后即可在对话中使用：
```
加载技能：skill_view("prd-document-creation")
```

### 方式二：手动复制（适合批量安装）

```bash
# 1. 克隆仓库
git clone git@github.com:azgituse/pm-hermes-skills.git

# 2. 复制所有技能到 Hermes 目录
cp -r pm-hermes-skills/skills/* ~/.hermes/skills/productivity/

# 3. 验证安装
ls ~/.hermes/skills/productivity/
```

### 方式三：使用 skill_manage 工具

```bash
# 创建技能目录并复制文件
mkdir -p ~/.hermes/skills/productivity/prd-document-creation
cp pm-hermes-skills/skills/prd-document-creation/SKILL.md ~/.hermes/skills/productivity/prd-document-creation/
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
