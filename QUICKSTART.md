# Jinpa Lhawang Jambudvipa

## Quick Start

### discovery

```
cd ~/Development/jambudvipa/discovery
mvn package && mvn spring-boot:run
```

* [Discovery Management](http://localhost:8761)

### configuration

```
cd ~/Development/jambudvipa/configuration
mvn package && mvn -DCONFIG_URI=file:/Users/nicholaseden-walker/Development/jambudvipa/properties spring-boot:run
```

Configuration for:
* [configuration](http://localhost:8888/configuration/master)
* [account-middle](http://localhost:8888/account-middle/master)
* [hello-world-middle](http://localhost:8888/hello-world-middle/master)

### account-middle

```
mongod --dbpath ~/mongodb/data/db/
cd ~/Development/jambudvipa/account-middle
mvn package && mvn spring-boot:run
```

* [Find by First Name](http://localhost:8090/accounts/search/findByFirstName?firstName=Jinpa)
* [Find by Last Name](http://localhost:8090/accounts/search/findByLastName?lastName=Lhawang)
* [Discovery for account-middle](http://localhost:8090/service-instances/account-middle)

### hello-world-middle

```
cd ~/Development/jambudvipa/hello-world-middle
mvn package && mvn spring-boot:run
```

* [Hello Jinpa Lhawang!](http://localhost:8091)
* [Discovery for hello-world-middle](http://localhost:8091/service-instances/hello-world-middle)

### account-edge

```
cd ~/Development/jambudvipa/account-edge
mvn package && mvn spring-boot:run
```

* [From Middle: Hello Jinpa Lhawang!](http://localhost:8080)
