# buff 数据结构

详细的 buff 数据通过 name 字段读表获取
```ts
export class buffStruct {
    name: string = ''; // 状态名字
    remainTime: number = 0; // 持续时间
    constructor(name, time) {
        this.name = name;
        this.remainTime = time;
    }
}
```