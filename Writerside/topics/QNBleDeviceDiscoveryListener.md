# QNBleDeviceDiscoveryListener

扫描设备监听回调类

## 方法

### onDeviceDiscover

#### 参数

|名称|类型|说明|
|:--|:--|:--|
|device  |QNBleDevice|扫描到的蓝牙设备|

### onBroadcastDeviceDiscover

广播秤设备相关信息的回调

SDK会返回能扫描到周围的所有广播秤的设备信息，app需要自行处理这些信息

>同时为了兼容已接入广播秤的客户，原onDeviceDiscover方法中回调广播秤设备信息将保持不变。强烈建议有接入广播秤的客户使用该API

#### 参数

|名称|类型|说明|
|:--|:--|:--|
|device  |[QNBleBroadcastDevice](./QNBleBroadcastDevice.md)|扫描到广播秤|


### onKitchenDeviceDiscover

厨房秤设备相关信息的回调

SDK会返回能扫描到周围的所有厨房秤的设备信息，app需要自行处理这些信息

#### 参数

|名称|类型|说明|
|:--|:--|:--|
|device  |[QNBleKitchenDevice](./QNBleKitchenDevice.md)|扫描到厨房秤|

### onStartScan

成功启动扫描后触发该方法

### onStopScan

停止扫描后的回调

自动停止(定时)或调用stopScan停止后，都会触发该回调

### onScanFail

没有扫描成功则回调(只有Android才会有这个回调)

#### 参数

|名称|类型|说明|
|:--|:--|:--|
|code|int | 参考[扫描状态码](../attouched_list/scan_error.md)|





