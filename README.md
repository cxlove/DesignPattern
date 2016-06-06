# DesignPattern
The example code from head first design patterns for practicing 

**Reference: [Head First Design Patterns](http://www.amazon.com/Head-First-Design-Patterns-Freeman/dp/0596007124)**

**If there is any content related to copyright, please concat author to declare it or remove it. Thanks.**

## Singleton Pattern

Your ticket to creating one-of-a-object, for which there is only one instance.

We're taking a class and letting it manage a single instance of itself. We're also provide a global access point to get the instance.

Create a static member instance in class which has a private constructor and using a static function to get the single instance. At the same time, pay attention to the problem of synchronization.

Java Code: [Issue #1](https://github.com/cxlove/DesignPattern/issues/1) 

c++ Code: [Issue #2](https://github.com/cxlove/DesignPattern/issues/2) 

## Strategy Pattern

Define a family of algorithms, encapsulates each one, and makes them interchangeable. Strategy lets the algorithm vary independently from clients that use it.

Java Code & Design Step: [Issue #3](https://github.com/cxlove/DesignPattern/issues/3) 

c++ Code: [Issue #4](https://github.com/cxlove/DesignPattern/issues/4) 

## Observer Pattern

It defines a one-to-many dependency between objects so that when one object changes state, all of its dependents are notified and updated automatically.

I guess called Subscription Pattern will be more appropriate. We have a Subject which have some data or some information, just like a journal or website. Some people or Observer want to have a subscription. The Subject need to notifiy all of the Observer when some changes happend or just regularly. Meanwhile, the Subject need to support register and unregister for Observer. So, it's Observer Pattern. It's a one-to-many dependency between Subject and Observers.

In our example, the weather station or weather data is the Subject. So it implements from a Subject interface which support register & unregister & notify. And some different DisplayElements is the Observer. It implements from a DisplayElement which support display and a Observer which support observed multiple Subjects.  

The DisplayElement don't need to know how Subject implemented, because it just use some interfaces to interact with Subject. And Subject also don't need to know what is the difference for different types of Observer, beacuse it also just use some same interfaces to interfact with all of Observers. It's convenient to add a new DisplayElement or Observer.

Java Code & Design Step: [Issue #5](https://github.com/cxlove/DesignPattern/issues/5) 

## Decorator Pattern

The Decorator Pattern attaches additional responsibilities to an object dynamically. Decorators provide a flexible alternative to subclassing for extending functionality.

We have some componment. Some of them, I called Base Componment which are Concrete Componments. Others are decorations. In our example, base Coffe are Concrete Componments, such as Espresso and DarkRoast. And we have some options, such as Milk, Moca and Soy, which are decorations.

If we build each coffe with different options as a new Class, it will be a large scale. And also we cannot add all of decorations in coffe class for options, if there is a new decorations, we need to change the code, even the whole interfaces. 

Actually, in decorations pattern, we build a Componment class, Concrete Componment and Decorators both inherit it. Seems like a Wrapping operation one by one for decorations, and the Concrete Componment is innermost.  

<del>By the way, I cann't find its benefit compared to Combination between Concrete Componment and Decorators. I can add a ArrayList for decorations in Concrete Componment.</del> 

Java Code: [Issue #8](https://github.com/cxlove/DesignPattern/issues/8) 

c++ Code: [Issue #9](https://github.com/cxlove/DesignPattern/issues/9) 
