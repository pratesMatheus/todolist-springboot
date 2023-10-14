<h1 align="center"><b>To-Do List in Java</b></h1>
<i>With Spring Boot and Apache Maven</i>

<h2>About</h2>
Java application, using Spring as a framework and Maven as a package manager in building a backend with Rest architecture (w/ best practices) in a simple "To-Do List" app...

It was amazing and I loved the development experience!


<h2>Path</h2>
<i>br.com.matheusprates.todolist</i>

<h2>Libs</h2>

<ul>
<li><b>Lombok</b>: It is a Java lib that simplifies Spring Boot development, eliminating the need to write boilerplate code, such as getters, setters and constructors, making the code more concise and readable;</li>
<li><b>H2 (Database Engine)</b>: It is an in-memory database (does not require installation or configuration, and obviously cannot be used in production) that is used for development and testing in Spring Boot projects;
</li>
  <ul>
    <li>It is a <b>Spring Data JPA</b> project that simplifies interaction with relational databases, allowing CRUD operations in an easier and more efficient way, using the ORM concept. <b>NOTE</b>: uses Hibernate underneath (the most well-known Java ORM);</li>
    <li>An <b>ORM</b> (Object-Relational Mapping) is used to map objects in a software system to tables in a relational database. This facilitates data manipulation and abstracts SQL complexities, making development more efficient and less prone to errors;</li>
  </ul>
</ul>


<h2>Integration with H2 Database</h2>
Add the following dependencies to the project's <code>pom.xml</code>:

```xml
<dependencies>
  <!-- add the dependencies bellow: -->
  <dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-data-jpa</artifactId>
  </dependency>
  <dependency>
    <groupId>com.h2database</groupId>
    <artifactId>h2</artifactId>
    <scope>runtime</scope>
  </dependency>
</dependencies>
```

Add the following changes to: <code>src/resources/application.properties</code>


```sh
  spring.datasource.url=jdbc:h2:mem:todolist
  spring.datasource.driverClassName=org.h2.Driver
  spring.datasource.username=admin
  spring.datasource.password=admin
  spring.jpa.database-platform=org.hibernate.dialect.H2Dialect
  spring.h2.console.enabled=true
```

- Access the following URL: `http://localhost:8080/h2-console`

<h2>Deploy</h2>

The platform chosen to deploy the developed application was [render.com](https://render.com/), as it is a free option and with direct integration with GitHub

<h2>Thank you</h2>

Made w/ ❤ by [pratesMatheus](https://github.com/pratesMatheus "pratesMatheus").