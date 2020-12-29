# 搜索节点

代码很简单，一个标准的 astar 的搜索节点的数据结构。如需具体了解每个参数的意义。请自己阅读代码或者百度，相信你哟
```ts
export enum SearchStatus {
    NONE = 1,
    CLOSE,
    OPEN
}
export default class SearchNode {
    public col: number = 0;
    public row: number = 0;
    // f = g + h
    public f: number; // 总cost
    public g: number; // 起始点到本节点的cost
    public h: number; // 本节点到终点的估计cost
    public Status: SearchStatus = SearchStatus.NONE;
    public parentSearchNode: SearchNode = null;
    public walkAble: boolean = true;
    public constructor(col: number, row: number) {
        this.col = col;
        this.row = row;
    }
}
```