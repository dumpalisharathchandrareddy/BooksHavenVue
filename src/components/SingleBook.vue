<template>
    <div class="book-details">
        <div class="img-container">
            <img class="book-img" :src="book.image" />
        </div>
        <h2 class="book title">{{book.title}}</h2>
        <!-- <p class="book author"> - {{book.author}}</p> -->
        <p class="book summary">{{book.summary}}</p>
        <p class="book author"> - {{book.author}}</p>
        <div class="tags">
            <p class="book genre">{{book.genre}}</p>
            <p class="book publication_date">{{book.publication_date}}</p>
            <p class="book rating_review">{{book.rating_review}}</p>
        </div>

        <!-- <p class="book suggestions">{{book.related_book_suggestions_images}}</p> -->
    </div>
</template>

<script>
    export default{
        name: 'SingleBook',
        props:{
            book: Object
        }
    }
</script>

<style scoped>
    .book-details{
    padding: 20px;
    background-color: white;
    line-height: 1.5rem;
    border-radius: 8px;
    margin-bottom: 1rem;
    /* border: solid #3F51B5; */
    background-color: #454b6c;
    color: #FFF;
    }
    .title {
        text-align: center;
    margin: 0.5rem 0;
    text-transform: uppercase;
    color: burlywood;
    }
    .author {
        text-align: right;
    font-size: 0.8rem;
    color: #FFF;
    font-weight: bold;
    }
    .summary{
        font-size: 0.85rem;
        text-align: justify;
        margin: 0.5rem 0;
    }
    .img-container{
        width: 100%;
        text-align: center;
    }
    .img-container img{
        width: 100%;
        max-height: 425px;
    object-fit: cover;
    border-radius: 8px;
    border: 2px solid #000;
    }
    .tags {
        display: flex;
        justify-content: space-around;
    margin: 0.5rem 0;
    }

    .genre, .publication_date, .rating_review{
        color: #000;
    background-color: #FFF;
    padding: 5px 10px;
    border-radius: 10px;
    font-size: 0.8rem;
    letter-spacing: 1px;
    font-weight: bold;
    }
</style>