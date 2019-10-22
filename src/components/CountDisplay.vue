<template>
  <div>
    <slot name="before"></slot>
    <div>{{ count }}回</div>
    <slot></slot>
  </div>
</template>
<script lang="ts">
import Vue from "vue";
import store from "@/store/";
export default Vue.extend({
  store,
  computed: {
    count(): number {
      return this.$store.state.count;
    }
  }
});
</script>
<style lang="scss" scoped>
div {
  font-size: 3rem;
  color: red;
}
</style>
