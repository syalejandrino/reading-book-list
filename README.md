# reading-book-list

This Vue.js application presents a simple reading book list, allowing users to browse through a selection of books. The project utilizes the Options API for component structure and includes the following features:

Components
BookItem.vue: Represents individual book items and displays:

Book cover image
Title (passed as a prop)
Author (passed as a prop)
Genres (displayed via a slot)
Rating (displayed via a slot)
A "Select" button that emits an event when clicked, showing an alert with the selected book's title.
ReadingBookList.vue: Serves as the main template for the book list. It includes:

An array of at least four book objects, each containing title, author, genres, rating, and image.
Total count of books displayed at the bottom of the page.
A method that handles the emitted event from the BookItem component to show an alert with the selected book's title.
Features
Dynamic rendering of book information using v-for to iterate over the book array.
Communication between parent (ReadingBookList) and child (BookItem) components through props and events.
A clean and user-friendly interface, with CSS styling applied to enhance the visual appeal.
Setup Instructions
Clone the repository.
Navigate to the project directory and install dependencies:
bash
Copy code
cd reading-book-list
npm install
Run the application:
bash
Copy code
npm run dev
Open the application in your browser.
