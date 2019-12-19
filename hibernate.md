# Hibernate 5

## Modeling Entity Relationship

### Deciding the Cardinality of an Entity Relationship

* Q1: Can the email belong to more than one user?
* Q2: Can a customer have more than one email address?

| Q1 Answer | Q2 Answer | Relationship |
| --- | --- | --- |
| No | No | One-To-One |
| Yes | No | Many-To-One |
| No | Yes | One-To-Many |
| Yes | Yes | Many-To-Many |

### Embedded One-To-One Association

Defining the embedded class only @Basic, @Column, @Lob, @Temporal, and @Enumerated annotations can be used. It cannot maintain its own primay key with the @Id tag because its primary key is the primary key of the enclosing entity.

    @Embedded
    public  class AuthorAddress {

    }

    @Embedded
    AuthorAddress address


### Conventional One-To-One Association

The bidirectional relationship with the one-to-one association one side will need to own the relationship. That side be responsible for joining columns with a foreign key tothe otherside. The nonowning side will need to use the `mappedBy` attribute to indicate the entity that own the relationship.

    @OneToOne
    Address address;


### Many-To-One and One-To-Many Associations

The many-to-one and one-to-many assocations are the same association seen from the perspective of the owning and subordinate entities, repectively.


The `mappedBy` attribute specifies which side of the association is managed by. This tell hibernate to look at the bean specified for the configuration. To sum this up it means that the key to the relationship is on the other side.  

The `@JoinColumn` attributes indicates that this is the owner of the relationship and the foreign key. 

The owning side is the entity defined on the 'many' side of the relationship because it usually owns the foreign key.

    @Entity
    public class Email {
        @ManyToOne
        @JoinColumn(name = "employee_id")
        private Employee employee;
    }

    @Entity
    public class Employee {
        @OneToMany(mappedBy = "employee")
        private List<Email> emails;
    }


#### Cascading Operations

To have persistent operations on one entity to be applied to the linked entity the operation must be defined in the association. 

* `ALL` all operations to be cascaded to the dependent entity. This is the same as MERGE, PERSIST, REFRESH, DETATCH, and REMOVE.
* `MERGE` updates the entity's state in the database.
* `PERSIST` stores the entity's state in the database.
* `REFRESH` updates the entity's state from the database.
* `DETATCH` removes entity from managed persistence context.
* `REMOVE` deletes entity from the database
* If no cascade type is specified, no operations will be cascaded through the association.


