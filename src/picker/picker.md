# Picker 选择器

定义：在一组预设数据中进行选择

## 1. 组件类型

TDesign目前只提供一种基础类型

### 1.1. 基础类型

::: demo ./demos/base.vue
:::

### 1.2. 对象数组

::: demo ./demos/object-array.vue
:::

### 1.3. 默认选中

::: demo ./demos/default-selected.vue
:::

### 1.4. 自定义展示内容

::: demo ./demos/custom.vue
:::

### 1.5. 多列选择

::: demo ./demos/multiple.vue
:::

### 1.6. 联动选择

::: demo ./demos/cascade.vue
:::

### 1.7. 弹窗层的 Picker

::: demo ./demos/popup-picker.vue
:::

## Props

### Picker Props

| 属性              | 类型   | 默认值  | 必传 | 说明         |
| ----------------- | ------ | ------- | ---- | ------------ |
| theme             | String | default | N    | picker 主题  |
| title             | String | -       | N    | 标题         |
| confirmButtonText | String | 确定    | N    | 确定按钮文字 |
| cancelButtonText  | String | 取消    | N    | 取消按钮文字 |

### PickerItem Props

| 属性         | 类型     | 默认值               | 必传 | 说明                                              |
| ------------ | -------- | -------------------- | ---- | ------------------------------------------------- |
| options      | Array    | []                   | Y    | 列的候选项                                        |
| optionKey    | String   | -                    | N    | options 为 ObjectArray 的时候，指定显示对象的 key |
| formatter    | Function | (val: string) => val | N    | 格式化显示的候选项                                |
| defaultIndex | Number   | 0                    | N    | 默认选中的候选项                                  |

## Events

### Picker Events

| 事件名  | 说明                 | 回调参数               |
| ------- | -------------------- | ---------------------- |
| change  | 选中变化时候触发     | [{value, index}]       |
| confirm | 点击确定按钮时候触发 | {value: [], index: []} |
| cancel  | 点击取消时候触发     | -                      |

### PickerItem Events

| 事件名 | 说明                   | 回调参数       |
| ------ | ---------------------- | -------------- |
| change | 候选项滚动变化时候触发 | {value, index} |