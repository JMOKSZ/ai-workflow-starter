# R02 — 数据库规范

> **用途**: 告诉AI数据库怎么改、怎么写迁移。

---

## 变更原则

- 所有表结构变更必须通过迁移文件，不能手动改DB
- 只新增列和表，不改 / 删已有的（除非明确要求）
- 加索引必须评估查询场景

## 命名

- 表名: `snake_case` 复数（`users`, `orders`）
- 列名: `snake_case`（`created_at`, `order_id`）
- 主键: `id`（自增 / UUID）
- 外键: `{表名}_id`（`user_id`）
- 时间戳: `created_at`, `updated_at`

## 迁移模板

```sql
-- {{描述这次迁移做什么}}
ALTER TABLE {{表名}} ADD COLUMN {{列名}} {{类型}} {{约束}};
```

## 🚫 禁止

- 禁止在生产环境直接执行未经Review的SQL
- 禁止删除列（先用 deprecated 过渡）
- 禁止在循环里逐条执行SQL
