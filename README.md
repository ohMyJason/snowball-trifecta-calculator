---
permalink: /index.html
---

# 雪球三分法速算器 | Snowball Trifecta Calculator

> 解决雪球组合不能等比例增减大类资产占比的痛点

## 痛点

雪球基金的三分法配置（债券/股票/商品）有一个功能缺失：

**雪球不支持等比例增减大类资产占比。**

当你想调整某个大类的总占比时，雪球不会自动重新计算该类下各基金的权重。这意味着你需要：

1. 手动拿出计算器，算出每只基金的新权重
2. 确保新权重之和等于调整后的总占比
3. 逐个修改每只基金的占比

**这很麻烦**，尤其是当一个大类下有 10+ 只基金时。

## 这个工具能帮你

本工具自动完成上述繁琐的计算：

1. **粘贴配置** — 从雪球复制基金配置 JSON
2. **调整大类占比** — 修改债券/股票/商品的 totalPercent
3. **自动计算** — 工具自动等比例缩放各大类内部基金的 weight
4. **一键复制** — 输出新的配置 JSON，直接粘贴回雪球

不用再手动按计算器了。

## 使用方法

访问项目页面：https://ohmyjason.github.io/snowball-trifecta-calculator

## 功能

- 解析雪球基金配置 JSON
- 展示债券/股票/商品三大类资产占比
- 自动校验权重之和是否等于 totalPercent
- **等比例缩放各大类内部基金权重**
- 一键复制新配置

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

## License

GNU GPL v3
