# QNWiFiConfig

WiFi信息类

### 属性

|名称|类型|是否必须| 说明|
|:--|:--|:--|:--|
|ssid |String| Y |wifi名称(长度必须少于32个字节)|
|pwd |String| Y |wifi密码(有密码时，密码长度必须大于或等于8个字节且小于64个字节<br>无密码时，可以传nil)|
|serveUrl| String| N | 数据传输地址，`用户秤设备设置有效`，`其他设备可设为 null`，格式要求http://hostname:port/path/, 最大长度为 128 个字节|


## 方法

### checkSSIDVail

检验WiFi名称的有效性

#### 返回值

类型：Boolean

### checkPWDVail

检验WiFi密码的有效性

#### 返回值

类型：Boolean
