<template>
  <div :class="classes">
    <template v-if="type == 'sof'">
      <button class="btn" disabled="disabled"><slot name="hint-btn-txt">#btn</slot></button>
      <div class="callout">
        <div class="hint-title"><slot name="hint-callout-title">#title</slot></div>
        <div class="hint-content"><slot name="hint-callout-content">#content</slot></div>
      </div>
    </template>
  </div>
</template>

<script>
const prefixCls = 'rz-hint'

export default {
  name: 'Hint',
  props: {
    type: {
      type: String,
      required: false,
      default: 'sof'
    }
  },
  computed: {
    classes () {
      return `${prefixCls}-${this.type}`
    }
  }
}
</script>
