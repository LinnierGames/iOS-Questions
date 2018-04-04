1. Explain “Arrange-Act-Assert”	
> AAA is a pattern for arranging and formatting code in Unit Tests. If we were to write XCTests each of our tests would group these functional sections, separated by blank lines:
> 
> - Arrange all necessary preconditions and inputs.
> - Act on the object or method under test.
> - Assert that the expected results have occurred.

2. Explain Swift Standart Library Protocol ?	
> There are a few different protocol. Equatable protocol, that governs how we can distinguish between two instances of the same type. That means we can analyze. If we have a specific value is in our array. The comparable protocol, to compare two instances of the same type

3. What is the difference SVN and Git ?	
> SVN relies on a centralised system for version management. It’s a central repository where working copies are generated and a network connection is required for access.
> 
> Git relies on a distributed system for version management. You will have a local repository on which you can work, with a network connection only required to synchronise.

4. What is Alamofire ?	
> Alamofire uses URL Loading System in the background, so it does integrate well with the Apple-provided mechanisms for all the network development. This means, It provides chainable request/response methods, JSON parameter and response serialization, authentication, and many other features. It has thread mechanics and execute requests on a background thread and call completion blocks on the main thread.

5. Explain Swift Package Manager	
> The Swift Package Manager will help to vastly improve the Swift ecosystem, making Swift much easier to use and deploy on platforms without Xcode such as Linux. The Swift Package Manager also addresses the problem of dependency hell that can happen when using many interdependent libraries.
> 
> The Swift Package Manager only supports using the master branch. Swift Package Manager now supports packages with Swift, C, C++ and Objective-C.

6. How is an inout parameter different from a regular parameter?
> A Inout passes by reference while a regular parameter passes by value.
