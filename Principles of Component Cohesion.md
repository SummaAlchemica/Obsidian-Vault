https://blog.avenuecode.com/principles-of-package-and-component-design#:~:text=The%20Common%20Reuse%20Principle%20(CRP)&text=If%20you%20reuse%20one%20of,are%20seldom%20reused%20in%20isolation.

#Computer

[[SOLID]] principles are quite well known nowadays, but do you know their cousin, the Principles for Package and Component Design? Okay, maybe it's not the catchiest name, but that's what [Robert C. Martin](https://blog.cleancoder.com/) named them in his book entitled _[Agile Software Development, Principles, Patterns, and Practices](https://www.goodreads.com/book/show/84985.Agile_Software_Development_Principles_Patterns_and_Practices)_. 

In this book, Uncle Bob tried to cover everything he knew at the time about [[Agile]] software development, and this is where SOLID principles came from. Many of the chapters are just reviews, like the one about UML, but the chapter about Principles for Package and Component Design is something I've never seen elsewhere.

These principles are like a version of SOLID principles with a granular focus, as the name implies, and are quite helpful in keeping software components well defined.

They are divided into two categories:

-   **Principles of Component Cohesion**, which focus on the granularity of components and help the developer partition classes into components, and
-   **Principles of Component Coupling**, which focus on the stability and relationships between the components.

##### Principles of Component Cohesion

In the first group, **Principles of Component Cohesion**, you can find 3 principles:

**The Reuse/Release Equivalence Principle (REP)**

_The granular of reuse is the granular of release._

> REP states that the granule of reuse, a component, can be no smaller than the granule of release. Anything that we reuse must also be released and tracked. It is not realistic for a developer to simply write a class and then claim that it is reusable. Reusability comes only after a tracking system is in place and offers the guarantees of notification, safety, and support that the potential reusers will need. REP gives us our first hint at how to partition our design into components. Since reusability must be based on components, reusable components must contain reusable classes. So, at least some components should comprise reusable sets of classes.  
>   
> Martin, Robert C. [_Agile Principles, Patterns, and Practices in C#_](https://www.goodreads.com/book/show/84983.Agile_Principles_Patterns_and_Practices_in_C_) . Pearson Education. Kindle Edition.

**The Common Reuse Principle (CRP)**

_The classes in a component are reused together. If you reuse one of the classes in a component, you reuse them all._

> This principle helps us to decide which classes should be placed into a component. CRP states that classes that tend to be reused together belong in the same component. Classes are seldom reused in isolation. Generally, reusable classes collaborate with other classes that are part of the reusable [[abstract]]ion. CRP states that these classes belong together in the same component. In such a component, we would expect to see classes that have lots of dependencies on each other. A simple example might be a container class and its associated iterators. These classes are reused together because they are tightly coupled. Thus, they ought to be in the same component.  
>   
> Martin, Robert C. [_Agile Principles, Patterns, and Practices in C#_](https://www.goodreads.com/book/show/84983.Agile_Principles_Patterns_and_Practices_in_C_) . Pearson Education. Kindle Edition.

**The Common Closure Principle (CCP)**

_The classes in a component should be closed together against the same kinds of changes. A change that affects a component affects all the classes in that component and no other components._

> This is the Single-Responsibility Principle (SRP) restated for components. Just as SRP says that a class should not contain multiple reasons to change, CCP says that a component should not have multiple reasons to change. In most applications, maintainability is more important that reusability. If the code in an application must change, you would prefer the changes to occur all in one component rather than being distributed through many components. If changes are focused into a single component, we need redeploy only the one changed component. Other components that don’t depend on the changed component do not need to be revalidated or redeployed.  
>   
> Martin, Robert C. [_Agile Principles, Patterns, and Practices in C#_](https://www.goodreads.com/book/show/84983.Agile_Principles_Patterns_and_Practices_in_C_) . Pearson Education. Kindle Edition.

##### Principles of Component Coupling

And for the second group, **Principles of Component Coupling**, we have another 3 principles.

**The Acyclic Dependencies Principle (ADP)**

_Allow no cycles in the component dependency graph._

> The dependency structure must always be monitored for cycles. When cycles occur, they must be broken somehow. Sometimes, this will mean creating a new component, making the dependency structure grow.  
>   
> Martin, Robert C. [_Agile Principles, Patterns, and Practices in C#_](https://www.goodreads.com/book/show/84983.Agile_Principles_Patterns_and_Practices_in_C_) . Pearson Education. Kindle Edition.

**The Stable-Dependency Principle (SDP)**

_Depend in the direction of stability._

> Designs cannot be completely static. Some volatility is necessary if the design is to be maintained. We accomplish this by conforming to CCP. Using this principle, we create components that are sensitive to certain kinds of changes. These components are designed to be volatile; we expect them to change. Any component that we expect to be volatile should not be depended on by a component that is difficult to change! Otherwise, the volatile component will also be difficult to change. It is the perversity of software that a module that you have designed to be easy to change can be made difficult to change by someone else simply hanging a dependency upon it. Not a line of source code in your module need change, and yet your module will suddenly be difficult to change. By conforming to SDP, we ensure that modules that are intended to be easy to change are not depended on by modules that are more difficult to change than they are.  
>   
> Martin, Robert C. [_Agile Principles, Patterns, and Practices in C#_](https://www.goodreads.com/book/show/84983.Agile_Principles_Patterns_and_Practices_in_C_) . Pearson Education. Kindle Edition.

**The Stable-[[Abstract]]ions Principle (SAP)**

_A component should be as [[abstract]] as it is stable._

> _This principle sets up a relationship between stability and abstractness. It says that a stable component should also be abstract so that its stability does not prevent it from being extended. On the other hand, it says that an instable component should be concrete, since its instability allows the concrete code within it to be easily changed. Thus, if a component is to be stable, it should also consist of abstract classes so that it can be extended. Stable components that are extensible  
>   
> Martin, Robert C. [Agile Principles, Patterns, and Practices in C#](https://www.goodreads.com/book/show/84983.Agile_Principles_Patterns_and_Practices_in_C_) . Pearson Education. Kindle Edition._

##### Conclusion

No matter what we call them, modules/components/packages are used far more today than they were at the time this book was written, and most of these principles are easily achievable when using [[package manager]]s, like _[[npm]]_, _[[maven]]_, _[[nuget]]_ and so on. Design your software components as if they will be released and versioned in a package manager, even when they won't be, and you will ensure that your components can evolve well.

To learn more about these patterns, read chapter 28 of the aforementioned book. The most recent revision, released in August 2013, can be found [here](https://www.goodreads.com/book/show/24814960-agile-software-development-principles-patterns-and-practices).