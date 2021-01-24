# Coding UI Kit Codemod

一组尝试将 coding-ui-kit 重构为 antd 的 codemod 脚本集合，基于 [jscodeshift](https://github.com/facebook/jscodeshift) 构建。(受 [codemod-v4](https://github.com/ant-design/codemod-v4) 启发)

## 使用

TODO

## 重构变化

统一的变化，组件统一从单包引入。

### coding-ui-kit

- Alert

  - type，danger -> error
  - 移除 placement，placement: top -> banner: true
  - noIcon -> showIcon
  - onDismiss -> onClose

- Avatar

  - size
    - xsmall -> 16
    - tiny -> small
    - small -> default
    - regular -> large
    - medium -> 64
    - large -> 128
    - big -> 200
  - 移除 resize，基础组件不应该包含业务逻辑

- Button
  - type
    - undefined | default | confirm -> primary
    - general -> undefined | default
    - danger | warning -> primary & danger: true
  - size
    - default -> undefind | middle
    - medium | large | big -> large
  - 移除 empty
  - 移除 leftIcon，可根据 children 和 loading 渲染
  - 移除 rightIcon，可在 children 中直接渲染
  - 移除 getLoadingIcon，可在 children 中直接渲染
  - 移除 showChildrenWhenLoading，可根据 loading 控制

### coding-ui-kit2

TODO

## License

MIT
