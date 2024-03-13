# QNBleConnectionChangeListener

蓝牙连接变化监听接口


## onConnecting

正在进行连接设备，在调用连接设备后，会马上回调

#### 参数

|名称|类型|说明|
|:--|:--|:--|
|device| [QNBleDevice](./QNBleDevice.md)| 状态变化的蓝牙设备对象|

## onConnected

设备已连接成功
会回调设备对象

## onServiceSearchComplete

设备的服务搜索完成，正常情况下会在 onConnected后面调用

## onStartInteracting

设备开始交互, 正常情况下会在 onServiceSearchComplete后面调用

## onDisconnecting

正在断开连接，调用断开连接时，会马上回调


## onDisconnected

蓝牙断开了连接

## onConnectError

出现了连接错误

#### 参数

|名称|类型|说明|
|:--|:--|:--|
|device|[QNBleDevice](./QNBleDevice.md)| | 蓝牙设备对象|
|errorCode|int | 错误码参考[附表-错误码](../attouched_list/error_code.md)，IOS的第二个参数使用系统错误对象|

