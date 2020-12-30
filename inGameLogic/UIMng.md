# 游戏内的 UI 管理模块

管理游戏内特有的 UI 相关逻辑
- ![代码](./img/game.PNG)
  
  
## 外部接口

- playerNumbEffect(showNumb: number, node: cc.Node) 播放数字特效。主要是伤害和治疗信息
- backHall() 返回大厅
- buffAddUpdate(target: OBJEditor) 添加 buff 更新(非编辑场景适用)
- onBagClick() 点击背包按钮 (非编辑场景适用)
- makeSKillBtns(cType: CharacterType) 构建技能按钮 [什么是 CharacterType](../enum/CharacterType.md)
- makeBuffs(buffs: buffStruct[]) 构建状态 [什么是 buffStruct](../functionClass/buffStruct.md)
- popRewardItem(name: string) 弹出物品获取示意