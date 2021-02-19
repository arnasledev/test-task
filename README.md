# Test task for the backend

### Description

You will need to create a backend API service for front-end communication. We chose to build book CRUD (create/read/update/delete) for that. You will have to use the database with several different collections to store books and its data. For fetching and manipulating the data you will have to use apollo graphql client.

### Tech description
Your API server should use both express and apollo server express for routing, mongo (with `mongoose`) or mysql (with `sequelize`) for data storage, typescript and `ts-node` for compiling and launching. 

### Task and the goal
The situation: there is a book store and the owner wants its clients to have an ability to read or leave the books reviews online. So we need to build a CRUD application for that. The database should have 3 different collections:

- Books (structure and the sample data)

id  | name | createdAt | updatedAt
------------- | ------------- | ------------- | -------------
595575df-af91-4b5f-92f4-376359768247 | Matilda | 2021/02/18 18:18:32 | 2021/02/18 18:18:32

- Books reviews (structure and the sample data)

id  | bookId | review | author | createdAt | updatedAt
------------- | ------------- | ------------- | ------------- | ------------- | -------------
595575df-af91-4b5f-92f4-376359768247 | 595575df-af91-4b5f-92f4-376359768247 | very good book! | Will J. Smith | 2021/02/18 18:18:32 | 2021/02/18 18:18:32

The api should provide these resolvers:

1. mutations
   1. addBook (name)
   2. updateBook (name)
   3. addReview (bookId, review, author)
   4. updateReview (bookId, review)
3. queries
   1. books
   2. book (bookId)
   3. reviews (bookId)
   4. review (reviewId)
   5. authors

### GraphQL requirements
No frontend needed, everything should be made using graphql playground. GraphQL relationships should be used.

### Nice to have
Docker with database container should be used if local database selected. The remote database should be used if there are no docker. ReadME with an explanation of how everything works. Keep your code as simple as that. 

### Big big big NICE TO HAVE
Clean architecture with entities and repositories. 

Submit your code to your Github repo.
