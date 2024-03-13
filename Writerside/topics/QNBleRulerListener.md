# QNBleRulerListener

蓝牙围度尺 设备链接状态 测量数据监听器

## 方法

## onRulerDeviceDiscover

发现围度尺，扫描到围度尺设备后，会马上回调

#### 参数

|名称|类型|说明|
|:--|:--|:--|
|device| [QNBleRulerDevice](./QNBleRulerDevice.md)| 发现围度尺设备 |

## onRulerConnecting

正在进行连接设备，在调用连接设备后，会马上回调

#### 参数

|名称|类型|说明|
|:--|:--|:--|
|device| [QNBleRulerDevice](./QNBleRulerDevice.md)| 状态变化的围度尺设备对象|

## onRulerConnected

设备已连接成功

#### 参数

|名称|类型|说明|
|:--|:--|:--|
|device| [QNBleRulerDevice](./QNBleRulerDevice.md)| 状态变化的围度尺设备对象|

## onRulerDisconnected

蓝牙断开了连接

#### 参数

|名称|类型|说明|
|:--|:--|:--|
|device| [QNBleRulerDevice](./QNBleRulerDevice.md)| 状态变化的围度尺设备对象|

## onRulerConnectFail

出现了连接错误

#### 参数

|名称|类型|说明|
|:--|:--|:--|
|device| [QNBleRulerDevice](./QNBleRulerDevice.md)| 状态变化的围度尺设备对象|


### onGetReceiveRealTimeData

实时测量数据

#### 参数

| 名称   | 类型                            | 说明         |
| :----- | :------------------------------ | :----------- |
| data | [QNBleRulerData](./QNBleRulerData.md) | 测量数据信息 |
|device| [QNBleRulerDevice](./QNBleRulerDevice.md)| 状态变化的围度尺设备对象|

### onGetReceiveResultData

用户确认测量数据

#### 参数

| 名称   | 类型                            | 说明         |
| :----- | :------------------------------ | :----------- |
| data | [QNBleRulerData](./QNBleRulerData.md) | 测量数据信息 |
|device| [QNBleRulerDevice](./QNBleRulerDevice.md)| 状态变化的围度尺设备对象|
