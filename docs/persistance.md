naf-persist (or networked-persist) will provide a way to store entities, so that they can be persisted by other clients. This works by storing the entity and component data in a db, and having clients smartly take ownership and recreate when applicable.

Networked entities are referenced by their network-id.

It should be noted in the current version of NAF, this would only work well for dynamically created NAF entities. Entities defined in the source html, would be created each time a new client joins, and spam the database with multiple of them. 

A singleton networked entity is what is needed in this case.

How should networked-persist handle this?
> This depends how NAF the network-id. If it uses a single network id, no matter when or who creates it, then the singleton instance created by a new client can be linked to the db. If NAF uses another mechanism to link an active instance to the singleton definition, then networked-persist will have to use that too.