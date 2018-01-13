Database Notes
==================

## Relationship

| Name | Notation | Example |
| --- | --- | ---|
|One-to-many | 1:M or 1..* | One customer generates many receipts |
|Many-to-many | M:N or *..* | Many receipts record many items and those items are on many receipts |
|One-to-one | 1:1 or 1..1 | One manager per store |

## Vocab

* Attribute - characteristic of an entity
* Business rule - percise and unambiguous description of a policy, procedure or principle
* Constraint - restrictions placed on data
* DBMS (database management system) - software or envionment to manage the database
* DDL (data definition language) - enables the database admin to define the schema components
* DML (data manipulation language) - defines the environment in which the data can be managed or worked
* Entity - a thing or object in our environemnt that we want to track
* Entity set - collection of entities of the same type
* Field - a fact represented as a column
* File - the entire data structure
* OODM (object-orientated data modele) - reflects the data in an oject model  
* RDBMS (relationship database management system) - collection of programs used to manage the relational database
* Record - collection of related data items
* Relationship - association amoung entities
* Schema - conceptual organization of the whole database as viewed by the database administrator
* Subschema - defines the portion of the database as seen by an application 

## Relationships

* Hierarchical - each child has only one parent
* Object-oriented - basic data model resembling a structure
* Relational - based on mathematical set theory and represents data as independent relations

* Cardinality - one to many usually annotated with 1..* or 1..4 which denote that the link is only to 4 entities
* Modality - same is cardinality but the relation ship may not have the link


## Big Data

3Vs - volumn, velocity, and variety

Table == Entity Set

## Tables and Characteristics

### Approach 

| Table | Set | Record |
| --- | --- | --- |
| Table | Relation | Record Type |
| Row | Tuple | Record | 
| Column | Attribute | Field |

### Keys

| Key Type | Description |
| --- | --- |
| Superkey | An attribute or combination of attributes that uniquely define each row in a table |
| Candidate key | A minimal (irreducible) superkey; a superkey that does not contain a subset of attributes that is itself a super key |
| Primary key | A candidate key selected to uniquly identify all other attribute values in a given row; cannot contain null entries | 
| Foreign key | An attribute or combonation of attributes in one table whoes values must either match the primary key in another table or be null |
| Secondary key | An attribute or combonation of attributes used strickly for data retrieval purpose |
