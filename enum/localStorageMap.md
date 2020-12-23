# 本地化存取功能数据键值

```ts
export enum localStorageMap {
    testData = "testData",
    rts_bag_data = 'rts_bag_data',
    rts_equp_data = 'rts_equp_data',
    rts_character_level = 'rts_character_level',
    rts_character_exps = 'rts_character_exps',
    rts_character_skill = 'rts_character_skill',
};
```

## 枚举意义

存取数据的键值

## 枚举描述

- testData 测试字段
- rts_bag_data 玩家背包数据
- rts_equp_data 玩家已经装备的物品数据
- rts_character_level 玩家**某个角色**的等级
- rts_character_exps 玩家**某个角色**的当前经验
- rts_character_skill 玩家**某个角色**的已经学会的技能