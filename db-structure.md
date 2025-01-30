## Структура таблицы blocked_clients

![blocked_clients](img/db-structure.png)

## SQL запрос на создание таблицы blocked_clients

``` sql
CREATE TABLE blocked_clients (  
  id SERIAL PRIMARY KEY,  
  client_id UUID NOT NULL,  
  reason VARCHAR(50),  
  comment TEXT,  
  blocked_at TIMESTAMP DEFAULT NOW(),  
  blocked_until TIMESTAMP,  
  is_active BOOLEAN DEFAULT TRUE  
);
```

*На примере СУБД PostgreSQL**
