# 游戏对象头顶UI信息

- 组件的功能有三个，显示名字，显示hp，显示会话
- 游戏对象 相关的代码都在一窝，不在挨个截图了
- ![代码](img/drag.PNG)

## 对外接口

-  hideAll() 隐藏所有
-  setName(name: string) 设置角色名字
-  setHpBar(rate: number) 设置hp槽
-  say(words: string) 对象上方弹出对话内容