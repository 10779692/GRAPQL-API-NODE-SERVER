# DGM 4790 GraphQL API Node Server - Jared Reed

## Instructions: 


1. Clone repository into Github: https://github.com/10779692/GRAPQL-API-NODE-SERVER.git

2. Run "cd my-yoga-server"

3. Run the command "npm i graphql-yoga prisma-binding

4. Run the command "node src/index.js"

5. Your playground should start on "http://localhost:4000"

![Image of playground-layout](<img src="playground-layout.png">)

6. To run a posts query, use the following schema: 

    `query {
  posts(searchString: "insert title here or leave blank to retrieve all posts") {
    id
    title
    content
    published
    author {
      id
      name
    }
  }
}`

7. To run a single user query, use the following schema: 

    `query {
  user(id: "") {
    id
    name
  }
}`

8. To run a query to retrieve all users, use the following schema: 

    `query {
  users {
    id
    name
    posts{
      content
    }
  }
}`

9. To run a signup mutation, use the following schema: 

    `mutation {
  signup(name: "") {
    id
  }
}`

10. To run a createDraft mutation, use the following schema: 

    `mutation {
  createDraft(
    title: "insert new title here",
    content: "insert new content here",
    authorId: "insert id from signup mutation here"
  ) {
    id
    published
  }
}`

11. To run a publish mutation, use the following schema:

    `mutation {
  publish(
    id: "insert created id from createDraft mutation here",
  ) {
    id
    published
  }
}`

12. To run a deletePost mutation, use the following schema:

    `mutation {
  deletePost(
    id: "run posts query to grab id from post to delete it",
  ) {
    id
  }
}`
