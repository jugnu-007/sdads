

### Software Design Approach


  
A software design approach is a method or strategy used to structure, plan, and organize the development of software systems. It encompasses various principles, practices, and techniques that guide software engineers in designing software that meets the desired requirements and specifications. These approaches help in managing complexity, improving maintainability, and ensuring that the software is reliable and scalable.


| Aspect       | Function Oriented Approach                                                     | Object Oriented Approach                                                                                                            |
| ------------ | ------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------- |
| Abstraction  | The basic abstractions, which are given to the user, are real world functions. | The basic abstractions are not the real world functions but are the data abstraction where the real world entities are represented. |
| Execute      | carried out using  structured analysis and structured design                   | Carried out using UML                                                                                                               |
| Approach     | It is a top down approach.                                                     | It is a bottom up approach.                                                                                                         |
| Reusability  | Functions are not inherently reusable.                                         | Objects are designed for reusability, through inheritance and composition.                                                          |
| Polymorphism | Achieved through function overloading and function overriding.                 | Achieved through method overriding and interfaces.                                                                                  |
| Examples     | Procedural programming languages like C.                                       | Object-oriented programming languages like Java, C++, Python.                                                                       |


### UML

UML (Unified Modeling Language) diagrams are graphical representations of a system or software application's structure, behavior, and interactions. They are used by software developers, analysts, and stakeholders to understand, design, and communicate about the system. UML diagrams are standardized and provide a way to visualize different aspects of a system, making it easier to understand its architecture and design.

There are several types of UML diagrams, each serving a different purpose:

1. **Class Diagram**: Shows the static structure of the system, including classes, attributes, operations, and relationships between classes.
    
2. **Use Case Diagram**: Describes the functionality of the system from the user's perspective, showing interactions between actors (users) and the system.
    
3. **Sequence Diagram**: Illustrates how objects interact in a particular scenario of a use case, showing the messages exchanged between objects over time.
    
4. **Activity Diagram**: Represents the flow of control in a system, showing the sequence of activities and decision points.
    
5. **State Diagram**: Shows the different states of an object and how it transitions between states in response to events.
    
6. **Component Diagram**: Represents the physical components of the system and their dependencies.
    
7. **Deployment Diagram**: Shows the physical deployment of software components to hardware nodes.
    

UML diagrams provide a common language for developers and stakeholders to communicate and collaborate during the software development process.





### Use case Diagram

  
A use case diagram is a type of UML (Unified Modeling Language) diagram that represents the functionality of a system from the user's perspective. It depicts the various interactions between users (actors) and the system to achieve specific goals (use cases). Use case diagrams are used to visualize the functional requirements of a system and help in identifying and organizing the system's functionalities.

In a use case diagram, the following elements are typically included:

1. **Actor**: Represents a user or an external system that interacts with the system. Actors are usually depicted as stick figures.
    
2. **Use Case**: Represents a specific functionality or task that the system performs to achieve a goal for an actor. Use cases are depicted as ovals.
    
3. **Association**: Represents the relationship between an actor and a use case, indicating that the actor is involved in the use case. Associations are depicted as lines connecting actors to use cases.
    
4. **System Boundary**: Represents the scope of the system, which defines what is inside the system and what is outside. It is usually depicted as a rectangle that encompasses all the use cases.
    

Use case diagrams help in understanding the functional requirements of a system by visualizing how users interact with the system to accomplish tasks. They are often used during the early stages of software development to capture and communicate the system's behavior and requirements.





### Include Relationship vs Extend Relationship

| Aspect               | Include Relationship                                           | Extend Relationship                                             |
|----------------------|------------------------------------------------------------------|------------------------------------------------------------------|
| Purpose              | Describes a common behavior that is shared across multiple use cases. | Describes optional or alternative behaviors that are not always included in the base use case. |
| Dependency           | The base use case always includes the included use case.         | The extension use case is optional and may or may not be included based on certain conditions. |
| Notation             | Shown as a dashed arrow with an open arrowhead pointing from the including use case to the included use case. | Shown as a dashed arrow with an open arrowhead pointing from the extending use case to the extended use case. |
| Example              | A 'Submit Order' use case includes 'Validate Order' and 'Calculate Total'. | A 'Manage User Account' use case can extend 'Login' with an optional 'Forgot Password' extension. |

In summary, the `include` relationship is used when a use case includes another use case as part of its behavior, while the `extend` relationship is used when a use case extends another use case with optional or alternative behavior.





### Coding Standards and Guidelines



Coding standards and guidelines are sets of rules and best practices that developers follow when writing code. These standards help ensure that code is readable, maintainable, and consistent across a project or organization. Here are some common coding standards and guidelines for software engineering:

1. **Naming Conventions**: Use meaningful names for variables, functions, classes, and other elements. Follow a consistent naming convention (e.g., camelCase, PascalCase, snake_case) throughout the codebase.

2. **Formatting**: Use consistent indentation, spacing, and line breaks to improve code readability. Consider using automated code formatting tools to enforce formatting standards.

3. **Comments**: Use comments to explain the purpose of code, especially for complex or non-obvious logic. Avoid excessive comments that state the obvious.

4. **Error Handling**: Implement proper error handling mechanisms to gracefully handle exceptions and errors. Avoid swallowing exceptions without proper logging or handling.

5. **Code Structure**: Organize code into logical modules, classes, and functions. Use meaningful file and directory structures to facilitate code navigation.

6. **Code Reuse**: Encapsulate reusable code into functions, classes, or modules to promote code reusability and maintainability.

7. **Performance Considerations**: Write efficient code by avoiding unnecessary loops, excessive memory usage, and redundant calculations. Consider performance implications when designing algorithms and data structures.

8. **Security Practices**: Follow security best practices to protect against common vulnerabilities such as SQL injection, cross-site scripting (XSS), and cross-site request forgery (CSRF).

9. **Version Control**: Use version control systems (e.g., Git) to manage code changes, track history, and collaborate with team members.

10. **Testing**: Write testable code and include unit tests, integration tests, and other forms of automated testing to ensure code correctness and reliability.

It's important for development teams to establish and follow coding standards and guidelines to maintain code quality, improve collaboration, and reduce maintenance overhead.




### Code review techniques

Code review techniques are methods used to evaluate and improve the quality of code through peer review. These techniques help in identifying issues, improving code readability, ensuring adherence to coding standards, and sharing knowledge among team members. Some common code review techniques include:

1. **Pair Programming**: Two developers work together on the same code, with one writing the code and the other reviewing it in real-time. This technique can lead to immediate feedback and can improve code quality.
    
2. **Tool-Assisted Code Review**: Various tools are used to automate the code review process. These tools can check for coding standards, detect bugs, and provide suggestions for improvement.
    
3. **Checklists**: Developers use predefined checklists to review code for common issues such as code formatting, error handling, performance optimizations, and security vulnerabilities.
    
4. **Over-the-Shoulder Review**: A more experienced developer reviews the code of a less experienced developer while sitting together. This technique allows for immediate feedback and knowledge sharing.
    
5. **Email-Based Code Review**: Code changes are sent via email to team members for review. Comments and feedback are provided through email threads.
    
6. **Meeting-Based Review**: Team members gather in a meeting to discuss and review code changes. This can be done in person or through video conferencing.
    
7. **Ad Hoc Review**: Code changes are reviewed informally whenever a team member has time. This can be done by walking through the code changes together or leaving comments in the code.
    

Each of these techniques has its strengths and weaknesses, and the choice of technique depends on factors such as team size, project requirements, and time constraints.
