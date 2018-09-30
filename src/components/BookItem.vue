<template>
  <li <li v-for="book in books" :key="book.title">
    {{ book.title }} : {{ book.author }}
  </li>
</template>

<script>
export default {
  data() {
    return {
      name: 'BookItem',
    };
  },
  props: ['book'],
};
</script>

<style scoped>
li {
  display: block;
  margin: 0 10px;
}
</style>
