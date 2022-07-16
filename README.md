# Reto NewRelic y Platzi
Observability challenge with New Relic and Platzi

## platzi route certificates

<img src="src/diploma-docker.jpg" alt="drawing" width="200"/><img src="src/diploma-new-relic.jpg" alt="drawing" width="220"/><img src="src/diploma-devops.jpg" alt="drawing" width="200"/>

## FoodMe App DashBoard

![dashboard](src/dashboard.png)

## Used NRQL Queries

### Troughput
```sql
SELECT count(*) FROM Transaction
```

### avg duration
```sql
SELECT average(duration) FROM PageView SINCE 1 week ago COMPARE WITH 1 day ago
```

### Count visits
```sql
SELECT count(*) FROM PageView FACET appName 
```

### Max duration (transaction)
```sql
SELECT max(duration) FROM Transaction 
```

### Count status code
```sql
SELECT count(*) FROM Transaction FACET http.statusCode
```

### Transaction AVG in FoodMe
```sql
SELECT average(duration) FROM Transaction WHERE appName = 'FoodMe'
```

### Slower cities
```sql
SELECT max(duration), average(duration) FROM PageView FACET city
```

### Average transaction duration
```sql
SELECT average(duration) FROM Transaction FACET name SINCE 1 week ago
```

### Visit by country
```sql
SELECT max(duration), average(duration) FROM PageView FACET city
```