
## ER diagram 

As can be seen from the ER diagram above, Petclinic application model consists of the following six entities:

- vets — Veterinarians
- specialties — Specializations of the Veterinarians
- owners — Pet owners
- pets — Pets themselves
- types — Types of the pets (ie. cats, birds, dogs, ….)
- visits — Records of the pet visits to the veterinarians

## Code

```
jhipster import-jdl path_to_the_downloaded_file/petclinic.jh

```

As you can see from the console log, JHipster has created a lot of files :-) In short, for each of our entities the following has been create on the server side:

- JPA Class representation of an entity
- Liquibase change set to create an entity table in the database
- SpringData JPa Repository for the entity
- Service, both interface and implementation, with base CRUD operations
- DTO representation of the entity
- Mapstruct mapper to map entity to DTO
  
Resource controller that provides a rest interface for base CRUD operations
Furthermore, the resource controller will also provide the single GET endpoint with the ability to filter the entity based on its attributes (for more on this powerful feature of JHipster see: Filtering Entities)

In addition, JHipster has also performed the following tasks: configured ehcache for all our entities, created swagger documentation for rest API endpoints. Last but not least, it also generated the full Angular front end app with simple CRUD functionality for all of our entities.
