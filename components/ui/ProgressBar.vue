<template>
  <div class="progressBar">
    <div class="progressBar__fill"></div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.progressBar {
  max-width: 260px;
  min-height: 40px;
  background-color: #f4f4f4;
  display: flex;
}
.progressBar__fill {
  background-color: #613a93;
  position: absolute;
  left: 0;
  top: 0;
}
</style>
