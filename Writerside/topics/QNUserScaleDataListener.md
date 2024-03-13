# QNUserScaleDataListener

 用户秤设备数据监听器，该设备相关测量数据在这里回调，该 listener 继承于 QNScaleDataListener

## 方法

### registerUserComplete

用户秤设备注册用户成功，注册用户成功后设备会返回该用户在秤端的序列号

#### 参数

| 名称   | 类型                            | 说明         |
| :----- | :------------------------------ | :----------- |
| device | [QNBleDevice](./QNBleDevice.md) | 蓝牙设备对象 |
| user   | [QNUser](./QNUser.md)           | 用户对象     |

### visitUserComplete

用户秤设备访问用户成功，访问用户成功后设备会返回当前访问用户信息

#### 参数

| 名称   | 类型                            | 说明         |
| :----- | :------------------------------ | :----------- |
| device | [QNBleDevice](./QNBleDevice.md) | 蓝牙设备对象 |
| user   | [QNUser](./QNUser.md)           | 用户对象     |

### getLastDataHmac

获取最近一次测量数据hmac,用于访客模式测量

#### 参数

| 名称   | 类型                            | 说明         |
| :----- | :------------------------------ | :----------- |
| device | [QNBleDevice](./QNBleDevice.md) | 蓝牙设备对象 |
| user   | [QNUser](./QNUser.md)           | 用户对象     |
