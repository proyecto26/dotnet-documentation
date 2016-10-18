# .Net Starter Template (to whom it may concern)
SOLID, DI, N-Tier, Logs

# Tools
* **[ASP.NET Dynamic Data](https://msdn.microsoft.com/en-us/library/ee845452.aspx)**: Dynamic Data enables you to create a data-driven Web site with little or no coding (Only a simple CRUD).

# Layered Architectural Pattern (separation of concerns)
* Layered Architectures keep the Software flexible, more resilient to change.
* Allows you to change underlying technologies and implementations.
* Allow you to change how you package and deploy your application.

# Domain Layer
The logic of the business, is a model of business. The rules and needs of the business with the workflow.
Domain Layer is all about the business problem - so keep ti "pure" (Only C# classes, methods, properties, interfaces, enums), free of specific technologies, API's, libraries, frameworks, etc.
The Domain Layer is the main unifying concept of the application... bridging  technical concepts and business concepts. Starting with the Domain Layer help us utilize Test Driven Development. Not every application needs the complexity introduced by a domain layer.

# Presentation Layer
UI Components and Process Components. It should do basic/simple formatting and validation. Also responsible for displaying exceptions, asking for user input on what to do next

# Persistence Layer
The communication with Domain Layer is through C# interfaces/Contracts using Inversion of Control and Dependency Inversion.
The Domain Layer only cares that the Persistence Layer abides by the terms of the contract. Besides CRUD operations, the Persistence Layer should also enforce data integrity constraints, validations, transactions, connection pooling, security, etc.
Object Relation Mappers are used to mapping relational data to object instances. The Persistence Layer is merely an implementation detail (The security is in the Domain).

  To transfer data the following types are used:
  * Simple Types
  * Plain Old CLR Objects (POCOs)
  * Generic Collections of Objects
  * Object Graphs (Relationships of Objects)

# Application Services Layer
Application Services layer orchestrates lower-level, chattier methods to solve higher-level domain-specific problems. Focus on have Cohesive methods and classes adhere to SRP and DRY.
The Application Services Layer has methods that serve the Presentation Layer by rolling-up many lower-level methods into fewer higher-level methods, orchestrating those lower-lever methods to coordinate/collaborate a solution.

# Web Services Layer

# Data Transfer Objects

# Concepts
* **Layers:** are about logical organization of code.
* **Tiers:** are the physical deployment of layers (only about where the code runs).
* **Cross-cutting concerns:** are aspects of a program that affect other concerns (Security, Communication, Operational Management, etc).
* **DRY:** Don't repeat yourself. "Every piece of knowledge must have a single, unambiguous, authoritative representation within a system".
* **SRP:** Single responsibility principle. Every module or class should have responsibility over a single part of the functionality provided by the software, and that responsibility should be entirely encapsulated by the class. "A class should have only one reason to change".
* **YAGNI:** You aren't gonna need it. "Always implement things when you actually need them, never when you just foresee that you need them".
* **TDD:** Test Driven Design.
* **DDD:** Domain Driven Design.
* **Architecture:** Application architecture seeks to build a bridge between business requirements and technical requirements by understanding use cases, and then finding ways to implement those use cases in the software.
* **Facade:** Common pattern name used to identify a thin layer of code that wraps around other code to present a "friendly" interface/interaction.
* **SOLID:** single responsibility, open-closed, Liskov substitution, interface segregation and dependency inversion. The intention is that these principles, when applied together, will make it more likely that a programmer will create a system that is easy to maintain and extend over time.

