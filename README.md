# Apache Pulsar Biscuit authentication plugin

## Tests

```bash
# run test using maven
mvn test
```

## Configuration

copy jars (from `build/libs`) to pulsar's `/lib` directory:
- biscuit-pulsar
- vavr
- vavr-match
- protobuf
- commons-codec
- biscuit
- curve25519-elisabeth

```
# Enable authentication
authenticationEnabled=true

# Autentication provider name list, which is comma separated list of class names
authenticationProviders=com.clevercloud.biscuitpulsar.BiscuitAuthenticationPlugin

# Enforce authorization
authorizationEnabled=true

# Authorization provider fully qualified class-name
authorizationProvider=com.clevercloud.biscuitpulsar.BiscuitAuthorizationPlugin

# Biscuit root signing key
biscuitRootKey=da905388864659eb785877a319fbc42c48e2f8a40af0c5baea0ef8ff7c795253

superUserRoles=admin
```
