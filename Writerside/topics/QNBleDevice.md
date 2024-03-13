# QNBleDevice

Yolanda蓝牙设备对象，目前只是指体脂称，后续可能会延续到手环

### 属性

|名称|类型|说明|
|:--|:--|:--|
|mac |String| MAC地址，sdk会根据扫描到的广播信息解析，同一台设备，安卓和IOS返回的结果一样。每台设备唯一|
|name |String|型号名称，SDK会识别扫描到的设备型号，如果识别不出来，则返回一个默认的型号名称，Scale|
|modeId |String|型号标识|
|bluetoothName |String|蓝牙名称，这个是硬件设备广播名称，不同于name。APP以name为准。|
|RSSI |int|信号强度，是一个负数，一般在-30~-100 之间，数值越大，表示信号强度越大，同一个设备可能回调多次，每次回调时，可能信号强度的值不一样。|
|isScreenOn |Boolean|是否已开机，秤的屏幕亮着，则是开机，否则未开机。|
|isSupportWifi |Boolean|是否支持Wifi功能，如果支持，则可以调用配网等操作|
|maxUserNum |int|秤最大支持注册用户数|
|registeredUserNum |int|秤已注册用户数|
|isSupportEightElectrodes |boolean|是否支持八电极设备|
|displayModuleType | [QNDisplayModuleType](../attouched_list/display_module_type.md)| 显示模块类型 |
