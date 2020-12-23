# 玩家游戏数据管理中心

该类为单例类，管理了跟玩家游戏相关的所有数据。包括（玩家拥有角色，物品，装备，角色的技能，等级，经验等），只要你能想到的就归这个类管。你想到但是这个类没有的，就是要**添加的功能**

## 接口

- resetLevel() 重置所有角色等级及其经验
- resetAll() 重置整个后台数据
- getCurrentExps(type: CharacterType) 获取当前经验
  - [CharacterType 是什么](../enum/CharacterType.md)
- setCurrentExps(type: CharacterType, newExps: number) 设置当前经验
- getCharacterLevel(type: CharacterType) 获取角色等级
- setCharacterLevel(type: CharacterType, level: number) 设置角色等级
- getCharacterTotleProperty(cType: CharacterType, levelNum: number) 获取角色总属性
  - [返回值 propertyGroup 是什么](../functionClass/propertyGroup.md)
- getCharacterEquipProperty(cType: CharacterType) 获取角色装备属性
- readLocalEquipData(cType: CharacterType) 读取装备内容
- readLocalBagData() 读取背包内容
- readLocalSkillData(cType: CharacterType) 读取技能内容
- addItemInLocalBagData(itemName: string) 再背包数据中添加物品
- getLevelProperty(level: number) 获取等级固定属性