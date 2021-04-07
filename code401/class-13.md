# Relationshisps in Spring Data Rest

Spring data rest allows you to define one to one relationships between entities.You can do this by using the;

- @OneToOne annotation

@Entity
public class Library {

    @Id
    @GeneratedValue
    private long id;

    @Column
    private String name;

    @OneToOne
    @JoinColumn(name = "address_id")
    @RestResource(path = "libraryAddress", rel="address")
    private Address address;
    
    // standard constructor, getters, setters
}

- Creating repositories interfaces for each of the entities that extends CrudRepository interface.

public interface LibraryRepository extends CrudRepository<Library, Long> {}
public interface AddressRepository extends CrudRepository<Address, Long> {}


- Creating Resources

- Creating associations


You can also define one-to-many relationships using the @Many-To-One annotation.