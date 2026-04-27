# 雪球三分法速算器 | Snowball Trifecta Calculator

一个专为雪球三分法投资者设计的基金配置解析工具。

## 简介

本工具用于快速解析和校验雪球三分法（债券/股票/商品）的基金配置 JSON 数据，帮助投资者：

- 解析基金配置 JSON，自动识别各大类资产
- 展示债券、股票、商品三大类资产占比
- 自动校验各大类内部权重之和是否等于该类总占比
- 快速定位配置不平衡的问题

## 使用方法

1. 从雪球或其他平台复制基金配置 JSON
2. 粘贴到工具输入框
3. 点击「解析」按钮
4. 查看各大类占比和权重校验结果

## 配置格式示例

```json
{
  "categories": [
    {
      "type": "bond",
      "name": "债券基金",
      "totalPercent": 50,
      "funds": [
        {
          "name": "鹏华稳福中短债债券 A",
          "code": "015530",
          "weight": 10.00
        }
      ]
    },
    {
      "type": "stock",
      "name": "股票基金",
      "totalPercent": 45,
      "funds": [...]
    },
    {
      "type": "commodity",
      "name": "商品基金",
      "totalPercent": 5,
      "funds": [...]
    }
  ]
}
```

## 技术栈

- Vue.js 3
- Vite

## License

GNU GPL v3
