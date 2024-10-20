# Software Engineeering Best Practices

Here are some best practices in software engineering:


## SOLID 

The SOLID principles are a set of five design principles in software engineering that aim to create more maintainable, robust, flexible, extensible, and understandable code for object-oriented software systems and solve particular problems that might arise while developing software systems.

Each principle focuses on a specific aspect of software design and encourages practices that lead to modular and well-structured code. The five SOLID principles are:
 
- Single Responsibility: This principle states that a class should have only one reason to change. In other words, a class should have a single responsibility or job. This promotes high cohesion, where each class focuses on doing one thing well, making the code easier to understand, maintain, and extend.

- Open Closed: The Open-Closed Principle suggests that software entities (classes, modules, functions, etc.) should be open for extension but closed for modification. This means that you can add new functionality without modifying existing code. This is typically achieved through abstraction, inheritance, and polymorphism.

- Liskov Substitution: The Liskov Substitution Principle states that objects of a derived class should be able to replace objects of the base class without affecting the correctness of the program. In simpler terms, if a class is a subclass of another class, it should be able to be used interchangeably with the parent class without introducing unexpected behavior.

- Interface Segregation: The Interface Segregation Principle suggests that clients should not be forced to depend on interfaces they don't use. In other words, interfaces should be specific and fine-grained, tailored to the needs of the implementing classes. This prevents classes from being burdened with methods they don't need.

- Dependency Inversion: The Dependency Inversion Principle states that high-level modules should not depend on low-level modules; both should depend on abstractions. Additionally, abstractions should not depend on details; details should depend on abstractions. Polymorphism is a form of abstraction. This promotes loose coupling and flexibility, allowing components to be easily replaced or extended without affecting the entire system.

Following these SOLID principles helps developers create more modular, maintainable, and adaptable software systems. By designing code with these principles in mind, developers can reduce code duplication, improve readability, and make future changes and additions to the codebase smoother and less error-prone.

They work in tandem with the 4 pillars of OOP: Encapsulation, Abstraction, Polymorphism, Inheritance

## Code Maintainability:
- Write clean and readable code that is easy to understand and maintain.

- Use meaningful variable and function names, follow coding conventions, and include comments when necessary.

- Break down complex code into smaller, reusable functions or modules.

- Write unit tests to ensure code correctness and facilitate future changes. Use ESlint etc.

## Modularity and Reusability:
- Design your codebase with modular components that have clear responsibilities.

- Encapsulate functionality into reusable functions, classes, or modules.

- Aim for loose coupling between modules to make them more independent and interchangeable.

- Use design patterns and principles like SOLID to create modular and extensible code.

## Version Control:
- Utilize version control systems (e.g., Git) to track and manage changes in your codebase.

- Follow best practices for branching, merging, and committing code.

- Use descriptive commit messages to provide clear information about changes.

## Testing and Quality Assurance:
- Write automated tests to verify the correctness of your code and prevent regressions.

- Adopt test-driven development (TDD) or behavior-driven development (BDD) approaches.

- Perform code reviews to ensure code quality and catch potential issues early.

- Use static code analysis tools to identify potential bugs, code smells, or security vulnerabilities (TypeScript, ESLint, SonarCube etc).

#### What to look out for in Unit Tests

 A well-designed suite of unit tests provides a safety net for making changes and additions to your codebase with confidence.

- Isolation: Each unit test should be isolated, meaning it tests a specific piece of functionality without relying on external factors or dependencies.

- Coverage: Tests should cover a wide range of scenarios and edge cases to ensure that the code behaves correctly in various situations.

- Assertion: Clear and meaningful assertions should be present to verify that the expected outcome matches the actual outcome.

- Independence: Tests should not depend on the order of execution or the results of other tests.

- Fast Execution: Unit tests should run quickly to allow for frequent execution during development.

- Readability: Tests should be easy to read and understand by using descriptive names and clear structure.

- Maintainability: Tests should be easy to maintain as the code evolves, without requiring frequent updates.

- Consistency: Test naming conventions, structure, and organization should be consistent across the codebase.

- Mocking: Dependencies should be mocked or stubbed to isolate the code being tested.

- Refactoring Safety: Tests should catch regressions and breakages when code is refactored.

- Error Handling: Tests should cover error scenarios and ensure that error-handling code functions correctly.
  
- Good commenting


#### Related Resource:
https://github.com/kukuu/quality-assurance

## Documentation:
- Document your codebase, including high-level architecture, important design decisions, and any complex logic.

- Document APIs and provide clear instructions on how to use them.

- Create README files or wikis with setup instructions, troubleshooting guides, and examples.

## Performance Optimization:
- Profile and optimize your code for better performance when necessary.

- Identify and eliminate bottlenecks, reduce unnecessary computations, and optimize algorithms.

- Follow best practices for database queries, caching, and network requests.

- Manage Technical Debt efficiently

https://github.com/kukuu/integration/blob/main/clent-side-caching.md

## Security:
- Implement secure coding practices to protect against common vulnerabilities (e.g., SQL injection, cross-site scripting).

- Validate and sanitize user input to prevent malicious activities.

- Keep libraries and dependencies up to date to address security vulnerabilities.

- Vulnerabilities to look out for:

      i. Broken Access control

      ii. Cryptographic failure

      iii. Insecure design

      iv. SQL Injection Attacks

      v. DOS Attack

      vi. DDOS Attack

      vii. Authentication and Authorisation failures

      viii. Cross-Site Scripting

      ix. Malware and Phishing.

      x. Authentication: Used SSO, 2FA, OAuth for the Backend.

## Continuous Integration and Deployment:
- Adopt continuous integration (CI) practices to automatically build, test, and validate code changes.

- Automate deployment processes to ensure consistent and reliable deployments.

- Use tools like continuous deployment (CD) pipelines for smooth and efficient software releases.

## Collaboration and Communication:
- Foster effective collaboration among team members through clear communication and documentation.

- Use collaboration tools (e.g., project management, issue tracking, team chat) to facilitate communication and coordination.

- Embrace agile methodologies and regular feedback loops to iterate and improve software development.


## Continuous Delivery (RRASc)

Reliable :: Repeatable :: Automation :: Source control

 CD is the ability to get changes of all types including new features, configuration changes, bug fixes and experiments into production, or into the hands of users, safely and quickly in a sustainable way. 

 A logical extension of Continuous Integration (CI), It is based on the use of smart automation. This is all about creating a repeatable and reliable process for delivering software. You have to automate pretty much everything in order to be able to achieve continuous delivery. Manual steps will get in the way or become a bottleneck. This goes for everything from requirements authoring to deploying to production.

The ultimate goal of continuous delivery is to minimise the iteration time of the code-test-deliver-measure experimentation cycle. Increasing deliverable throughput in this way is the key to not only more feature work being delivered but higher quality code as well. This might seem counter-intuitive at first but code is fixed and polished through that same cycle and less time spent on deployment is more time spent on designing quality code.

	The high-level requirements FOR CD are:

	1. Software must be easily testable, which means it must be loosely coupled.

	2. Delivery must—under normal circumstances—require minimal human interaction.

	3. Delivery—from commit to production—must be fast. Preferably under 10 minutes.

	4. Rolling back a deployed feature if it is found to be broken or unwanted must be trivial.

	5. Build binaries only once. Binaries should be compiled once and once only. 
	   The binary should then be stored in some place (perhaps s3) which is accessible only to your deployment mechanism/instances, 
	   and your deployment mechanism should deploy this same binary to each successive environment

	6. Use precisely the same mechanism (Docker) to deploy to every environment. Both QA and production
	   deployment must be both automated.

	7. Smoke test your deployment. Write a smoke test and include that in the deployment process.

	8. Stop the lines if anything fails.

#### CI/CD Guiding Principles

	1. The process for releasing/deploying software MUST be repeatable and reliable (RR). 

	2. Automate everything!

	3. If somethings difficult or painful, do it more often.

	4. Keep everything in source control

	5. Done means “released”.

	6. Build quality in. 

	7. Everybody has responsibility for the release process

	8. Improve continuously

