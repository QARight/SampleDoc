# QNUserScaleConfig

 用户秤设备配置类，由它来控制用户秤操作

配置说明:

- wifiConfig = null && curUser != null时，SDK仅进行注册访问等操作
- wifiConfig != null && curUser == null时，SDK仅对设备进行配网操作
- wifiConfig != null && curUser != null时，SDK会先进行配网，配网成功后进行注册访问等操作；若配网失败，则不会有注册访问等操作


## 属性

| 名称        | 类型                             |  是否必须  | 说明                                                                                         |
| :---------- | :--------------------------------| :--------------------------------  | :---------------------------------------------------------------- |
| wifiConfig  | [QNWiFiConfig](./QNWiFiConfig.md) | N | 配网信息。针对支持WiF设备,当 value 值为 null 时，不进行配网操作 ；当 value 值为 QNWiFiConfig 对象时，根据对象中的值进行配网设置       |
| userlist |  [QNUser](./QNUser.md)               | N | 已注册秤端用户列表, 用于同步删除秤端多余用户。当列表为null时,不会进行同步用户列表操作                                                     |
| curUser     | [QNUser](./QNUser.md)             | N | 当前测量用户，当只需配网无需测量时，可设置为null                                         |
| isVisitor   | Boolean                           | N | 是否使用访客进行测量，使用访客进行测量时不必设置 [QNUser](./QNUser.md)无需设置 index、secret|
