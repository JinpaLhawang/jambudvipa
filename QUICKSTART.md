# Jinpa Lhawang Jambudvipa

## Quick Start

### discovery

```
cd ~/Development/jambudvipa/discovery
mvn package && mvn spring-boot:run -q
```

* [Discovery Management](http://localhost:8761)
* [Service Instances for account-middle](http://localhost:8090/service-instances/account-middle)
* [Service Instances for account-edge](http://localhost:8092/service-instances/account-edge)
* [Service Instances for hello-world-middle](http://localhost:8091/service-instances/hello-world-middle)

### configuration

```
cd ~/Development/jambudvipa/configuration
mvn package && mvn -DCONFIG_URI=file:/Users/nicholaseden-walker/Development/jambudvipa/properties spring-boot:run -q
```

* [Configuration for account-middle](http://localhost:8888/account-middle/master)
* [Configuration for account-edge](http://localhost:8888/account-edge/master)
* [Configuration for hello-world-middle](http://localhost:8888/hello-world-middle/master)

### account-middle

```
mongod --dbpath ~/mongodb/data/db/
cd ~/Development/jambudvipa/account-middle
mvn package && mvn spring-boot:run -q
```

* [Find by First Name](http://localhost:8090/accounts/search/findByFirstName?firstName=Jinpa)
* [Find by Last Name](http://localhost:8090/accounts/search/findByLastName?lastName=Lhawang)

### hello-world-middle

```
cd ~/Development/jambudvipa/hello-world-middle
mvn package && mvn spring-boot:run -q
```

* [Hello Jinpa Lhawang!](http://localhost:8092)

### account-edge

```
cd ~/Development/jambudvipa/account-edge
mvn package && mvn spring-boot:run -q
```

* [Account](http://localhost:8091)

### hello-world-edge

```
cd ~/Development/jambudvipa/hello-world-edge
mvn package && mvn spring-boot:run -q
```

* [From Middle: Hello Jinpa Lhawang!](http://localhost:8093)
