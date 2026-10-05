# 自用分支的玩法差异

`gravarc-selfhost` 保留官方玩法与实现，只在下述规则上有意不同。

## 烛煌三技能

普通与精锐烛煌的 S3 按 `SKILL_RANGE` 自动开启：技力充足且技能范围内有可选敌人时，无需等待普通攻击。
沉默、自动操作冷却及目标可选性仍由现有 `SkillRuntime` 检查。S1/S2 不变，原始数据表的 `DEFAULT` 不变。

官方的 `ACTIVE_RANGE` 只用于技能范围严格包含普通攻击范围的情况；烛煌的 4-11 不包含整个 3-1，
所以这条自用规则不是对官方实现的等价修复，不应随显示修复一并提交上游。

固定种子的对局结果有意改变：`roster-013`、`roster-015`，`bond-investShip-high`、
`bond-skillfulShip-high`、`bond-yanShip-high`，`boss-boss_1-solo`、`boss-boss_3-solo`、
`boss-boss_5-solo`、`boss-boss_7-solo`、`hidden-boss_9-solo` 及 `coop2-ABYSS-10-boosted`。
它们均包含烛煌；其他场景应保持官方结果。对应基准仅维护在自用分支中。
