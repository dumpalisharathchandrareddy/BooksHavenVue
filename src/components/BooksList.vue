<template>
    <div class="books-list">
        <div v-for="book of books" :key="book.title" > 
            <SingleBook :book=book />
        </div>
    </div>
</template>
<script>
import SingleBook from './SingleBook.vue'

export default {
    name: 'BooksList',
    props:{
        books: Array
    },
    components:{
        SingleBook
    }
    
}
</script>
<style scoped>
    .books-list{
    padding: 0px 40px;
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: 1fr;
    gap: 0px 20px;
    grid-template-areas: "project-item-1 project-item-2 project-item-3";
    width: 80%;
    margin: auto;
    }
</style>
