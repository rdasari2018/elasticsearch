https://www.journaldev.com/18148/spring-boot-elasticsearch

Start ElasticSearch
Start Spring Boot app (Elastic6Application.java)

Start Postman and make POST request at http://localhost:8080/books with this JSON:
{
  "title" : "Java Always",
  "author" : "JournalDev",
  "price" : 99.1
}
Response is below JSON:
{
    "id": "c744db6f-1609-4408-919d-b25e43e80b99",
    "title": "Java Always",
    "author": "JournalDev",
    "price": 99.1
}

Now, make GET request at http://localhost:8080/books/c744db6f-1609-4408-919d-b25e43e80b99
Response is below JSON:
{
    "author": "JournalDev",
    "price": 99.1,
    "id": "c744db6f-1609-4408-919d-b25e43e80b99",
    "title": "Java Always"
}

Now, make PUT request at http://localhost:8080/books/c744db6f-1609-4408-919d-b25e43e80b99
{
  "title" : "Java Always Updated",
  "author" : "JournalDev",
  "price" : 99.1
}
Response is below JSON:
{
    "id": "c744db6f-1609-4408-919d-b25e43e80b99",
    "title": "Java Always Updated",
    "author": "JournalDev",
    "price": 99.1
}

Now, make GET request at http://localhost:8080/books/c744db6f-1609-4408-919d-b25e43e80b99
Response is below JSON:
{
    "author": "JournalDev",
    "price": 99.1,
    "id": "c744db6f-1609-4408-919d-b25e43e80b99",
    "title": "Java Always Updated"
}

Now, make DELETE request at http://localhost:8080/books/c744db6f-1609-4408-919d-b25e43e80b99