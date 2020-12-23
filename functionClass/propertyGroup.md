# 属性数据集合,集合完整描述一个游戏对象的数值属性

```ts
export class propertyGroup {
    phyDamage: number = 0; // 物理攻击
    magicDamage: number = 0; // 魔法攻击
    phyResis: number = 0; // 物理抗性
    magicResis: number = 0; // 魔法抗性
    atkSpeed: number = 0; // 攻击速度
    critRate: number = 0; // 暴击率
    critDamage: number = 0; // 暴击伤害
    atkRange: number = 0; // 攻击范围
    hp: number = 0; // 生命值
    mp: number = 0; // 魔法值
    walkSpeed: number = 0; // 移动速度
    hate: number = 0; // 仇恨加成
}
```

# 类描述

    该类完整描述了一个游戏对象应该具有的所有属性。