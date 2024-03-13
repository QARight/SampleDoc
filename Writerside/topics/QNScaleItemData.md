# QNScaleItemData

Yolanda体脂称单个指标对象，包含了该指标生成报告的基本数据。

## 属性

|名称|类型|说明|
|:--|:--|:--|
|type |int|该指标的类型，具体参考附表|
|value |double|该指标的值，为了通用，该字段会直接返回double，如果该项值是int类型，app需要自己判断类型然后转化|
|valueType |int|指标值的类型，0 为 double，1 为 int |
|name  |String|该指标的名称，全部为英文名称，提供附表转化中文名称|





