# Jinpa Lhawang Jambudvipa

## Quick Start

### discovery

```
cd ~/Development/jambudvipa/discovery
mvn package && mvn spring-boot:run
```

[http://localhost:8761/](http://localhost:8761)

### configuration

```
cd ~/Development/jambudvipa/configuration
mvn package && mvn -DCONFIG_URI=file:/Users/nicholaseden-walker/Development/jambudvipa/properties spring-boot:run
```

http://localhost:8888/configuration/master
http://localhost:8888/account-middle/master
http://localhost:8888/hello-world-middle/master

### account-middle

```
mongod --dbpath ~/mongodb/data/db/
cd ~/Development/jambudvipa/account-middle
mvn package && mvn spring-boot:run
```

http://localhost:8090/accounts/search/findByFirstName?firstName=Jinpa
http://localhost:8090/accounts/search/findByLastName?lastName=Lhawang

http://localhost:8090/service-instances/account-middle

### hello-world-middle

```
cd ~/Development/jambudvipa/hello-world-middle
mvn package && mvn spring-boot:run
```

http://localhost:8091
http://localhost:8091/service-instances/hello-world-middle

### account-edge

```
cd ~/Development/jambudvipa/account-edge
mvn package && mvn spring-boot:run
```

http://localhost:8080
