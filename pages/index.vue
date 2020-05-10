<template>
  <div class="container">
    <statistics-block></statistics-block>
  </div>
</template>

<script>
import Statistics from '@/components/Statistics/Statistics';
export default {
  components: {
    'statistics-block': Statistics,
  },
};
</script>

<style>
input {
  display: block;
}
</style>
