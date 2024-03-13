### decodeShareData

获取共享秤测量数据

将共享秤测量结果后的扫描字符串传入该方法获取测量结果数据

#### 返回值

类型: [QNShareData](./QNShareData.md)

#### 参数

|名称|类型|说明|
|:--|:--|:--|
|qnCode|String|URL|
|user|[QNUser](./QNUser.md)|用户信息|
|validTime|long|二维码有效时间,单位s,设置为0时则一直有效。设置的值不能为负数|
|callback|[QNResultCallback](./QNResultCallback.md)|安卓是接口，IOS用block或闭包）回调方法，返回初始化的结果，错误码参考附表。|