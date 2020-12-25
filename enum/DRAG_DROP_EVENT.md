# 拖拽事件枚举

```ts
export enum DRAG_DROP_EVENT {
    TouchStart = 'TouchStart',
    TouchMove = 'TouchMove',
    TouchEnd = 'TouchEnd',
    DragStart = 'DragStart',
    Drag = 'Drag',
    Drop = 'Drop',
}
```

## 枚举描述

```ts
    TouchStart = 'TouchStart',
    TouchMove = 'TouchMove',
    TouchEnd = 'TouchEnd',
```
这三个是引擎自带的事件，这里只是转发，如果有需要可以组测

```ts
    DragStart = 'DragStart',
    Drag = 'Drag',
    Drop = 'Drop',
```
这三个是拖拽的主要事件，分别对应，拖拽开始，拖拽中，拖拽放下