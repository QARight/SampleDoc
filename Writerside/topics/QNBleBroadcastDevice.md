# QNBleBroadcastDevice

Yolanda广播秤蓝牙设备对象

广播秤是一款无需连接，通过接收设备发出的广播获取相关数据的设备。该秤与普通蓝牙秤不同，区别在于普通蓝牙秤在扫描到周围的设备信息时，可以发起对周围某一设备的连接，从而可以选择是否停止扫描周围的设备信息，而不影响从已连接设备中获取相关的测量信息。

然而广播秤由于是通过获取周围设备的广播数据进而分析相关的测量信息，无需对某一设备进行连接。因此倘若在使用广播秤进行测量过程中，停止了对周围设备的扫描，意味着无法获取这次的测量数据。

### 属性

|名称|类型|说明|
|:--|:--|:--|
|mac |String| MAC地址，sdk会根据扫描到的广播信息解析，同一台设备，安卓和IOS返回的结果一样。每台设备唯一|
|name |String|型号名称，SDK会识别扫描到的设备型号，如果识别不出来，则返回一个默认的型号名称，Scale|
|modeId |String|型号标识|
|bluetoothName |String|蓝牙名称，这个是硬件设备广播名称，不同于name。APP以name为准。|
|RSSI |int|信号强度，是一个负数，一般在-30~-100 之间，数值越大，表示信号强度越大，同一个设备可能回调多次，每次回调时，可能信号强度的值不一样。|
|supportUnitChange |boolean|是否支持协议方式修改秤体单位|
|unit |int|秤体当前显示的单位<br /> 0 为 kg，默认值 <br />1 为 lb <br />2 为 斤|
|weight |double|当前秤体显示的体重数值|
|isComplete |boolean|是否测量完成|
|measureCode |int|测量完成后数据编码，测量完成后可能收到多条相同广播数据，因此该字段用于区分相邻时间内收到多条测量完成数据是否是同一次测量数据|


## 方法

### generateScaleData

当isComplete字段为true时，可以调用该方法获取相关的测量数据

获取测量数据

#### 参数

|名称|类型|说明|
|:--|:--|:--|
|user |[QNUser](./QNUser.md)|用户对象|
|callback|[QNResultCallback](./QNResultCallback.md)|返回该方法调用是否成功|

#### 返回值

类型：[QNScaleData](./QNScaleData.md)

Yolanda测量数据，包含了体重，BMI、体脂率等数据。

### syncUnit

当设备supportUnitChange字段为true时，表明设备允许通过协议的方式修改，这时可以使用该方法修改单位

当方法调用成功后，SDK会发出蓝牙广播信号，当目标设备的单位已经修改或10s后SDK将停止广播

该方法调用后将取消之前同步单位的操作，比如正在同步A设备的单位，此时同步B设备的单位时，SDK将会先取消A设备单位的同步，再启动B设备的单位同步

该单位为[QNConfig](./QNConfig.md)中设置的单位

#### 参数

|名称|类型|说明|
|:--|:--|:--|
|callback|[QNResultCallback](./QNResultCallback.md)|返回该方法调用是否成功|
