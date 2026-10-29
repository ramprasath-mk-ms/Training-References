## 1. SQL

```text
// ##### SQL Authentication #####
// "Server=MS-MDU-DESKTOP-;Database=EmployeeDB;User Id=AdminUser;Password=Admin@123;TrustServerCertificate=True"
```

```text
// ##### Windows Authentication #####
// "Server=MS-MDU-DESKTOP-;Database=EmployeeDB;Trusted_Connection=True;TrustServerCertificate=True";
```

```bash
Scaffold-DbContext "Server=MS-MDU-DESKTOP-;Initial Catalog=EmployeeManagementSystemDB;Integrated Security=True;User ID=AdminUser;Password=Admin@123;TrustServerCertificate=True;"  Microsoft.EntityFrameworkcore.SqlServer -Context AppDbContext -ContextDir Data -OutputDir Models -f
```

```text
## Connection String

Data Source=localhost;Initial Catalog=EmployeeManagementSystemDB;Integrated Security=True;Persist Security Info=True;User ID=AdminUser;Password=Admin@123;Pooling=False;MultipleActiveResultSets=False;Encrypt=True;TrustServerCertificate=True;
```

```bash
## Scaffold Command

Scaffold-DbContext "Data Source=localhost;Initial Catalog=UserDB;Integrated Security=True;Persist Security Info=True;User ID=AdminUser;Password=Admin@123;Pooling=False;MultipleActiveResultSets=False;Encrypt=True;TrustServerCertificate=True;" Microsoft.EntityFrameworkcore.SqlServer -ContextDir Data -OutputDir Models -f
```

```bash
## using dotnet

dotnet ef dbcontext scaffold "Your_Connection_String" Microsoft.EntityFrameworkCore.SqlServer \
--context ApplicationDbContext \
--context-dir Data \
--output-dir Models \
--force
```

```bash
## using Scaffold Command

Scaffold-DbContext "conn-string" Microsoft.EntityFrameworkcore.SqlServer -Context AppDbContext -ContextDir Data -OutputDir Models -f
```

```bash
Scaffold-DbContext "Server=localhost;Database=WebAppTest_DbContext;User Id=AdminUser;Password=Admin@123;TrustServerCertificate=True;" Microsoft.EntityFrameworkCore.SqlServer -Context AppDbContext -ContextDir Data -OutputDir Models -NoOnConfiguring -DataAnnotations -f
```

```bash
dotnet ef dbcontext scaffold "Host=localhost;Port=5432;Database=blogsdb;Username=adminuser;Password=Admin@123" Npgsql.EntityFrameworkCore.PostgreSQL -o Models -c BlogsDbContext -f
```

```bash
dotnet ef dbcontext scaffold "Host=localhost;Port=5432;Database=blogsdb;Username=adminuser;Password=Admin@123" Npgsql.EntityFrameworkCore.PostgreSQL --context AppDbContext --context-dir Data --output-dir Models --force
```

```bash
dotnet ef dbcontext scaffold "Host=localhost;Port=5432;Database=amazondb;Username=adminuser;Password=Admin@123" Npgsql.EntityFrameworkCore.PostgreSQL --context AppDbContext --context-dir Data --output-dir Models --annotations --force
```

## 2. For RabbitMQ

```bash
docker run -d -name rabbitmq -p 5672:5672 -p 15672:15672 rabbitmq:3-management
```

```bash
docker pull rabbitmq:3-management
```

```bash
## docker scout quickview rabbitmq:3-management

## use this
docker run --rm -it --name rabbitmq -p 15672:15672 -p 5672:5672 rabbitmq:3-management
```

```bash
docker run --rm -it -p 15672:15672 -p 5672:5672 rabbitmq:4.3.3-management-alpine
```

```bash
docker run --rm -it -p 15672:15672 -p 5672:5672 rabbitmq:4.3-alpine
```

## 3. For KeyCloak

```bash
docker pull quay.io/keycloak/keycloak:latest
```

```bash
docker run -p 127.0.0.1:8080:8080 -e KC_BOOTSTRAP_ADMIN_USERNAME=admin -e KC_BOOTSTRAP_ADMIN_PASSWORD=admin quay.io/keycloak/keycloak:26.7.0 start-dev
```

```bash
docker run -name keycloak -p 127.0.0.1:8080:8080 -e KEYCLOAK_ADMIN=admin -e KC_BOOTSTRAP_ADMIN_USERNAME=admin -e KC_BOOTSTRAP_ADMIN_PASSWORD=admin quay.io/keycloak/keycloak:latest start-dev
```

```bash
docker run -name trusting_cohen -p 8080:8080 \
-e KEYCLOAK_ADMIN=admin \
-e KEYCLOAK_ADMIN_PASSWORD=admin \
quay.io/keycloak/keycloak:latest start-dev
```

```bash
## without name
docker run -p 8080:8080 \
-e KEYCLOAK_ADMIN=admin \
-e KEYCLOAK_ADMIN_PASSWORD=admin \
quay.io/keycloak/keycloak:latest start-dev
```

```
// Client Secret:
LfO4eRpDKczjJ9zzeKeq9zOKQbLOHEMjO4CuxEOJdvr3T9Sd9gC2kJKcr9JTZy909Cybc6OzDlrUBR2SLODGo7
```

```bash
## with name
docker run -name keycloak -p 8080:8080 \
-e KEYCLOAK_ADMIN=admin \
-e KEYCLOAK_ADMIN_PASSWORD=admin \
quay.io/keycloak/keycloak:latest start-dev
```

```
http://localhost:8080/realms/demo-realm/protocol/openid-connect/token
```

### master realm: admin email

theonlyadmin123@yopmail.com
