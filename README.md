# Swift Questions Part 1 for IT4445

Q. What is the difference between "strong" and "weak"

A. A strong reference is implicit and tracks the reference using ARC, weak references are not counted to determine when an object should be deallocated

Q. Explain the "lazy" keyword

A. A variable declared as lazy isn't allocated unless it's used

Q. What are the benefits of guard

A. Guard helps keep code clean by reducing the nesting of multiple ifs

Q. What is the difference between non-escaping and escaping closures?

A. Escaping closures can be called after the function they're passed to returns, non-escaping closures are deallocated when their enclosing function returns

Q. What is ARC?

A. Automatic Reference Counting counts the uses of references to an object in memory and when that count reaches zero the object is deallocated

Q. How does memory management work in swift

A. ARC

Q. Explain force unwrapping

A. It will force an uptional to be unwrapped, either using the value inside or causing the program to crash due to a nil value

Q. What problems does delegation solve

A. Delegation allows for an event handler-like system using a class with various functions rather than registering specific methods for specific events

Q. What is the difference between a delegate and an NSNotification

A. delegation is used to send information to a single recipient (ie a tableview) notifications are used when there may be any number of recipients for the data

Q. How is an inout parameter different from a regular parameter

A. inout parameters are passed by reference rather than by value

Q. Explain View Controller lifecycle events order? What are the events and in what order do they occur?

A. ViewDidLoad (view object loaded into memory), ViewWillAppear (view is going to appear), ViewDidAppear (view is now visible to the user), ViewWillDisappear (view is going to disappear), ViewDidDisappear (view has disappeared and is no longer visible to the user)

Q. What is downcasting?

A. Downcasting is casting an object to a more specific type ie from UIViewController to a custom view controller class

Q. What is upcasting?

A. Upcasting is casting an object to a more generic type ie from UIViewController to UIResponder

Q. What is the nil coalescing operator and when do you use it?

A. nil coalescing provides an alternate value when assigning an optional to a variable. if the optional value is nil, it will use the alternative instead. This uses a double question mark (var x = optional ?? value)

Q. What is optional chaining and when do you use it

A. Optional chaining is used to call methods on an wrapped optional without explicitly unwrapping. If the optional contains a nil value the function will fail silently/return nil

Q. Explain subscripts

A. Subscripts are used to reference the index of an array

Q. What is DispatchGroup?

A. DispatchGroups are used to manage threads for parallel processing

Q. What is the difference between Any and AnyObject

A. AnyObject references class types, Any can reference a struct or class

Q. What is the difference between the filter and map functions

A. Filter will remove items from the collection, map modifies elements in the collection

Q. When do you use optional chaining vs if let or guard?

A. Use optional chaining when a nil value won't be the end of the world, use if/guard let when you need to explicitly handle nil values

Q. Describe the different ways to pass data in swift.

A. Data can be passed across view controllers by setting an optional variable in the prepareforsegue method. Data can be passed via a delegate/datasource method or via NSNotifications

Q. What is an app ID and a bundle ID

A. bundle id is unique across all apps registered with apple

Q. explain what a property observer is and how/when it is used

A. property observers allow you to perform functions when a variable will be set or retrieved, and should be used when logic will need to be performed when a variable is set or retrieved

Q. What is URLSession

A. URLSession manages the creation and processing of a request to a url, optionally passing data

Q. Explain the rethrows keyword

A. rethrows marks a function which will call a function that throws an exception

Q. Explain type inferences

A. The swift compiler can infer the type of a variable based on how it's being set, so the type doesn't have to be explicitly written

Q. Explain @objc inference

A. @objc marks where swift code will intermingle with objective-c code in legacy ios apis

Q. What is the mutating keyword

A. mutating marks a function in a struct that will mutate the object, as struct functions are not mutable by default

Q. What is the deifference between the stack and the heap?

A. Stacks have static memory allocation, heaps have dynamic allocation

Q. Explain tuples

A. Tuples contain multiple values withou explicitly defining a type

Q. What is the difference between the frame and the bounds?

A. bounds use coordinates relative to the view, frame is relative to the superview

Q. What is a raw value for an enum and give an example for how it can be used

A. raw values allow for an associated value with enumerated types. for example you could have your enum extend string to have a more user-friendly associated value for each enum case

Q. What is the difference between synchronous and asynchronous tasks

A. synchronous tasks will wait for execution to complete before continuing execution of the program. Async will run in the background and continue exectuion immediately

Q. What are the states of an iOS App

A. willfinishlaunching and didfinishlaunching are called while the app is starting up and when it's finished starting up respectively. didbecomeactive is called when the application comes back to the foreground. didenterbackground is called when the app is put in the background. those two functions also have related "will" methods for when those are going to happen

Q. What is a UIStackView and how is it used

A. stackviews let you position subviews in a defined subspace