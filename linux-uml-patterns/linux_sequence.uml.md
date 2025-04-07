# Linux工厂方法模式顺序图
```mermaid
sequenceDiagram
    participant Driver as 驱动模块
    participant Kernel as 内核
    Driver ->> Kernel: platform_driver_register()  // 注册驱动
    Kernel ->> Driver: 调用 probe() 检测设备
    Driver ->> Kernel: 返回设备实例