# Linux工厂方法模式类图  
```mermaid  
classDiagram  
  class PlatformDriver {  
    +probe()  // 探测设备  
    +remove() // 移除设备  
  }  
  class PlatformDevice {  
    +driver_data  // 设备私有数据  
  }  
  PlatformDriver --> PlatformDevice : 创建/关联  
  

```mermaid
sequenceDiagram
    participant Driver as 驱动模块
    participant Kernel as 内核
    Driver ->> Kernel: platform_driver_register()  // 注册驱动
    Kernel ->> Driver: 调用 probe() 检测设备
    Driver ->> Kernel: 返回设备实例