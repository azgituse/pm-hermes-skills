# PM Hermes Skills

产品经理专属的 Hermes Agent 技能集合，用于低代码平台营销活动玩法组件的产品需求文档编写。

## 技能列表

| 技能名称 | 描述 | 路径 |
|---------|------|------|
| prd-document-creation | 创建PRD文档，包括原型设计和飞书文档生成 | `skills/prd-document-creation/` |

## 使用方式

1. 将本仓库克隆到本地
2. 把需要的技能目录复制到 `~/.hermes/skills/productivity/` 下
3. Hermes Agent 会自动识别并加载技能

## 目录结构

```
pm-hermes-skills/
├── README.md              # 本文件
├── skills/                # 技能目录
│   └── prd-document-creation/
│       ├── SKILL.md
│       ├── references/    # 参考资料
│       ├── templates/     # 模板文件
│       └── scripts/       # 辅助脚本
└── docs/                  # 文档
```

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

## 作者

产品经理 @ 低代码平台团队
