JPA

@EnableJpaRepositories - can have basePackage, transactionRef 
Distingush 2 Repo
@EnableJpaRepositories(basePackages = "com.acme.repositories.jpa")
@EnableMongoRepositories(basePackages = "com.acme.repositories.mongo")

interface Configuration { }

<jpa:repositories base-package=“”/> 

@NoRepositoryBean - intermediate bean. no instance will be created. 

Repository or crudRepo or paginationAndSortingRepo - 

Hibernate configuration using LocalContainerEntityFactoryBean 