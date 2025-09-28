
The right way to create auto increment primary key

```sql
CREATE TABLE users (
  id INT GENERATED ALWAYS AS IDENTITY PRIMARY KEY
)
```
