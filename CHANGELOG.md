# Changelog

## 2026-06-17

### 升级所有 npm 依赖到最新版本

将前端依赖从 2023 年版本升级到 2026 年最新版本。

#### Dependencies

| 包名 | 旧版本 | 新版本 |
|------|--------|--------|
| `vue` | `^3.3.4` | `^3.5.38` |
| `element-plus` | `^2.4.1` | `^2.14.2` |
| `pinia` | `^2.1.7` | `^3.0.0` |
| `@element-plus/icons-vue` | `^2.1.0` | `^2.3.2` |

#### DevDependencies

| 包名 | 旧版本 | 新版本 |
|------|--------|--------|
| `vite` | `^4.4.5` | `^8.0.0` |
| `@vitejs/plugin-vue` | `^4.2.3` | `^6.0.7` |
| `typescript` | `^5.0.2` | `^5.8.0` |
| `vue-tsc` | `^1.8.5` | `^3.3.5` |
| `unplugin-auto-import` | `^0.16.6` | `^21.0.0` |
| `unplugin-vue-components` | `^0.25.2` | `^31.0.0` |

#### TypeScript 配置

- `tsconfig.json`: `target` / `lib` 从 `ES2020` 更新为 `ES2022`

### 更新 CI/CD 构建流程

升级 GitHub Actions workflow 中的所有工具版本。

#### GitHub Actions

| Action | 旧版本 | 新版本 |
|--------|--------|--------|
| `actions/checkout` | `v3` | `v6` |
| `actions/setup-go` | `v4` | `v6` |
| `actions/setup-node` | `v3` | `v6` |
| `actions/upload-artifact` | `v3` | `v4` |

#### 工具版本

| 工具 | 旧版本 | 新版本 |
|------|--------|--------|
| Go | `1.20` | `1.26` |
| Node.js | `18` | `22` |
| Wails CLI | `v2.6.0` | `v2.12.0` |

#### Linux 构建环境

- `libwebkit2gtk-4.0-dev` → `libwebkit2gtk-4.1-dev`（Ubuntu 24.04+ 兼容）
- 构建命令添加 `-tags webkit2_41` 标志

### 环境要求

- Node.js ≥ 20.19（Vite 8 和 unplugin 系列要求）
- Go ≥ 1.26
