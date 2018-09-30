<template>
  <div>
    <form action="#" method="post" @submit.prevent="bookSubmit(bookTitle, bookAuthor)">
      <input type="text" placeholder="Book Title" v-model="bookTitle">
      <input type="text" placeholder="Book Author" v-model="bookAuthor">
      <button type="submit" name="button">Add Book</button>
    </form>
  </div>
</template>

<script>
export default {
  name: 'BookForm',
  props: ['books'],
  data() {
    return {
      bookTitle: '',
      bookAuthor: '',
    };
  },
  methods: {
    bookSubmit(bookTitle, bookAuthor) {
      this.$emit('addBook', bookTitle, bookAuthor);
    },
  },
};
</script>

<style scoped>
</style>
