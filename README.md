
# Elasticsearch CRUD Operations: Library & Book Example

Welcome to the GitHub repository for our Elasticsearch and Kibana tutorial on CRUD operations using a library and book example. This repository contains all the code examples demonstrated in the video tutorial on "Tech Talks with Veer." Feel free to try these examples and explore the capabilities of Elasticsearch.

## Getting Started

Before you begin, ensure you have Elasticsearch and Kibana installed and running. If you need guidance on setting up, please refer to our previous tutorials.

## CRUD Operations Examples

### Creating an Index

An index in Elasticsearch is like a library. Here's how you create an index named `library_books`:

```

PUT /library_books
{
  "settings": {
    "number_of_shards": 1,
    "number_of_replicas": 0
  }
}
```

### Adding Data (Create)

To add books to our library, we use the following commands:

- Adding 'The Great Gatsby'

```
POST /library_books/_doc
{
  "title": "The Great Gatsby",
  "author": "F. Scott Fitzgerald"
}
```

##Adding '1984' with a specific ID (ISBN):

```
PUT /library_books/_doc/9780451524935
{
"title": "1984",
"author": "George Orwell"
}
```

### Reading Data (Read)

To retrieve the details of a book, use the GET method:

GET /library_books/_doc/[Document ID]


Replace `[Document ID]` with the actual ID of the book.

### Updating Data (Update)

To update a book's details, use the POST method with an update endpoint:

```
POST /library_books/_doc/[Document ID]/_update
{
"doc": {
"title": "New Title"
}
}
```

Replace `[Document ID]` with the book's ID.

### Deleting Data (Delete)

To remove a book from the index, use the DELETE method:

```
DELETE /library_books/_doc/[Document ID]
```

Replace `[Document ID]` with the ID of the book you wish to delete.

## Conclusion

These examples should give you a basic understanding of how to perform CRUD operations in Elasticsearch. Experiment with different data and queries to explore further.

## Connect with Us

- **YouTube**: [Tech Talks with Veer](https://www.youtube.com/techtalkswithveer)
- **GitHub**: [TechTalksWithVeer](https://github.com/TechTalksWithVeer)

If you have any questions or suggestions, feel free to open an issue or submit a pull request. Happy coding!






