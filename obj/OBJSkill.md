# 技能释放组件

主要由两个功能，一是提供默认攻击的接口，二是监听玩家操作的游戏对象的主动释放技能;[关于通过学习习得的技能有专门的章节介绍](../learnSkill/index.md)

## 外部接口

- cast(type: OBJSkillTYPE, atkSource: cc.Node) 释放默认攻击
- caculateSkillDamage(type: OBJSkillTYPE) 默认攻击伤害