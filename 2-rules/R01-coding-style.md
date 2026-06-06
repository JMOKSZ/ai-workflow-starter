# R01 — 编码规范

> **用途**: 告诉AI你的代码应该长什么样。  
> **改法**: 删掉不相关的，补充你团队的特殊要求。

---

## 命名规范

- **变量/函数**: `camelCase` / `snake_case` / （选你用的）
- **类/类型**: `PascalCase`
- **常量**: `UPPER_SNAKE_CASE`
- **文件/目录**: `kebab-case` / `snake_case`
- 私有方法前缀：`_` / `#`

## 注释规范

- 公共 API 必须写 docstring
- // TODO: 标明未完成但已知的问题
- // HACK: 标明临时解决方案
- 不要注释"显而易见"的代码

## 错误处理

- 不要吞异常（除非明确注释原因）
- 使用自定义异常类，不要抛 `Exception` / `Error` 裸类
- 所有外部调用（DB、API、文件）必须 try/catch

## 函数规范

- 一个函数不超过 50 行
- 一个函数只做一件事（单一职责）
- 避免嵌套超过 3 层

## 提交规范

- 提交信息格式：`type(scope): description`
  - type: `feat` `fix` `refactor` `test` `docs` `chore`
  - scope: 模块名
  - 示例: `feat(auth): add OAuth2 login flow`
