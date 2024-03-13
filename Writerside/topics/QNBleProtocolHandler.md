# QNBleProtocolHandler

Yolanda蓝牙协议处理类，配合[QNBleProtocolDelegate](./QNBleProtocolDelegate.md) 可实现客户自己管理蓝牙连接。

称重数据的回调，还是通过[QNScaleDataListener](./QNScaleDataListener.md)来回调。蓝牙连接状态等相关信息不再回调[QNBleConnectionChangeListener](./QNBleConnectionChangeListener.md)


## 方法

### prepare

通知协议处理器做初始化的工作

#### 参数

|名称|类型|说明|
|:--|:--|:--|
|service_uuid |string|主服务的UUID|


### onGetBleData

|名称|类型|说明|
|:--|:--|:--|
|service_uuid |string|蓝牙服务的UUID|
|characteristic_uuid|string|特征值的UUID|
|data|byte[]/NSData|蓝牙回传的数据（不论是读取的数据还是，蓝牙回调的数据，都是传到这个方法），安卓是字节数组，iOS是NSData对象|
