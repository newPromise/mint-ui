<template>
  <div class="mint-swipe-item">
    <slot></slot>
  </div>
</template>

<script>
  export default {
    name: 'mt-swipe-item',
    mounted() {
      //  执行 this.$parent.swipeItemCreated(this); 方法
      this.$parent && this.$parent.swipeItemCreated(this);
    },

    destroyed() {
      this.$parent && this.$parent.swipeItemDestroyed(this);
    }
  };
</script>
