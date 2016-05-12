# Jinpa Lhawang Jambudvipa

## Quick Start

### discovery

```
cd ~/Development/jambudvipa/discovery
mvn package && mvn spring-boot:run
```

* [Discovery Management](http://localhost:8761)
* [Service Instances for account-middle](http://localhost:8090/service-instances/account-middle)
* [Service Instances for account-edge](http://localhost:8092/service-instances/account-edge)
* [Service Instances for hello-world-middle](http://localhost:8091/service-instances/hello-world-middle)

### configuration

```
cd ~/Development/jambudvipa/configuration
mvn package && mvn -DCONFIG_URI=file:/Users/nicholaseden-walker/Development/jambudvipa/properties spring-boot:run
```

* [Configuration for account-middle](http://localhost:8888/account-middle/master)
* [Configuration for account-edge](http://localhost:8888/account-edge/master)
* [Configuration for hello-world-middle](http://localhost:8888/hello-world-middle/master)

### account-middle

```
mongod --dbpath ~/mongodb/data/db/
cd ~/Development/jambudvipa/account-middle
mvn package && mvn spring-boot:run
```

* [Find by First Name](http://localhost:8090/accounts/search/findByFirstName?firstName=Jinpa)
* [Find by Last Name](http://localhost:8090/accounts/search/findByLastName?lastName=Lhawang)

### hello-world-middle

```
cd ~/Development/jambudvipa/hello-world-middle
mvn package && mvn spring-boot:run
```

* [Hello Jinpa Lhawang!](http://localhost:8092)

### account-edge

```
cd ~/Development/jambudvipa/account-edge
mvn package && mvn spring-boot:run
```

* [Account](http://localhost:8091)

### hello-world-edge

```
cd ~/Development/jambudvipa/hello-world-edge
mvn package && mvn spring-boot:run
```

* [From Middle: Hello Jinpa Lhawang!](http://localhost:8093)

### google-calendar-middle

```
cd ~/Development/jambudvipa/google-calendar-middle
mvn package && mvn spring-boot:run
```

* [Show Calendars](http://localhost:8095/calendar/list)

* [Add Calendars using Batch](http://localhost:8095/calendar/batch/add)
* [Add Calendar](http://localhost:8095/calendar/add)
* [Update Calendar](http://localhost:8095/calendar/{calendarId}/update)
* [Add Event](http://localhost:8095/calendar/{calendarId}/add)
* [Show Events](http://localhost:8095/calendar/{calendarId}/events/list)
* [Delete Calendars using Batch](http://localhost:8095/calendar/batch/delete)
* [Delete Calendar](http://localhost:8095/calendar/{calendarId}/delete)
