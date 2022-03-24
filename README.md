## 简介

使用了最新的`vue3`,`vite2`,`TypeScript`等主流技术开发，开箱即用的中后台前端解决方案。

## 安装使用

- 获取项目代码

```bash
git clone https://github.com/Southliu/vue-vite-admin.git
```

- 安装依赖

```bash
cd vue-vite-admin
pnpm install
```

- 运行

```bash
pnpm dev
```

- 打包

```bash
pnpm build
```

## 图标(iconify)

- 参考 [iconify官方地址](https://icon-sets.iconify.design/)
- VS Code安装Iconify IntelliSense - 图标内联显示和自动补全

## Git 贡献提交规范

- 参考 [vue](https://github.com/vuejs/vue/blob/dev/.github/COMMIT_CONVENTION.md) 规范

  - `feat` 增加新功能
  - `fix` 修复问题/BUG
  - `style` 代码风格相关无影响运行结果的
  - `perf` 优化/性能提升
  - `refactor` 重构
  - `revert` 撤销修改
  - `test` 测试相关
  - `docs` 文档/注释
  - `chore` 依赖更新/脚手架配置修改等
  - `workflow` 工作流改进
  - `ci` 持续集成
  - `types` 类型定义文件更改
  - `wip` 开发中

- 如果无法运行commitlint，请运行以下指令：

```
  npx husky add .husky/commit-msg 'npx --no-install commitlint --edit "$1"'
```

## 计划

- [ ] 主题换肤功能
- [ ] i18n语言切换
- [ ] E2E测试
- [ ] 安全优化
- [x] 封装文档说明
- [x] 密码规则
- [ ] cli生成增删改查
- [ ] 弹窗拖拽功能
- [ ] 手机端适配
- [x] Icon封装
- [x] 标签页右键功能
- [x] 搜索功能
- [x] 修改密码弹窗

## 关于封装

  - 封装目的

    1. 功能扩展，在原有的api上拓展。
    2. 功能整合，合并两个或两个以上组件的api。
    3. 样式统一，避免后期样式变动，导致牵一发而动全身。
  
  - 封装说明
    1. `BasicForm`表单
      ```base
        key: string; // 唯一标识
        title: string; // 标题
        rules?: IFormRule[]; // 规则
        component: IComponents; // 组件名，参考(https://next.antdv.com/components/overview-cn)
        componentProps?: IComponentProps; // 组件参数，官方组件参数
      ```

    2. `BasicTable`表格
      ```base
        total: number; // 表格总数
        ...other; // 表格UI参数，参考(https://xuliangzhan_admin.gitee.io/vxe-table/#/table/grid/basic)
      ```

    3. `BasicPagination`分页器
      ```base
        total: number; // 分页总数
        defaultCurrent: number; // 当前页码数
      ```
        