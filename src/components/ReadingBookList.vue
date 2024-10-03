<template>
    <div class="reading-book-list">
      <div v-for="book in books" :key="book.title">
        <BookItem
          :title="book.title"
          :author="book.author"
          :book="book"
          @select="handleSelect"
        >
          <template #genres>
            <li v-for="genre in book.genres" :key="genre">{{ genre }} </li>
          </template>
          <template #rating>
            <span>Rating: {{ book.rating }}</span>
          </template>
        </BookItem>
      </div>
      <p class="total-books">Total Books: {{ books.length }}</p>
    </div>
  </template>
  
  <script>
  import BookItem from './BookItem.vue';
  
  export default {
    components: {
      BookItem,
    },
    data() {
      return {
        books: [
          {
            title: "The Great Gatsby",
            author: "F. Scott Fitzgerald",
            genres: ["Fiction", "Classic", "Romance", "Literature"],
            rating: 3.93,
            image: "src/assets/the-great-gatsby.jpg",
          },
          {
            title: "Catching Fire",
            author: "Suzanne Collins",
            genres: ["Fiction", "Fantasy", "Young Adult", "Post Apocalyptic"],
            rating: 4.33,
            image: "src/assets/catching-fire.jpg",
          },
          {
            title: "Dry",
            author: "Augusten Burroughs",
            genres: ["Memoir", "Biography", "Humor", "Nonfiction"],
            rating: 4.03,
            image: "src/assets/dry.jpg",
          },
          {
            title: "The Catcher in the Rye",
            author: "J.D. Salinger",
            genres: ["Fiction", "Classic", "Young Adult", "Coming of Age"],
            rating: 3.80,
            image: "src/assets/catcher-in-the-rye.jpg",
          },
        ],
      };
    },
    methods: {
      handleSelect(bookTitle) {
        alert(`Selected Book: ${bookTitle}`);
      },
    },
  };
  </script>
