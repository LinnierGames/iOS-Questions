1. What is Synchronous vs. Asynchronous
> These terms describe when a function will return control to the caller, and how much work will have been done by that point. A synchronous function returns only after the completion of a task that it orders. An asynchronous function, on the other hand, returns immediately, ordering the task to be done but not waiting for it. Thus, an asynchronous function does not block the current thread of execution from proceeding on to the next function.

2. What is a managed object context ?
> A managed object context represents a single object space, or scratch pad, in a Core Data application.

3. What is intrinsic content size?
> Every view that contains content can calculate its intrinsic content size. The intrinsic content size is calculated by a method on every UIView instance. This method returns a CGSize instance.

4. Explain Polymorphism
> Polymorphism is the ability of a class instance to be substituted by a class instance of one of its subclasses.

5. Explain In-app Purchase products and subscriptions
> Consumable products: can be purchased more than once and used items would have to re-purchase.
>
> Non-consumable products: user would be able to restore this functionality in the future, should they need to reinstall the app for any reason. We can also add subscriptions to our app.
>
> Non-Renewing Subscription: Used for a certain amount of time and certain content.
>
> Auto-Renewing Subscription: Used for recurring monthly subscriptions.

6. Explain what a Sequence is in Swift
> Sequence is a basic type in Swift for defining an aggregation of elements that distribute sequentially in a row. All collection types inherit from Sequence such as Array, Set, Dictionary.
	
7. What is the difference between Any and AnyObject?
> ANY can represent an instance of any type at all, including function types and optional types. 
>
> AnyObject can represent an instance of any class type.

8. What is Continuous Integration?
> Continuous integration allows us to get early feedback when something is going wrong during application development. There are a lot of continuous integration tools available.

9. What is encapsulation?
> Encapsulation is an object-oriented design principle and hides the internal states and functionality of objects. That means the objects keep their state information private.

10. Closures - value or reference types?
> Closures are reference types. If a closure is assigned to a variable and the variable is copied into another variable, a reference to the same closure and its capture list is also copied.

11. What is Singleton Pattern ? 
> The Singleton design pattern ensures that only one instance exists for a given class and that there’s a global access point to that instance. It usually uses lazy loading to create the single instance when it’s needed the first time.

12. Explain MVVM
> UIKit independent representation of your View and its state. The View Model invokes changes in the Model and updates itself with the updated Model, and since we have a binding between the View and the View Model, the first is updated accordingly.
> Your view model will actually take in your model, and it can format the information that’s going to be displayed on your view.
> There is a more known framework called RxSwift. It contains RxCocoa, which are reactive extensions for Cocoa and CocoaTouch.

13. Explain generics in Swift ?
> Generics create code that does not get specific about underlying data types. 

14. An Optional is actually a type, what data structure is it? Enum? Class? Struct?
> an optional is an enum with two cases; none, or nil, and some
````swift
    enum Optional<T> {
      case none
      case some( T )
    }
````

15. Explain final keyword into the class ?
> By adding the keyword final in front of the method name, we prevent the method from being overridden. If we can replace the final class keyword with a single word static and get the same behavior.

16. REST, HTTP, JSON — What’s that?
> HTTP is the application protocol, or set of rules, web sites use to transfer data from the web server to client. The client (your web browser or app) use to indicate the desired action:
> 
> GET: Used to retrieve data, such as a web page, but doesn’t alter any data on the server.
> 
> HEAD: Identical to GET but only sends back the headers and none of the actual data.
> 
> POST: Used to send data to the server, commonly used when filling a form and clicking submit.
> 
> PUT: Used to send data to the specific location provided.
> 
> DELETE: Deletes data from the specific location provided.
> 
> REST, or REpresentational State Transfer, is a set of rules for designing consistent, easy-to-use and maintainable web APIs.
> 
> JSON stands for JavaScript Object Notation; it provides a straightforward, human-readable and portable mechanism for transporting data between two systems. Apple supplies the JSONSerialization class to help convert your objects in memory to JSON and vice-versa.
