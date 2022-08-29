<template>
  <v-sheet color="transparent container-title">
    <div class="sub-title">
      <slot></slot>
    </div>
  </v-sheet>
</template>

<script>
export default {};
</script>

<style>
.container-title {
  display: flex;
  justify-content: center;
}
.sub-title {
  font-family: "Kaushan Script";
  font-style: normal;
  font-weight: 400;
  font-size: 32px;
  line-height: 46px;
  color: #abdf3a;
  transform: rotate(-2deg);
}
</style>
