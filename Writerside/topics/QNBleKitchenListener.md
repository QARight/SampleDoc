# QNBleKitchenListener

蓝牙厨房秤 设备链接状态 测量数据监听器

## 方法

## onBleKitchenConnecting

正在进行连接设备，在调用连接设备后，会马上回调

#### 参数

|名称|类型|说明|
|:--|:--|:--|
|device| [QNBleKitchenDevice](./QNBleKitchenDevice.md)| 状态变化的蓝牙厨房秤对象|

## onBleKitchenConnected

设备已连接成功
会回调设备对象

## onBleKitchenDisconnected

蓝牙断开了连接

## onBleKitchenConnectError

出现了连接错误

#### 参数

|名称|类型|说明|
|:--|:--|:--|
|device|[QNBleKitchenDevice](./QNBleKitchenDevice.md)| 厨房秤设备对象 |
|errorCode|int | 错误码参考[附表-错误码](../attouched_list/error_code.md)，IOS的第二个参数使用系统错误对象|


### onGetBleKitchenWeight

蓝牙厨房秤测量数据回调

#### 参数

| 名称   | 类型                            | 说明         |
| :----- | :------------------------------ | :----------- |
| device | [QNBleKitchenDevice](./QNBleKitchenDevice.md) | 厨房秤设备对象 |
| weight   | double           | 秤端重量, 数值为g单位下重量     |


### onBleKitchenStateChange

蓝牙厨房秤测量数据回调

#### 参数

| 名称   | 类型                            | 说明         |
| :----- | :------------------------------ | :----------- |
| device | [QNBleKitchenDevice](./QNBleKitchenDevice.md) | 厨房秤设备对象 |
| scaleState | int | 参考[秤状态码](../attouched_list/scale_state.md) |
