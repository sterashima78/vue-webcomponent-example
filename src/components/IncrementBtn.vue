<template>
  <button @click="increment">増やす</button>
</template>
<script lang="ts">
import Vue from "vue";
import store from "@/store/";
export default Vue.extend({
  methods: {
    increment() {
      store.commit("increment");
      this.$emit("increment");
    }
  }
});
</script>
<style lang="scss" scoped>
button {
  color: green;
}
</style>
