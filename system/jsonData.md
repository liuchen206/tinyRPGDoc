# 读取策划配置表json数据

项目中的实现方案为，将策划excel表使用 **工具** 转为json文件供程序读取。本模块提供读取各种配置数据的接口。

**工具下载地址**，<a href="res/excelToJson.zip" target="_blank">点击下载 excelToJson.zip</a>

## 各个表单组织形式

- rtsItemsOverView 表
  - 该表配置了所有能够放置入背包的物品。配置的项目如第一行表头的描述，其中需要 **注意** 的是 `物品类型对应详细参数ID` 栏描述的是该物品对应 `物品类型` 下辖的子表的数据。
  - eg: `装备` 类型的物品对应的是装备的具体数据。`技能书` 类型对应的是技能数据
- rtsEquipSubTable 表
  - 配置的是`装备` 类型的物品的对应属性
- rtsSkill 表
  - 配置的是 `技能书` 相关数据
- rtsBuffs 表
  - 配置的是 buff 相关数据
- rtsMonster 表
  - 配置是 怪物 相关数据
- playerLevelProperty 表
  - 配置的是 玩家对应等级 对应的成长属性
  
## 接口总览
- getRtsItemByName
  - 该接口通过 **物品名字** 返回 **背包物品的具体数据** 
  - 示例
    ```ts
    let data = staticDesignData.instance.getRtsItemByName('普通大剑');
    cc.log('新版 物品表格', data['物品名字'], data['物品ID'])
    ```
- getRtsItemSubValByName
  - 通过 **item名字**（意味着可以放在背包），**获得item的详细子数据**
  - 示例
    ```ts
    let data2 = staticDesignData.instance.getRtsItemSubValByName('精良护肩');
    cc.log('新版 物品表格子表', data2['简要描述'], data2['装备部位'])
    let data3 = staticDesignData.instance.getRtsItemSubValByName('盾墙技能书');
    cc.log('新版 物品表格子表', data3['技能名字'], data3['技能描述'])
    ```
- getRtsBuffDataByName
  - 通过 **buff名字** ，获得 **buff数据**
  - 示例
    ```ts
        let data = staticDesignData.instance.getRtsBuffDataByName('冲动状态'); // 冲动状态 buff的数据
        let time = data['持续时间'];
    ```
- getRtsMonsterPropertyByName
  - 通过 **怪物名字** 获得 **怪物属性**
  - 示例
    ```ts
        let prop = staticDesignData.instance.getRtsMonsterPropertyByName('蝙蝠');// 蝙蝠的属性配置
    ```
  - [返回值 prop 是什么](../functionClass/propertyGroup.md)
- getRtsMonsterExpRewardByName
  - 通过 **怪物名字** 获得 **怪物奖励经验**
  - 示例
    ```ts
        let exps = staticDesignData.instance.getRtsMonsterExpRewardByName('蝙蝠'); // 蝙蝠的经验奖励
    ```
- getRtsMonsterItemRewardByName
  - 通过 **怪物名字** 获得 **怪物死亡物品奖励**
  - 示例
    ```ts
        let rewardItemList = staticDesignData.instance.getRtsMonsterItemRewardByName('蝙蝠'); // 蝙蝠的掉落奖励
        cc.log('读取击杀奖励', rewardItemList.toString());
    ```
- getExpsToNextLevel
  - 通过 **当前经验** 获得 **升级需要经验**
  - 示例
    ```ts
        let expToNewLevel = staticDesignData.instance.getExpsToNextLevel(99); // 升到100级所需经验
    ```
  - getPlayerPropertyByLevel
  - 获得玩家**当前级别**下的**固定属性**
  - 示例
    ```ts
        let levelPro = staticDesignData.instance.getPlayerPropertyByLevel(99) // 等级99固有属性
    ```