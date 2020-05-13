<template>
  <div class="page">
    <cover />
    <history-of-people />
    <!--<h1>Hello</h1>
    <input type="text" v-model="text" />
    <p>{{ text }}</p>-->
  </div>
</template>

<script>
import Cover from '@/components/Cover';
import HistoryOfPeople from '@/components/HistoryOfPeople';
export default {
  components: {
    cover: Cover,
    'history-of-people': HistoryOfPeople,
  },
  //data() {
  //return {
  //text: '',
  //};
  //},
};
</script>

<style>
/*input {
  display: block;
}*/
</style>
