# 游戏内拖拽游戏对象

组件的作用是，处理玩家在输入拖拽游戏对象时的逻辑
- ![代码](img/drag.PNG)
- 
## 组件逻辑

当玩家拖拽时，对象随着拖拽移动，当放置时，判断放置的位置是否可以放置，不能则放回起点

## 外部接口

- onDragStart() 拖拽开始
- moveOBJ(obj: cc.Node, e: cc.Event.EventTouch) 移动对象
- onDragMoving() 拖拽中
- isDropAble() 是否能放置
- align() 对齐
- onDragEnd() 拖拽完成

## 使用实例

该示例融入 [游戏对象总体设计](./OBJEditor.md) 中。