<template>
  <div class="g-card" :class="shadow ? 'is-' + shadow + '-shadow' : 'is-always-shadow'">
    <div class="g-card__header" v-if="$slots.header || header">
      <!-- //只有为 具名header 插槽分发内容 或者定义 prop header的值，该节点才会被渲染 -->
      <!-- $slots是一个Map，key是各个插槽的名称 -->
      <slot name="header">{{ header }}</slot>
    </div>
    <div class="g-card__body" :style="bodyStyle">
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: 'GrCard',
  props: {
    header: {},
    bodyStyle: {},
    shadow: {
      type: String,
    },
  },
};
</script>

<style>
.g-card {
  width: 500px;
  border-radius: 4px;
  border: 1px solid #ebeef5;
  background-color: #ffffff;
  overflow: hidden;
  color: #303133;
  transition: 0.3s;
}

.g-card.is-always-shadow {
  box-shadow: 0 2px 12px 0 rgba(0, 0, 0, 0.1);
}
.g-card.is-hover-shadow:focus,
.g-card.is-hover-shadow:hover {
  box-shadow: 0 2px 12px 0 rgba(0, 0, 0, 0.1);
}

.g-card__header {
  padding: 20px;
  border-bottom: 1px solid rgba(0, 0, 0, 0.1);
  box-sizing: border-box;
}

.g-card__body {
  padding: 20px;
}
</style>
