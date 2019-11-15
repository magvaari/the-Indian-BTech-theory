# GRASP: Patterns of General Principles in Assigning Responsibilities

GRASP is an acronym that stands for General Responsibility Assignment Software Patterns. The name was chosen to suggest the importance of grasp ing these principles to successfully design object-oriented software. GRASP patterns describe the fundamental principles of object design and responsibility assignment, expressed as patterns.

The following sections present the first five GRASP patterns:
1. Information Expert
2. Creator
3. High Cohesion
4. Low Coupling
5. Controller

## Information Expert or Expert
Assign a responsibility to the information expertóthe class that has the infor- mation necessary to fulfill the responsibility.
 
During object design, when the interactions between objects are defined, we make choices about the assignment of responsibilities to software classes. Done well, systems tend to be easier to understand, maintain, and extend, and there is more opportunity to reuse components in future applications.


Information Expert (also Expert or the Expert Principle) is a principle used to determine where to delegate responsibilities. These responsibilities include methods, computed fields, and so on.
Using the principle of Information Expert, a general approach to assigning responsibilities is to look at a given responsibility, determine the information needed to fulfill it, and then determine where that information is stored.
Information Expert will lead to placing the responsibility on the class with the most information required to fulfil it.

## Creator
Which class is responsible for creating objects is a fundamental property of the
relationship between objects of particular classes.
In general, a class B should be responsible for creating instances of class A if one, or more apply:
 - Instances of B contain or compositely aggregate instances of A
 - Instances of B record instances of A
 - Instances of B closely use instances of A
 - Instances of B have the initializing information for instances of A and pass it on creation.

## High Cohesion
High Cohesion is an evaluative pattern that attempts to keep objects appropriately focused, manageable and understandable. High cohesion is generally used in support of Low Coupling. High cohesion means that the responsibilities of a given element are strongly related and highly focused. Breaking programs into classes and subsystems is an example of activities that increase the cohesive properties of a system. Alternatively, low cohesion is a situation in which a given element has too many unrelated responsibilities. Elements with low cohesion often suffer from being hard to comprehend, hard to reuse, hard to maintain and averse to change.

## Low Coupling
Low Coupling is an evaluative pattern, which dictates how to assign responsibilities to support:
 - lower dependency between the classes,
 - change in one class having lower impact on other classes,
 - Higher reuse potential.

## Controller
The **Controller** pattern assigns the responsibility of dealing with system events to a non-UI class that represents the overall system or a use case scenario. A Controller object is a non-user interface object responsible for receiving or handling a system event.

A use case controller should be used to deal with all system events of a use case, and may be used for more than one use case

A controller should delegate to other objects the work that needs to be done; it coordinates or controls the activity. It does not do much work itself.


#### References:
[1] Applying UML and Patterns by Craig Larman