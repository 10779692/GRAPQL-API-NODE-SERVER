# DGM 4790 GraphQL API Node Server - Jared Reed

## Instructions: 


1. Clone repository from Github: https://github.com/10779692/GRAPQL-API-NODE-SERVER.git

2. Run the command "cd GRAPQL-API-NODE-SERVER"

3. Run the command "cd my-yoga-server"

4. Run the command "npm i graphql-yoga prisma-binding"

5. Run the command "node src/index.js"

6. Your playground should start on "http://localhost:4000"

![Image of playground-layout](https://github.com/10779692/GRAPQL-API-NODE-SERVER/blob/master/playground-layout.png?raw=true)

7. To run a posts query, use the following query: 

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

8. To run a single user query, use the following query: 

    `query {
  user(id: "") {
    id
    name
  }
}`

9. To run a query to retrieve all users, use the following query: 

    `query {
  users {
    id
    name
    posts{
      content
    }
  }
}`

10. To run a signup mutation, use the following mutation: 

    `mutation {
  signup(name: "") {
    id
  }
}`

11. To run a createDraft mutation, use the following mutation: 

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

12. To run a publish mutation, use the following mutation:

    `mutation {
  publish(
    id: "insert created id from createDraft mutation here",
  ) {
    id
    published
  }
}`

13. To run a deletePost mutation, use the following mutation:

    `mutation {
  deletePost(
    id: "run posts query to grab id from post to delete it",
  ) {
    id
  }
}`
