# spring-forum-backend

SQL Tables

```sql
CREATE TABLE Users (
    id BIGINT NOT NULL PRIMARY KEY AUTO_INCREMENT,
    login TINYTEXT NOT NULL,
    password TINYTEXT NOT NULL
);
```
```sql
CREATE TABLE Posts (
    id BIGINT NOT NULL PRIMARY KEY AUTO_INCREMENT,
    title TINYTEXT NOT NULL,
    content TINYTEXT NOT NULL,
    posterID BIGINT NOT NULL,
    creationDate TIMESTAMP NOT NULL
);
```

```sql
CREATE TABLE Comments (
    id BIGINT NOT NULL PRIMARY KEY AUTO_INCREMENT,
    isParentComment BOOLEAN NOT NULL,
    parentID BIGINT NOT NULL,
    posterID BIGINT NOT NULL,
    likes BIGINT NOT NULL,
    dislikes BIGINT NOT NULL,
    content TEXT NOT NULL,
    creationDate TIMESTAMP NOT NULL
);
```
