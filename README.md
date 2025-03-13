# @hs18/es-utils

`@hs18/es-utils` 是一个通用工具库，提供了一些常用的格式化和验证功能。以下是本项目的详细介绍、安装方法、使用示例和 API 文档。

## 安装

可以通过 npm 或 yarn 安装：

```bash
npm install @hs18/es-utils
```

或

```bash
yarn add @hs18/es-utils
```

## 使用示例

### 引入模块

```javascript
import { Format, Validate } from '@hs18/es-utils';
```

### 格式化工具

#### `formatMoney(money, symbol = "", decimals = 2)`

- **参数**:
  - `money` (Number/String): 需要格式化的金额。
  - `symbol` (String, 可选): 货币符号，默认为空字符串。
  - `decimals` (Number, 可选): 小数位数，默认为 2。
  
- **返回值**: 格式化后的金额字符串。

- **示例**:

```javascript
console.log(Format.formatMoney(12341234.246, '$')); // 输出: $ 12,341,234.25
```

### 验证工具

#### `mobileCheck(value)`

- **参数**:
  - `value` (String): 需要校验的手机号。

- **返回值**: 布尔值，表示手机号是否合法。

- **示例**:

```javascript
console.log(Validate.mobileCheck('13800138000')); // 输出: true
console.log(Validate.mobileCheck('12345678901')); // 输出: false
```

#### `IDCardCheck(value)`

- **参数**:
  - `value` (String): 需要校验的身份证号。

- **返回值**: 布尔值，表示身份证号是否合法。

- **示例**:

```javascript
console.log(Validate.IDCardCheck('11010519491231002X')); // 输出: true
console.log(Validate.IDCardCheck('123456789012345678')); // 输出: false
```

#### `emailCheck(value)`

- **参数**:
  - `value` (String): 需要校验的邮箱地址。

- **返回值**: 布尔值，表示邮箱地址是否合法。

- **示例**:

```javascript
console.log(Validate.emailCheck('example@example.com')); // 输出: true
console.log(Validate.emailCheck('invalid-email')); // 输出: false
```

## 贡献指南

欢迎贡献代码！请遵循以下步骤：

1. Fork 仓库。
2. 创建新分支 (`git checkout -b feature/your-feature`)。
3. 提交更改 (`git commit -m 'Add some feature'`)。
4. 推送到分支 (`git push origin feature/your-feature`)。
5. 提交 Pull Request。

## 许可证

本项目采用 [ISC License](https://opensource.org/licenses/ISC) 许可证。

---

更多详细信息请参考 [GitHub 仓库](https://github.com/hs185556/es-utils)。
```