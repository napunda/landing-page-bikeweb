<template>
  <div class="header">
    <Desktop />
  </div>
</template>

<script>
import Desktop from "./Desktop.vue";
export default {
  components: { Desktop },
};
</script>

<style>
.header {
  position: fixed !important;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 999;
}
</style>
