<template>
  <div class="container">
    <h1>Hello</h1>
    <input type="text" v-model="text" />
    <p>{{ text }}</p>
    <about />
  </div>
</template>

<script>
import About from '@/components/About';
export default {
  components: {
    about: About,
  },
  data() {
    return {
      text: '',
    };
  },
};
</script>

<style>
input {
  display: block;
}
</style>
