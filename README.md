# Aprender el lenguaje [Java 25]

📖 **Lea el tutorial: [https://stahe.github.io/ales-java-oct-2026/](https://stahe.github.io/ales-java-oct-2026/)**

Este curso enseña el lenguaje [Java](https://dev.java/) 25 **mediante ejemplos**: más de doscientos programas (320 archivos Java), comentados línea por línea, con sus resultados de ejecución incluidos. Parte de los fundamentos del lenguaje y abarca el acceso a bases de datos con JDBC y Hibernate, la programación de redes y los servicios web con Spring Boot.

Es la adaptación a Java del curso [Aprender C# 14 con .NET 10](https://stahe.github.io/ales-csharp-oct-2026/) (octubre de 2026), que a su vez es una reescritura de un curso de C# de 2008: el mismo esquema, los mismos ejemplos, el mismo hilo conductor, pero escrito en Java moderno. Todos los programas compilan **sin errores ni advertencias** con JDK 25 (`javac -Xlint:all`) y se han ejecutado; los resultados que se muestran en el curso son los de estas ejecuciones.

| Curso de C# 14 (2026) | Curso de Java 25 (2026) |
|---|---|
| C# 14, .NET 10 (LTS) | Java 25 (LTS), JDK 25 |
| aplicaciones de un solo archivo (`dotnet run prog.cs`) | archivos fuente compactos (`java Prog.java`) |
| proyectos `.csproj`, soluciones `.slnx`, NuGet | proyectos Maven (`pom.xml`), Maven Central |
| propiedades, estructuras, sobrecarga de operadores | métodos de acceso, records, clases selladas, coincidencia de patrones |
| LINQ | Stream API |
| delegados y eventos | interfaces funcionales, lambdas, listeners |
| `Task`, `async` / `await` | `CompletableFuture`, hilos virtuales |
| MSTest, Microsoft.Extensions.DependencyInjection | JUnit 6, Spring Framework 7 |
| System.Text.Json | Jackson 3 |
| ADO.NET, MySqlConnector | JDBC, MySQL Connector/J, HikariCP |
| Entity Framework Core | **Hibernate 7** (Jakarta Persistence 3.2) |
| `HttpClient`, `TcpClient` / `TcpListener` | `java.net.http.HttpClient`, `Socket` / `ServerSocket` |
| ASP.NET Core Minimal API | Spring Boot 4 |

## Esquema del curso

| Capítulo | Contenido |
|---|---|
| Instalación | JDK 25, IntelliJ IDEA / VS Code, los comandos `java` y `javac`, archivos fuente compactos, Maven, proyectos multimódulo |
| Fundamentos del lenguaje | tipos, `var`, bloques de código, conversiones, arreglos, operadores, expresiones `switch` y coincidencia de patrones, excepciones verificadas y no verificadas, `try` con recursos, enumeraciones, paso de parámetros |
| Clases, records, interfaces | clases, herencia, polimorfismo, clases selladas, `equals` / `hashCode` / `compareTo`, interfaces, clases abstractas, genéricos, paquetes y módulos, records, coincidencia de patrones sobre objetos, `Optional` |
| Clases de Java de uso frecuente | cadenas, arreglos, colecciones (incluidas las colecciones secuenciadas), **Stream API** y `Gatherers`, archivos de texto y binarios (`java.nio.file`), JSON con Jackson 3, expresiones regulares |
| Arquitecturas en capas | capas [DAO] / [negocio] / [UI], proyectos Maven multimódulo, pruebas unitarias con **JUnit 6**, **inyección de dependencias** con Spring |
| Interfaces funcionales, lambdas y eventos | `java.util.function`, lambdas, referencias a métodos, clausuras, composición, listeners de eventos, `PropertyChangeSupport` |
| Hilos de ejecución | `Thread`, **hilos virtuales**, `synchronized`, `ReentrantLock`, `Condition`, operaciones atómicas, `Semaphore`, `CountDownLatch`, colecciones concurrentes, `ExecutorService`, fork/join, `ThreadLocal`, `ScopedValue` |
| Programación asíncrona | `CompletableFuture` e hilos virtuales, composición, excepciones, cancelación y tiempos de espera, progreso, E/S asíncrona, `Flow`, concurrencia estructurada (visión general) |
| Acceso a bases de datos con JDBC | MySQL, MySQL Connector/J, `DataSource` y HikariCP, consultas parametrizadas e inyección SQL, transacciones, lotes, `CachedRowSet` |
| **Hibernate** | entidades, `SessionFactory` / `Session`, CRUD, contexto de persistencia, HQL y Criteria API, relaciones y carga diferida, migraciones, concurrencia optimista, SQL nativo, `StatelessSession`, Spring ORM y `@Transactional` |
| Programación web | TCP/IP, IPv6, `InetAddress`, clientes y servidores TCP (un hilo virtual por cliente), HTTP, `HttpClient`, SMTP |
| Servicios web | REST / JSON con **Spring Boot 4**, clientes de consola en Java, cliente web en JavaScript, cliente Node.js |

## El hilo conductor: una calculadora del impuesto sobre la renta en 9 versiones

A lo largo del curso, versión a versión, se construye una aplicación de **cálculo del impuesto sobre la renta**:

- **Versión 1**: un único programa; **Versión 2**: clases e interfaces; **Versión 3**: datos leídos desde un archivo de texto o JSON;
- **versiones 4 y 5**: una arquitectura en capas que usa módulos Maven, probada con JUnit e integrada mediante inyección de dependencias con Spring;
- **versiones 6 y 7**: datos almacenados en una base de datos MySQL, leídos mediante JDBC y luego Hibernate;
- **versión 8**: un servidor TCP para el cálculo del impuesto y su cliente;
- **Versión 9**: un servicio web REST con Spring Boot, su cliente de consola y su cliente web.

## Tecnologías

Java 25 · JDK 25 · Maven 3.9 · IntelliJ IDEA · VS Code · JUnit 6 · Spring Framework 7 · Jackson 3 · MySQL 8 · MySQL Connector/J 9 · HikariCP · Hibernate ORM 7.4 · Jakarta Persistence 3.2 · Spring Boot 4.1 · Laragon

## Requisitos previos

- Experiencia previa en programación en cualquier lenguaje.
- Un [JDK 25](https://adoptium.net) (Eclipse Temurin u otra distribución), [Maven](https://maven.apache.org) y un IDE ([IntelliJ IDEA](https://www.jetbrains.com/idea/) o [VS Code](https://code.visualstudio.com) con el Extension Pack for Java); [Laragon](https://laragon.org) para MySQL (capítulos sobre bases de datos). Las instrucciones de instalación se proporcionan en el curso.

## Autor

Este curso y su código fueron escritos por **Claude**, la IA de [Anthropic](https://www.anthropic.com) (octubre de 2026), a petición de Serge Tahé, a partir de su curso de C# 14.

Revisor: [Serge Tahé](https://stahe.github.io)
