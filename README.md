## SETUP

### pour configurer un service postgresql/pgadmin

* après le lancement du contneur pgadmin
  - `docker compose exec -u postgres database createdb formation`

* création de la table **errors** dans la db formation

```sql
CREATE TABLE errors (
    id INTEGER GENERATED ALWAYS AS IDENTITY PRIMARY KEY,
    workflow VARCHAR(255) NOT NULL,
    node VARCHAR(255) NOT NULL,
    message TEXT NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```