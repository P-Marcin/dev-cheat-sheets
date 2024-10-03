# :clipboard: PROPERTIES

The `application.properties` file name with `-` like: `application-someprofile.properties` becomes a profile.

## :pushpin: Spring Core

* `spring.application.name` - indicates the name of spring application
* `logging.level.package` - sets [logging level](https://docs.spring.io/spring-boot/docs/2.1.13.RELEASE/reference/html/boot-features-logging.html#boot-features-custom-log-levels) of the package

## :pushpin: Spring Boot DEV Tools

* `spring.devtools.livereload.enabled` [default: `true`] - disables embedded LiveReload server

## :pushpin: Spring Data REST

* `spring.data.rest.base-path=/api/v1` - sets rest base path to `/api/v1`

## :pushpin: Spring Data JPA

* `spring.h2.console.enabled` [default: `false`] - enables H2 in-memory Database web console. The url is http://localhost:8080/h2-console and connection details can be found in spring logs

## :pushpin: Database

* `spring.datasource.username` - login user of the database
* `spring.datasource.password` - login password of the database
* `spring.datasource.url` - JDBC url of the database
* `spring.datasource.driver-class-name` - fully qualified name of the JDBC driver, auto-detected based on the URL by default
* `spring.jpa.database` - configures Spring JPA to use specific database
* `spring.jpa.properties.hibernate.dialect` - configures Spring JPA Hibernate dialect
* `spring.jpa.hibernate.ddl-auto` - controls Hibernate’s database initialization. How to Guide: [Database Initialization](https://docs.spring.io/spring-boot/how-to/data-initialization.html)
* `spring.jpa.properties.hibernate.show_sql` - writes all SQL statements to console
* `spring.jpa.properties.hibernate.format_sql`- pretty prints the SQL statements in console
* `logging.level.org.hibernate.orm.jdbc.bind=trace` - writes binding parameters of SQL statements to console
* `spring.jpa.properties.jakarta.persistence.schema-generation.scripts.action=drop-and-create` - defines which scripts the persistence provider shall create
* `spring.jpa.properties.jakarta.persistence.schema-generation.scripts.create-source=metadata` - defines how the schema shall be created (in this case based on the mapping metadata)
* `spring.jpa.properties.jakarta.persistence.schema-generation.scripts.drop-target=drop-and-create.sql` - defines the target location of the drop script generated by the persistence provider
* `spring.jpa.properties.jakarta.persistence.schema-generation.scripts.create-target=drop-and-create.sql` - defines the target location of the create script generated by the persistence provider

HikariCP configuration example can be found [here](https://github.com/brettwooldridge/HikariCP/wiki/MySQL-Configuration). HikariCP list of properties can be found [here](https://github.com/brettwooldridge/HikariCP?tab=readme-ov-file#gear-configuration-knobs-baby):
* `spring.datasource.hikari.pool-name` - sets the name of the Hikari Pool
* `spring.datasource.hikari.maximum-pool-size` - configures maximum Hikari Pool size. [About Pool Sizing](https://github.com/brettwooldridge/HikariCP/wiki/About-Pool-Sizing)