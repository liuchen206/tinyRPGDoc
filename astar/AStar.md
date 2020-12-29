# 搜索主逻辑

构造时传入寻路数据，可以计算两点之间的路径

## 接口

- 构造函数
```ts
constructor(coverCol?: number, coverRow?: number, searchDir?: SearchDirection) {
        if (coverCol) this._coverCol = coverCol;
        if (coverRow) this._coverRow = coverRow;
        if (searchDir) this._searchDir = searchDir;
    }
```

- tryFindPath(nav: Navigation) // 尝试寻找路径
- 最终路径
```ts
public get caculatePath(): Array<SearchNode> {
    return this._caculatePath;
}
```