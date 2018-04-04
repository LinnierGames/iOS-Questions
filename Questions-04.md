1. What’s accessibilityHint?
> accessibilityHint describes the results of interacting with a user interface element. A hint should be supplied only if the result of an interaction is not obvious from the element’s label.

2. What is Instruments?
> Instrument is a powerful performance tuning tool to analyze that performance, memory footprint, smooth animation, energy usage, leaks and file/network activity.

3. What is Deep Linking?
> Deep linking is a way to pass data to your application from any platform like, website or any other application. By tapping once on link, you can pass necessary data to your application.

4. What is an “app ID” and a “bundle ID” ?
> A bundle ID is the identifier of a single app. For example, if your organization’s domain is xxx.com and you create an app named Facebook, you could assign the string com.xxx.facebook as our app’s bundle ID.
> 
> An App ID is a two-part string used to identify one or more apps from a single development team. You need Apple Developer account for an App ID.

5. What is Factory method pattern?	
> Factory method pattern makes the codebase more flexible to add or remove new types. To add a new type, we just need a new class for the type and a new factory to produce it like the following code. For more information check this out.

6. What is CoreSpotlight?	
> CoreSpotlight allows us to index any content inside of our app. While NSUserActivity is useful for saving the user’s history, with this API, you can index any data you like. It provides access to the CoreSpotlight index on the user’s device.

7. What are layer objects?	
> Layer objects are data objects which represent visual content and are used by views to render their content. Custom layer objects can also be added to the interface to implement complex animations and other types of sophisticated visual effects.

8. Explain AVFoundation framework	
> We can create, play audio and visual media. AVFoundation allows us to work on a detailed level with time-based audio-visual data. With it, we can create, edit, analyze, and re-encode media files. AVFoundation has two sets of API, one that’s video, and one that is audio.

9. What’s the difference between accessibilityLabel and accessibilityIdentifier?
> accessibilityLabel is the value that’s read by VoiceOver to the end-user. As such, this should be a localized string. The text should also be capitalized. Because this helps with VoiceOver’s pronunciation. accessibilityLabel is used for testing and Visual Impaired users.
> 
> accessibilityIdentifier identifies an element via accessibility, but unlike accessibilityLabel, accessibilityIdentifier's purpose is purely to be used as an identifier for UI Automation tests. We use a value for testing process.

10. Explain Property Observer
> A property observer observes and responds to changes in a property’s value. With property observer, we don’t need to reset the controls, every time attributes change.

11. What’s the difference between a xib and a storyboard?
> Both are used in Xcode to layout screens (view controllers). A xib defines a single View or View Controller screen, while a storyboard shows many view controllers and also shows the relationship between them.

12. List out what the different control statements used used in Swift, return is one of them.
> Continue, Break, Fallthrough and Return. However, while it’s important to know these control statements, what would really impress an interviewer is being able to have a dialogue around how each of you uses these controls, which you use most often, etc.

13. What is Operator Overloading ? 
> Operator overloading allows us to change how existing operators behave with types that both already exist.

14. What is ABI ? 	
> ABIs are important when it comes to applications that use external libraries. If a program is built to use a particular library and that library is later updated, you don’t want to have to re-compile that application (and from the end-user’s standpoint, you may not have the source). If the updated library uses the same ABI, then your program will not need to change.

15. KVC — KVO, what do they mean?
> KVC adds stands for Key-Value Coding. It’s a mechanism by which an object’s properties can be accessed using string’s at runtime rather than having to statically know the property names at development time.
> 
> KVO stands for Key-Value Observing and allows a controller or class to observe changes to a property value. In KVO, an object can ask to be notified of any changes to a specific property, whenever that property changes value, the observer is automatically notified.

16. What is difference between BDD and TDD ?	
> The main difference between BDD and TDD is the fact that BDD test cases can be read by non-engineers, which can be very useful in teams.
