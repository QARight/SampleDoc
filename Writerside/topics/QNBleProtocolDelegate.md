# QNBleProtocolDelegate

蓝牙协议代理接口，该接口用来实现，自己管理蓝牙连接。

## 方法

### writeCharacteristicValue

写入特征值
#### 参数

|名称|类型|说明|
|:--|:--|:--|
|service_uuid |string|蓝牙服务的UUID|
|characteristic_uuid|string|特征值的UUID|
|data|byte[]/NSData|需要写入的数据，安卓是字节数组，iOS是NSData对象|
|device|[QNBleDevice](./QNBleDevice.md)|需要写入数据的设备|

示例代码
```java
//安卓
//根据服务UUID和特征值UUID先查找到特征值
characteristic.value = data;
gatt.writeCharacteristic(characteristic)
```

```swift
//iOS swift
//根据服务UUID和特征值UUID先查找到特征值
peripheral.writeValue(data, for: characteristic, type: CBCharacteristicWriteType.withResponse)
```
### readCharacteristicValue

读取特征值

|名称|类型|说明|
|:--|:--|:--|
|service_uuid |string|蓝牙服务的UUID|
|characteristic_uuid|string|特征值的UUID|
|device|[QNBleDevice](./QNBleDevice.md)|需要写入数据的设备|
```java
//安卓
//根据服务UUID和特征值UUID先查找到特征值
gatt.readCharacteristic(characteristic)
```
```swift
//iOS swift
//根据服务UUID和特征值UUID先查找到特征值
peripheral.readValue(for: characteristic)
```