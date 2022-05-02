## Installation:
1. Run docker compose mariadb instance from `/docker/spring-jwt.yml`

## Testing
1. Login 
```
curl --location --request POST 'http://localhost:8080/login' \
--header 'Content-Type: application/x-www-form-urlencoded' \
--header 'Cookie: JSESSIONID=C1BB28EAC531EAC9B728E7FDCAAF3EAA' \
--data-urlencode 'username=john' \
--data-urlencode 'password=qaz123'
```

2. refresh token
```
curl --location --request GET 'http://localhost:8080/api/token/refresh' \
--header 'Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJqb2huIiwicm9sZXMiOlsiUk9MRV9NQU5BR0VSIiwiUk9MRV9VU0VSIl0sImlzcyI6Imh0dHA6Ly9sb2NhbGhvc3Q6ODA4MC9sb2dpbiIsImV4cCI6MTY1MTQ3ODIzNn0.xdFuFFG9jCNG4TiBEZMCNI8xYvqvTf6ClX3RHKrGs68' \
--header 'Cookie: JSESSIONID=C1BB28EAC531EAC9B728E7FDCAAF3EAA'
```

3. Get users
```
curl --location --request GET 'http://localhost:8080/api/user/' \
--header 'Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJqb2huIiwicm9sZXMiOlsiUk9MRV9NQU5BR0VSIiwiUk9MRV9VU0VSIl0sImlzcyI6Imh0dHA6Ly9sb2NhbGhvc3Q6ODA4MC9sb2dpbiIsImV4cCI6MTY1MTQ3Njk0NX0.OBhhtnjKGJi1bOwiCpqUE1581NODYQ_a1NLRLGhYfqk' \
--header 'Cookie: JSESSIONID=C1BB28EAC531EAC9B728E7FDCAAF3EAA'
```