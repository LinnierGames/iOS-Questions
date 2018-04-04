1. Differences between a struct and a class?
> Both class and structure can do:
> - Define properties to store values
> - Define methods to provide functionality
> - Be used in an extension
> - Conform to protocols
> - Define intialisers
> 
> Only class can do:
> - Inheritance
> - Type casting
> - Define deinitialisers
> - Allow reference counting for multiple references.

2. What is the difference Non-Escaping and Escaping Closures ?
> Escaping closure means, inside the function, you can still run the closure (or not); the extra bit of the closure is stored some place that will outlive the function. There are several ways to have a closure escape its containing function:
> 
> Asynchronous execution: If you execute the closure asynchronously on a dispatch queue, the queue will hold onto the closure for you. You have no idea when the closure will be executed and there’s no guarantee it will complete before the function returns.
> 
> Storage: Storing the closure to a global variable, property, or any other bit of storage that lives on past the function call means the closure has also escaped.

3. Explain `[weak self]` and `[unowned self]` in the context of a closure?
> unowned does the same as weak with one exception: The variable will not become nil and therefore the variable must not be an optional.
> 
> But when you try to access the variable after its instance has been deallocated. That means, you should only use unowned when you are sure, that this variable will never be accessed after the corresponding instance has been deallocated.
> 
> However, if you don’t want the variable to be weak AND you are sure that it can’t be accessed after the corresponding instance has been deallocated, you can use unowned.
> 
> By declaring it [weak self] you get to handle the case that it might be nil inside the closure at some point and therefore the variable must be an optional. A case for using [weak self] in an asynchronous network request, is in a view controller where that request is used to populate the view."

4. What is iOS 11 SDK Features for Developers ?
> - New MapKit Markers
> - Configurable File Headers
> - Block Based UITableView Updates
> - MapKit Clustering
> - Closure Based KVO
> - Vector UIImage Support
> - New MapKit Display Type
> - Named colors in Asset Catalog
> - Password Autofill
> - Face landmarks, Barcode and Text Detection
> - Multitasking using the new floating Dock, slide-over apps, pinned apps, and the new App Switcher
> - Location Permission: A flashing blue status bar anytime an app is collecting your location data in the background. Updated locations permissions that always give the user the ability to choose only to share location while using the app.

5. What is the three major debugging improvements in Xcode 8 ?
> - The View Debugger lets us visualize our layouts and see constraint definitions at runtime. Although this has been around since Xcode 6, Xcode 8 introduces some handy new warnings for constraint conflicts and other great convenience features.
> - The Thread Sanitizer is an all new runtime tool in Xcode 8 that alerts you to threading issues — most notably, potential race conditions.
> - The Memory Graph Debugger is also brand new to Xcode 8. It provides visualization of your app’s memory graph at a point in time and flags leaks in the Issue navigator.

6. What is the Test Driven Development of three simple rules ?
> - You are not allowed to write any production code unless it is to make a failing unit test pass.
> - You are not allowed to write any more of a unit test than is sufficient to fail; and compilation failures are failures.
> - You are not allowed to write any more production code than is sufficient to pass the one failing unit test.

7. Describe what “app thinning” means ?
> The store and operating system optimize the installation of iOS, tvOS, and watchOS apps by tailoring app delivery to the capabilities of the user’s particular device, with minimal footprint. This optimization, called app thinning, lets you create apps that use the most device features, occupy minimum disk space, and a

8. What are NSNotificationCenter and how does it work ?
> NSNotificationCenter is what Apple has provided as an Observer Pattern in the Cocoa library . The basic idea is that a listener registers with a broadcaster using some predefined protocol. At some later point, the broadcaster is told to notify all of its listeners, where it calls some function on each of its listeners and passes certain arguments along. This allows for asynchronous message passing between two different objects that don’t have to know about one another, they just have to know about the broadcaster.

9. What is Core Data ?
> Core Data is not an ORM or object-relational mapper. Nor is it a database. Instead, Core Data is an object graph manager which also has the ability to persist object graphs to a persistent store, on a disk.

10. What is the purpose of the reuseIdentifier ?	
> Reusability of an already allocated object.

11. Define atomic and nonatomic.	
> Atomic is the default: if you don’t type anything, your property is atomic. An atomic property is guaranteed that if you try to read from it, you will get back a valid value. It does not make any guarantees about what that value might be, but you will get back good data, not just junk memory. What this allows you to do is if you have multiple threads or multiple processes pointing at a single variable, one thread can read and another thread can write. If they hit at the same time, the reader thread is guaranteed to get one of the two values: either before the change or after the change. What atomic does not give you is any sort of guarantee about which of those values you might get. Atomic is really commonly confused with being thread-safe, and that is not correct. You need to guarantee your thread safety other ways. However, atomic will guarantee that if you try to read, you get back some kind of value.
> 
> On the flip side, non-atomic, as you can probably guess, just means, “don’t do that atomic stuff.” What you lose is that guarantee that you always get back something. If you try to read in the middle of a write, you could get back garbage data. But, on the other hand, you go a little bit faster. Because atomic properties have to do some magic to guarantee that you will get back a value, they are a bit slower. If it is a property that you are accessing a lot, you may want to drop down to nonatomic to make sure that you are not incurring that speed penalty.

12. Whats the difference between weak and strong ?
> These keywords are related to reference counting and “denote ownership”, if you will. They help you eliminate retain-release cycles by limiting what objects increment the reference count for another object. A strong property is one where you increment the reference count of the object. If object A has a strong reference to B, and no other object is referencing B, B has count 1 (A owns, or needs to exist B). Now, if B wants to have a reference to A, we would want to use a weak reference. Weak references don’t increment the reference count of the object. So in this particular case, if A has no other objects referencing it but B, A’s count would be 0 given B’s weak reference.

13. What is the difference between viewDidLoad and viewDidAppear? Which should you use to load data from a remote server to display in the view?
> viewDidLoad is called when the view is loaded, whether from a Xib file, storyboard or programmatically created in loadView. viewDidAppear is called every time the view is presented on the device. Which to use depends on the use case for your data. If the data is fairly static and not likely to change then it can be loaded in viewDidLoad and cached. However, if the data changes regularly then using viewDidAppear to load it is better. In both situations, the data should be loaded asynchronously on a background thread to avoid blocking the UI.

14. What’s the difference between using a delegate and notification?
> Both are used for sending values and messages to interested parties. A delegate is for one-to-one communication and is a pattern promoted by Apple. In delegation, the class raising events will have a property for the delegate and will typically expect it to implement some protocol. The delegating class can then call the delegates protocol methods.
> 
> Notification allows a class to broadcast events across the entire application to any interested parties. The broadcasting class doesn’t need to know anything about the listeners for this event, therefore notification is very useful in helping to decouple components in an application.

15. Which is faster: for a search an NSArray or an NSSet?
> When the order of the items in the collection is not important, NSSet offers better performance for finding items in the collection; the reason is that the NSSet uses hash values to find items (like a dictionary), while an array has to iterate over its entire contents to find a particular object.
