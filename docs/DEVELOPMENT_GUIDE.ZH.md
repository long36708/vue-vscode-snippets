# Vue VSCode 代码片段 - 开发指南

## 概述

本文档为 Vue VSCode Snippets 扩展的开发提供详细的指导，包括如何添加新片段、代码片段格式规范、测试方法和贡献流程。

## 项目结构

```
vue-vscode-snippets/
├── extension.js          # 扩展入口点
├── package.json          # 扩展配置和片段映射
├── snippets/             # 代码片段目录
│   ├── vue.json          # Vue 基础组件片段
│   ├── vue-template.json # 模板指令片段
│   ├── vue-script.json   # 脚本功能片段
│   ├── vue-script-setup.json # Composition API 片段
│   ├── vue-script-vuex.json # Vuex 状态管理片段
│   ├── vue-script-router.json # 路由相关片段
│   ├── vue-pug.json      # Pug 模板片段
│   ├── nuxt-config.json  # Nuxt 配置片段
│   ├── nuxt-script.json  # Nuxt 脚本片段
│   └── ignore.json       # 忽略配置片段
├── docs/                 # 文档目录
│   ├── ARCHITECTURE.ZH.md # 架构文档
│   └── DEVELOPMENT_GUIDE.ZH.md # 本开发指南
├── README.md            # 英文使用文档
├── README.ZH.md         # 中文使用文档
├── CHANGELOG.md         # 英文变更日志
├── CHANGELOG.ZH.md      # 中文变更日志
└── LICENSE             # MIT 许可证
```

## 添加新代码片段

### 步骤 1: 选择正确的片段文件

根据片段的功能领域，选择相应的 JSON 文件：

- **Vue 基础组件**: `snippets/vue.json`
- **模板指令**: `snippets/vue-template.json` 
- **脚本功能**: `snippets/vue-script.json`
- **Composition API**: `snippets/vue-script-setup.json`
- **Vuex 状态管理**: `snippets/vue-script-vuex.json`
- **路由相关**: `snippets/vue-script-router.json`
- **Pug 模板**: `snippets/vue-pug.json`
- **Nuxt 配置**: `snippets/nuxt-config.json`
- **Nuxt 脚本**: `snippets/nuxt-script.json`

### 步骤 2: 定义片段格式

使用标准的 VSCode 片段格式：

```json
{
  "片段显示名称": {
    "prefix": "触发前缀",
    "body": [
      "代码行1",
      "代码行2 $1",
      "代码行3 $2",
      "代码行4 $0"
    ],
    "description": "片段的详细描述"
  }
}
```

### 步骤 3: 占位符语法

使用 `$` 符号定义占位符和制表位：

- `$1`, `$2`, `$3`, ...: 制表位顺序
- `$0`: 最终光标位置
- `${1:默认值}`: 带默认值的占位符
- `${2|选项1,选项2,选项3|}`: 多选项占位符

### 步骤 4: 更新语言映射（如果需要）

如果新片段需要支持新的语言，在 `package.json` 的 `contributes.snippets` 中添加映射：

```json
{
  "language": "vue",
  "path": "./snippets/vue.json"
}
```

## 片段编写规范

### 命名规范

- **前缀命名**: 使用有意义的缩写，如 `vbase` (Vue Base), `vfor` (v-for)
- **描述清晰**: 描述字段应该清楚地说明片段的功能
- **一致性**: 保持与现有片段命名风格一致

### 代码格式

- **缩进**: 使用 2 个空格缩进
- **引号**: 使用双引号
- **换行**: 适当的换行以提高可读性

### 示例：创建一个新的 Vue 组件片段

```json
{
  "Vue Single File Component with Custom Setup": {
    "prefix": "vbase-custom",
    "body": [
      "<template>",
      "\t<div>",
      "\t\t$1",
      "\t</div>",
      "</template>",
      "",
      "<script>",
      "export default {",
      "\tname: '${2:MyComponent}',",
      "\tprops: {",
      "\t\t$3",
      "\t},",
      "\tdata() {",
      "\t\treturn {",
      "\t\t\t$4",
      "\t\t}",
      "\t},",
      "\tmethods: {",
      "\t\t$5",
      "\t}",
      "}",
      "</script>",
      "",
      "<style scoped>",
      "$0",
      "</style>"
    ],
    "description": "自定义 Vue 单文件组件模板"
  }
}
```

## 测试方法

### 本地测试

1. **构建扩展**:
   ```bash
   npm run build
   ```

2. **安装到 VSCode**:
   ```bash
   npm run install
   ```

3. **重启 VSCode** 或重新加载窗口 (Ctrl+Shift+P -> "Developer: Reload Window")

4. **测试片段**: 在合适的文件中输入前缀，验证片段是否正确展开

### 测试要点

- 验证前缀触发是否正确
- 检查占位符顺序和默认值
- 测试在不同文件类型中的表现
- 验证代码格式和缩进

## 贡献流程

### 1. Fork 项目

在 GitHub 上 fork [vue-vscode-snippets](https://github.com/sdras/vue-vscode-snippets) 仓库

### 2. 创建功能分支

```bash
git checkout -b feature/new-snippet
```

### 3. 实现更改

- 添加新的代码片段
- 更新相关文档
- 添加测试用例（如果适用）

### 4. 提交更改

使用有意义的提交信息：

```bash
git commit -m "feat: add new snippet for Vue 3 custom component"
```

### 5. 创建 Pull Request

- 确保 PR 描述清晰说明更改内容
- 引用相关的 issue（如果有）
- 等待代码审查

## 文档要求

所有新片段必须在相应的文档中添加说明：

### 1. 更新 README

在 README.md 和 README.ZH.md 的相应表格中添加片段说明：

```markdown
| 代码片段 | 用途 |
|---------|------|
| `vbase-custom` | 自定义 Vue 组件模板 |
```

### 2. 更新变更日志

在 CHANGELOG.md 和 CHANGELOG.ZH.md 中添加版本变更说明：

```markdown
## 下一个版本

- 新增: 添加自定义 Vue 组件片段 (`vbase-custom`)
```

## 最佳实践

### 1. 保持简洁

片段应该简洁明了，避免过于复杂的逻辑

### 2. 提供有用的默认值

为占位符提供有意义的默认值：

```json
"body": [
  "const ${1:variableName} = ${2:value}"
]
```

### 3. 考虑用户体验

- 制表位顺序应该符合自然的编码流程
- 提供足够的灵活性让用户自定义
- 避免过于特定的实现

### 4. 版本兼容性

- 明确标注片段支持的 Vue 版本
- 为 Vue 2 和 Vue 3 提供相应的片段
- 使用条件注释或其他方式处理版本差异

## 常见问题处理

### 1. 片段不生效

- 检查 `package.json` 中的语言映射
- 验证 JSON 格式是否正确
- 重启 VSCode 重新加载扩展

### 2. 格式问题

- 使用 JSON 格式化工具验证语法
- 检查缩进和引号使用

### 3. 冲突处理

- 确保新片段的前缀不与现有片段冲突
- 如果必须使用相同前缀，提供更具体的变体

## 扩展开发资源

### 官方文档

- [VSCode Snippets Documentation](https://code.visualstudio.com/docs/editor/userdefinedsnippets)
- [VSCode Extension API](https://code.visualstudio.com/api)

### 有用工具

- [Snippet Generator](https://snippet-generator.app/)
- [JSON Formatter & Validator](https://jsonformatter.curiousconcept.com/)

## 版本发布

### 版本号规范

使用语义化版本号：`主版本.次版本.修订版本`

- **主版本**: 不兼容的 API 修改
- **次版本**: 向下兼容的功能性新增
- **修订版本**: 向下兼容的问题修正

### 发布流程

1. 更新 `package.json` 中的版本号
2. 更新变更日志
3. 创建 Git tag
4. 发布到 VSCode 扩展市场

---

通过遵循本指南，您可以有效地为 Vue VSCode Snippets 扩展贡献代码片段，确保代码质量和一致性。