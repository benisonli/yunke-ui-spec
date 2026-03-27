# 云客 CRM Ant Design Token 与组件映射清单

> 用途：给前端、UI、AI 页面生成器统一对齐的轻量落地清单。  
> 技术基线：Ant Design

---

## 1. 主题 Token 建议

```ts
export const yunkeTheme = {
  token: {
    colorPrimary: '#1677FF',
    colorSuccess: '#00CA75',
    colorWarning: '#FF8008',
    colorError: '#FF525C',
    colorText: '#333333',
    colorTextSecondary: '#545759',
    colorTextTertiary: '#8C8C8C',
    colorBorder: '#EBECED',
    colorBgLayout: '#F5F7FA',
    colorBgContainer: '#FFFFFF',
    borderRadius: 6,
    borderRadiusLG: 10,
    borderRadiusSM: 4,
    fontSize: 14,
    fontFamily: 'PingFang SC, Segoe UI, Helvetica Neue, Arial, sans-serif'
  }
}
```

---

## 2. 设计别名 Token

```ts
export const yunkeAliasTokens = {
  brandPrimary: '#1677FF',
  brandGradientStart: '#2586FF',
  brandGradientEnd: '#2874FC',
  colorNavBg: '#292E33',
  colorPageBgSoft: '#EBF2FF',
  colorHintBg: '#F2FAFF',
  textPrimary: '#333333',
  textSecondary: '#545759',
  textTertiary: '#8C8C8C',
  borderDefault: '#EBECED',
  radiusPanel: 10,
  radiusCard: 6,
  radiusControl: 4,
  pagePadding: 24,
  blockGap: 16
}
```

---

## 3. 页面级组件映射

| 场景 | 推荐组件 |
|---|---|
| 顶部导航 | `Layout.Header` + `Menu` + `Dropdown` + `Avatar` |
| 左侧导航 | `Layout.Sider` + `Menu` |
| 组织树 | `Tree` / `TreeSelect` |
| 页面筛选栏 | `Form` + `Input` + `Select` + `DatePicker` + `Button` |
| 时间切换 | `Tabs` / `Segmented` |
| 数据卡片 | `Card` + `Statistic` |
| 图表卡片 | `Card` + 图表容器 |
| 列表页 | `Table` + `Pagination` |
| 配置页 | `Form` + `InputNumber` + `Select` + `Tooltip` + `Upload` |
| 空状态 | `Empty` |
| 加载态 | `Spin` / `Skeleton` |
| 提示反馈 | `Alert` / `Message` / `Notification` |
| 弹层 | `Drawer` / `Modal` |

---

## 4. 页面模板映射

## 4.1 统计页
```text
PageHeader
FilterBar
KPIGrid
ChartsGrid
DetailSection
```

## 4.2 AI 看板页
```text
PageHero
TimeTabs
KPIGrid
InsightCards
ChartsGrid
RiskAndSuggestion
RankingOrDetail
```

## 4.3 列表页
```text
PageHeader
FilterBar
ActionBar
TableSection
PaginationSection
```

## 4.4 配置页
```text
SideMenu
ConfigForm
UploadArea
ConfigTable
SubmitBar
```

---

## 5. 组件细则

## 按钮
- 主按钮：`type="primary"`
- 次按钮：默认按钮
- 危险按钮：`danger`
- 控件圆角：4px
- 默认高度：32px

## 卡片
- 普通卡片：6px 圆角
- 重点看板卡片：10px 圆角
- 默认内边距：16~24px

## 表单控件
- Input / Select / DatePicker / InputNumber 尽量统一高度
- placeholder 使用三级文字色
- Tooltip 用于参数说明而不是大段说明文复制

## 表格
- 表头与正文默认 14px
- 操作列尽量固定到右侧
- 批量操作放在表格上方工具栏

---

## 6. 页面生成约束摘要

- 必须是 Ant Design 语义中后台
- 不要做成官网风
- 不要重拟态、重发光、赛博朋克
- 允许 AI 页面轻科技感增强，但不能跳出云客 CRM 体系
- 优先考虑结构清晰、信息密度、复用性、工程可实现性
