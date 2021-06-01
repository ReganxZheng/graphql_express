## This application is built for learning purpose on how to use express integrate with graphQL on both No-SQL and SQL databse.

### To run the development server
**```npm start```**

### To access the graphiQL GUI
**```localhost:8888/graphql```**

### Types
```graphql
type Friend {
    id: ID
    firstName: String
    lastName: String
    gender: Gender
    age: Int
    email: String
    contacts: [Contact]
}

enum Gender {
    MALE
    FEMALE
    OTHER
}

type Contact {
    firstName: String
    lastName: String
}

type Alien {
    id: ID
    firstName: String
    lastName: String
    planet: String
}
```

### Queries
```graphql
query {
    getOneFriend(id: "") {
        id
        firstName
        lastName
        gender
        language
        age
        email
        contacts
    }
    getAliens {
        id
        firstName
        lastName
        planet
    }
}
```

### Mutations
```graphql
mutation {
    createFriend(input: {}) {
        # Friend
    }
    updateFriend(input: {}) {
        # Friend
    }
    deleteFriend(id: "") {
        # Success message
    }
}