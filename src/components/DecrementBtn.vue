<template>
  <button @click="decrement">減らす</button>
</template>
<script lang="ts">
import Vue from "vue";
import store from "@/store/";
export default Vue.extend({
  methods: {
    decrement() {
      store.commit("decrement");
      this.$emit("decrement");
    }
  }
});
</script>
<style lang="scss" scoped>
button {
  color: blue;
}
</style>
