<template>
  <select v-on:change="change" :value="selected">
    <option value="en">{{ $t('languages.en') }}</option>
    <option value="pt">{{ $t('languages.pt') }}</option>
    <option value="zh-cn">{{ $t('languages.zhCN') }}</option>
  </select>
</template>

<script>
export default {
  name: 'languages',
  props: [ 'selected' ],
  methods: {
    change (event) {
      this.$emit('update:selected', event.target.value)
    }
  }
}
</script>
