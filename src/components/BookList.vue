<template>
    <div>
        <h1>{{ title }}</h1>
        <ul>
         <!-- <book-item ng-repeat="forBook in books" book="forBook" track-by="forBok.title" -->
            <book-item v-for="book in books" :book="book" :key="forBook.title"></book-item>
        </ul>
    </div>
</template>
<script>
    import BookItem from './BookItem';

    export default {
        name: 'BookList',
        data() {
            return {
                title: 'All Books',
                books: [
                    {title: 'Self-Reliance', author: 'Ralph Waldo Emerson'},
                    {title: 'American Gods', author: 'Neil Gaiman'},
                    {title: 'Amusing Ourselves to Death', author: 'Neil Postman'},
                ]
            };
        },
        components: {
            BookItem,
        }
    }
</script>
<style>
    h1, h2 {
        font-weight: normal;
    }
    ul {
        list-style-type: none;
        padding: 0;
    }
    li {
        display: block;
        margin: 0 10px;
    }
</style>