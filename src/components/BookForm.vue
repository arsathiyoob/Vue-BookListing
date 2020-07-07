<template>
<form class="" action="#" method="post">
    <input v-model="bookTitle" type="text" name="title" value="" placeholder="Book Title">
    <input v-model="bookAuthor" type="text" name="author" value="" placeholder="Book Author">
    <button type="submit" name="button">Add Book</button>
    <submit type='method' name='bookSubmit'>{{ bookTitle }}: {{ bookAuthor }}]</submit>
</form>
</template>
<script>
export default {
name: 'BookForm',
props: ['books']
}
data(){
  bookTitle: '',
  bookAuthor: ''
},
methods: {
bookSubmit(bookItem,bookAuthor){
  addBook: this.$emit('addBook', bookTitle, bookAuthor);
}
},
</script>
<style>

</style>
