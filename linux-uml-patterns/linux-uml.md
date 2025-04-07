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
  
