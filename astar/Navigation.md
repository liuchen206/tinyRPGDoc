# 导航信息

存储管理了网格（地图）上的可以行走点和不可行走点，作为寻路的依据。寻路时还有设置起始点和终点的功能

# 外部接口

- reset() 重置寻路信息
- getNode(numCol: number, numRow: number) 获取一个搜索节点
- setStartNode(numCol: number, numRow: number) 设置起点
- setEndNode(numCol: number, numRow: number) 设置终点
- setWalkable(numCol: number, numRow: number, walkable: boolean) 设置节点是否可行走
 
