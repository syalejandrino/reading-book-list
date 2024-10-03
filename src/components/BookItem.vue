<template>
    <div class="book-item">
      <img :src="book.image" alt="Book Cover" class="book-cover" />
      <h3>{{ title }}</h3>
      <p>Author: {{ author }}</p>
      <div class="genres">
        <slot name="genres"></slot>
      </div>
      <div class="rating">
        <slot name="rating"></slot>
      </div>
      <button @click="selectBook">Select</button>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      title: {
        type: String,
        required: true,
      },
      author: {
        type: String,
        required: true,
      },
      book: {
        type: Object,
        required: true,
      },
    },
    emits: ['select'],
    methods: {
      selectBook() {
        this.$emit('select', this.title);
      },
    },
  };
  </script>