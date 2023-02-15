# OAuth Authorization Server using Spring Security 

### Backend alias

The following lines must be added in ```/etc/hosts``` to avoid having the browser create the cookies for the same 
URL overriding values from the different backends.
```
127.0.0.1       backend-auth
127.0.0.1       backend-gateway-client
127.0.0.1       backend-resources
127.0.0.1       backend-client
```

### Local Postgre Database

The backend-auth needs a database where to store the credentials. The following docker command will create it.

```
docker run -d -e POSTGRES_HOST_AUTH_METHOD=trust -e POSTGRES_USER=auth_usr -e POSTGRES_PASSWORD=pwd -e POSTGRES_DB=authdb -p 5434:5432 postgres:13
```



