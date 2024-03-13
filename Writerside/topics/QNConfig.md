# QNConfig

SDK配置对象，由它来控制扫描的行为，通过它设置SDK的一些行为

## 属性


|名称|类型|说明|
|:--|:--|:--|
|onlyScreenOn  |Boolean|是否只返回已开机（亮屏）的设备，默认为false，即返回开机和不开机的秤。|
|allowDuplicates  |Boolean|同一个设备是否返回多次，一般来说，设备会一直发射蓝牙广播，扫描时系统会对同一个设备回调多次，SDK会对同一个设备做处理，让一次扫描过程中，一个设备只返回一次，商家可以设置这个参数，SDK则直接每次都进行返回。默认false（该字段对[onBroadcastDeviceDiscover](./QNBleDeviceDiscoveryListener.md#onbroadcastdevicediscover)监听无效）|
|duration  |int|扫描持续时间,单位 ms，默认为0，即一直进行扫描，除非APP调用了stopBleDeviceDiscovery.不为0时，最小值为 3000ms 则会延时 duration ms的时间后，自动停止扫描。（若有广播秤的接入需要注意该字段的设置,见[广播秤工作原理](./QNBleBroadcastDevice.md)）|
|connectOutTime  |long|(安卓专属)连接设备限定时间,单位 ms，默认为10000，即调用连接开始10秒之内，如果无法完成整个连接过程，就会停止连接并[回调错误](../api/QNBleConnectionChangeListener.md#onConnectError);设置的值小于等于0时，表示不进行回调;设置的值小于3000且大于0时，表示超时时间为3000ms.如果在连接超时之前，已经停止了连接，即使期间没有成功连接设备也不会有错误回调.|
|unit |int|0 为 kg，默认值 <br />1 为 lb,磅，所有秤都能够支持这个单位 <br />2 为 斤，秤端如果不支持，则会显示kg <br />3 为 st+lb，英石，秤端如果不支持，则会显示lb，的数值<br />4 为st, 秤端如果不支持，则会显示lb的数值|
|showPowerAlertKey |bool|默认为false,为true时，当SDK初始化，并且蓝牙处于关闭状态，系统会弹框提示蓝牙状态，详情请参考Apple Developer Documenttation =\> CoreBluetooth =\> CBCentralManager =\>  Central Manager Initialization Options|
|setNotCheckGPS |bool|(安卓专属)默认为false,为true时，SDK进行扫描时不会进行GPS权限做判断，继续执行扫描|
|enhanceBleBoradcast |bool|是否需要在扫描时启动强化广播秤信号(对普通秤无效，该选项只针对广播秤)|
### unit

端显示的单位，不设置的话，SDK默认为kg，设置后会保存本地，如果当前已经有连接的设备，会尽量实时更新秤端的单位显示。

> SDK会一直返回kg的数值。APP需要自己进行数值的转换。

## 方法

### save

保存修改后的设置

#### 参数

|名称|类型|说明|
|:--|:--|:--|
|callback|[QNResultCallback][1]|返回该设置操作是否成功|

[1]:	./QNResultCallback.md
