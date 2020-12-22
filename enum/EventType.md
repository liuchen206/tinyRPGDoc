# 事件类型枚举

```ts
export enum EventType {
    TEST_EVENT = "TEST_EVENT",
    New_Event1 = "New_Event1",
    New_Event2 = "New_Event2",
    
}
```
## 枚举描述
- 枚举值描述了在客户端定义的所有事件类型
- **注意** 这是个可变动的枚举值，每当需要定义一个新的事件的时候，会在此枚举中添加一个值.