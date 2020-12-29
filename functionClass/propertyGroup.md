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
    属性的意义可以按字面意思理解。需要着重提出的几个属性是
    - 1，atkSpeed: number = 0; // 攻击速度
      - 攻击速度的单位是 次/每秒 ，例如：设置为 0.5 是意味着 2 秒攻击 1 次。
    - 2，atkRange: number = 0; // 攻击范围
      - 单位是 网格 ，例如：设置为 2 时，与敌人相距两个网格时可发起攻击。
    - 3，hate: number = 0; // 仇恨加成
      - 单位是百分比，游戏对象可以设置为按仇恨选中首选攻击目标，在每次攻击时给予对方的仇恨会乘以这个系数