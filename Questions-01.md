1. What are some ways to support newer API methods or classes while maintaining backward compatibility?

```` swift
    if #available(iOS 8, *, *) {
     self.view.convertPoint(.Zero, toCoordinateSpace:anotherView) 
    } else { 
     self.view.convertPoint(CGPointZero, toView:anotherView)
    }
````

2. Difference between frame and bounds?
> The bounds of an UIView is the rectangle, expressed as a location (x,y) and size (width,height) relative to its own coordinate system (0,0). The frame of an UIView is the rectangle, expressed as a location (x,y) and size (width,height) relative to the superview it is contained within.

3. List out the different app states?
> Not running: The app has not been launched or was running but was terminated by the system.
> 
> Inactive: The app is running in the foreground but is currently not receiving events. (It may be executing other code though.) An app usually stays in this state only briefly as it transitions to a different state.
> 
> Active: The app is running in the foreground and is receiving events. This is the normal mode for foreground apps.
> 
> Background: The app is in the background and executing code. Most apps enter this state briefly on their way to being suspended. However, an app that requests extra execution time may remain in this state for a period of time. In addition, an app being launched directly into the background enters this state instead of the inactive state.
> 
> Suspended: The app is in the background but is not executing code. The system moves apps to this state automatically and does not notify them before doing so. While suspended, an app remains in memory but does not execute any code. When a low-memory condition occurs, the system may purge suspended apps without notice to make more space for the foreground app.

4. What is ARC and how is it different from Garbage collection?
> 

5. Explain unwind segue
> An unwind segue moves backward through one or more segues to return the user to a scene managed by an existing view controller.

6. Explain how to add frameworks in Xcode project without a dependency manager?
> First, choose the project file from the project navigator on the left side of the project window
> Then choose the target where you want to add frameworks in the project settings editor
> Choose the “Build Phases” tab, and select “Link Binary With Libraries” to view all of the frameworks
> 
> To add frameworks click on “+” sign below the list select framework and click on add button.

7. Explain what Lazy stored properties are and when they are useful
> Lazy stored properties are used for a property whose initial values are not set until the first time it is used. You can declare a lazy stored stored property by writing the lazy modifier before its declaration. Lazy properties are useful when the initial value of a property is reliant on outside factors whose values are unknown.

8. Where do we use dependency injection?
> We use a storyboard or xib in our iOS app, then we created IBOutlets. IBOutlet is a property related to a view. These are injected into the view controller when it is instantiated, which is essentially a form of Dependency Injection. There are forms of dependency injection: constructor, property and method.

9. What is the difference between method overriding and method overloading?
> Overriding is when you create a subclass with a function identical (or near identical) to one in its superclass. 
>
> Whereas overloading is when a function of the same name takes a different type of argument. 

10. Explain what is the defer keyword? 
> defer keyword which provides a block of code that will be executed in the case when execution is leaving the current scope.

11. What are benefits of Guard?
> There are two big benefits to guard. One is avoiding the pyramid of doom, as others have mentioned — lots of annoying if let statements nested inside each other moving further and further to the right. The other benefit is provide an early exit out of the function using break or using return.

12. What is the difference fileprivate, private, internal, and public, private(set) access level?
> fileprivate is accessible within the current file, private is accessible within the current declaration.
>
> internal, is the default, is accessible within the current module. Each app, or framework, is its own module
>
> public vars or classes are accessible outside of its module but cannot be subclassed or overriden 
>
> open class members and classes are also accessible outside the current module but can be subclassed or overriden from outside of the module
>
> public private(set) means getter is public, but the setter is private.

[Apple Docs](https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/AccessControl.html), scroll to **Access Control**

13. What is Downcasting?
> When we’re casting an object to another type in Objective-C, it’s pretty simple since there’s only one way to do it. In Swift, though, there are two ways to cast — one that’s safe and one that’s not .
>
> `as` used for upcasting and type casting to bridged type
>
> `as?` used for safe casting, return nil if failed
>
> `as!` used to force casting, crash if failed. should only be used when we know the downcast will succeed.
