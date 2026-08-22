# Rules

本仓库用于存放个人维护的分流规则。

## 目录

- `RuleSet`：纯文本 classical 规则，可供 Egern 及支持 text rule-provider 的 Mihomo 客户端使用。
- `Mihomo`：标准 YAML classical rule-provider，适用于 Clash Party、FlClash、Clash Verge Rev 等 Mihomo 内核客户端。

## Mihomo 使用示例

```yaml
rule-providers:
  Perplexity:
    type: http
    behavior: classical
    format: yaml
    url: "https://raw.githubusercontent.com/hbchnz/Rules/main/Mihomo/Perplexity.yaml"
    path: ./ruleset/Perplexity.yaml
    interval: 86400

rules:
  - RULE-SET,Perplexity,AI
```

`AI` 需要替换为配置中实际存在的策略组名称；自定义 `RULE-SET` 应放在较宽泛的规则及最终 `MATCH` 之前。
