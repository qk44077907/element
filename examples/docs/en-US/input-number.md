<script>
  export default {
    data() {
      return {
        num1: 1,
        num2: 1,
        num3: 5
      }
    },
    methods: {
      handleChange(value) {
        console.log(value);
      }
    }
  };
</script>

## InputNumber

Input numerical values with a customizable range.

### Basic usage

:::demo Bind a variable to `v-model` in `<el-input-number>` element and you are set.

```html
<template>
  <el-input-number v-model="num1" @change="handleChange" :min="1" :max="10"></el-input-number>
</template>
<script>
  export default {
    data() {
      return {
        num1: 1
      };
    },
    methods: {
      handleChange(value) {
        console.log(value)
      }
    }
  };
</script>
```
:::

### Disabled

:::demo The `disabled` attribute accepts a `boolean`, and if the value is `true`, the component is disabled. If you just need to control the value within a range, you can add `min` attribute to set the minimum value and `max` to set the maximum value. By default, the minimum value is `0`.

```html
<template>
  <el-input-number v-model="num2" :disabled="true"></el-input-number>
</template>
<script>
  export default {
    data() {
      return {
        num2: 1
      }
    }
  };
</script>
```
:::

### Steps

Allows you to define incremental steps.

:::demo Add `step` attribute to set the step.

```html
<template>
  <el-input-number v-model="num3" :step="2"></el-input-number>
</template>
<script>
  export default {
    data() {
      return {
        num3: 5
      }
    }
  };
</script>
```
:::

### Attributes

| Attribute      | Description          | Type      | Accepted Values       | Default  |
|----| ----| ---| ----| -----|
|value | binding value| number | — | — |
|min | the minimum allowed value | number | — | 0 |
|max | the maximum allowed value | number | — | `Infinity` |
|step | incremental step | number | — | 1 |
|size | size of the component | string | large/small| — |
|disabled| whether the component is disabled | boolean | — | false |

### Events

| Event Name | Description | Parameters |
|----| ---- | -----|
|change | triggers when the value changes | value after change |