# spring-forum-backend

### Spring dependencies

- Lombok
- Spring Web
- MySQL Driver
- Spring Data JPA
- Spring Security
- OAuth2 Client

### SQL Tables

```sql
CREATE TABLE Posts (
    id BIGINT NOT NULL PRIMARY KEY AUTO_INCREMENT,
    title TINYTEXT NOT NULL,
    content TEXT NOT NULL,
    poster_id BIGINT NOT NULL,
    creation_date TIMESTAMP NOT NULL
);
```

```sql
CREATE TABLE Comments (
    id BIGINT NOT NULL PRIMARY KEY AUTO_INCREMENT,
    is_parent_comment BOOLEAN NOT NULL,
    parent_id BIGINT NOT NULL,
    poster_id BIGINT NOT NULL,
    likes BIGINT NOT NULL,
    dislikes BIGINT NOT NULL,
    content TEXT NOT NULL,
    creation_date TIMESTAMP NOT NULL
);
```
