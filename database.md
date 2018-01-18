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

### Referential Integrity

There are 3 types of rules:
* Delete
* Insert
* Update

#### Delete Rules

This rule states that if an attempt is made to delete a record in one table where one or more records with matching foreign key values exist in another table:

* Cascade Delete: All associated records will be deleted.
* Restrict Delete: The delete operation will not be allowed.
* Set-to-Null Delete: The foriegn key values are set to Null so we know that the record they used to point to has been deleted.


## ERM - Entity Relationship Model

ERD - The ERD represents the conceptual database as viewed by the end user. Whereby it depicts the database's main components: entities, attributes and relationships.

* Entities - correspond to a table
* Attributes - charateristics of entities and each one has a domain or a set of possible values
* Identifiers(primary keys) - used to uniquely identify each entity instance
* Composite Identifier - more than one attribute that make up the unique identifier

### Composite and Simple Attributes

The two type of attributes are composite and simple. The simple type are an attribute that cannot be broken up into additional attributes. Whereas a composite is made up of additional attributes. Example of a simple attribute would be maritial status and a composite is and address. An address is made up of multiple simple attributes like the city, state and zip code.

* Single-Valued Attribute - is an attribute that is made up of only a single value.
* Multivalue Attribute - are attributes that can have many values
* Derived Attribute - are attributes that are calculated from other attributes.

### Connectivity and Cardinality

Connectivity is used to describe the relationship classification. Where cardinality expresses that minimum and maximum number of occurences of a related entity in the format of (x,y). The first number represents the minimum number of associated entities and the second is the maximum. Whereby cardinalities are usually established by business rules.

### Existence Dependence

* An entity is said to be existence dependence if it can exist in the database only when it's associated with another entity occurance.
* An entity is said to be existence independence if it can exist in the database apart from all of its related entities. They're referered to as a strong or regular entity.

### Relationships

* Weak or non-identifying relationship -  A relationship in which the primary key of the related entity does not contain a primary key of the parent entity.
* Strong or identifying relationship - A relationship that occurs when two entities are existence-dependent whereby the primary key of the parent makes up the primary key of the related entity.

### Weak Entities

These are entities that are dependent on another enity to exist. An example is a dependent child on insurance. They wouldn't exist unless the primary existed. 

A weak entity must meet two conditions:
1. The entity is existance-dependent; it cannot exist without the entity it has the primary relationship with.
1. The entity has a primary key that is partially or totally derived from the parent entity in the relationship.

##  Normalization

| Level | Definition | Description |
|--- |--- |---|
| first normal form (1NF) | The first stage in the normalization process. It describes a relation depicted in tabular format, with no repeating groups and a primary key identified. All nonkey attributes in the relation are dependent on the primary key. | 1. Table format 2. Each row is unique 3. Pk identified |
| second normal form (2NF) | The second stage in the normalization process, in which a relation is in 1NF and there are no partial dependencies (dependencies in only part of the primary key). | 1. Already in 1NF 2. All the non-key columns are dependent on the table’s primary key |
| third normal form (3NF) | A table is in 3NF when it is in 2NF and no nonkey attribute is functionally dependent on another nonkey attribute; that is, it cannot include transitive dependencies. | 1. Already in 2NF 2. It contains only columns that are non-transitively dependent on the primary key |
| fourth normal form (4NF) | A table is in 4NF if it is in 3NF and contains no multiple independent sets of multivalued dependencies. | |

* Transitive dependence to mean a column’s value relies upon another column through a second intermediate column

1. A table that has all key attributes defined, has no repeating groups, and all its attributes are dependent on the primary key
