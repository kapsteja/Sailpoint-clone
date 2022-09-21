
1. Drop the binaries to their respective folders inside the `binaries` folder \
    - `identityiq-8.1.zip` -> `binaries/base/` (only one file allowed)
    - `identityiq-8.1p2.jar` -> `binaries/patch/` (only one file allowed)
    - `identityiq-8.1p2-XXXXX.zip ` -> `binaries/efixes/` (multiple files allowed)
2. Adjust the `.env` file to match the binaries you want to use. 
    ```
    TOMCAT_VERSION=9.0.43
    ```

### Build & Launch
```
docker-compose up --build

### Start Fresh (between different version of IdentityIQ)
Delete the volumes created from previous executions by running this command:
```
docker-compose rm -v
```

### Access
IdentityIQ should be accessible from [http://localhost:8080/](http://localhost:8080/) and [http://localhost:8080/identityiq](http://localhost:8080/identityiq).

> I'm not gonna provide any details regarding the authentication. You will find those details inside the software documentation.

Tomcat manager from [http://localhost:8080/manager/](http://localhost:8080/manager/) with the username `admin` and password `admin`

Adminer from [http://localhost:8081/](http://localhost:8081/)
