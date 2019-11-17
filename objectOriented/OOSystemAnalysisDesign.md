# What Is Object-Oriented Analysis and Design? 
 
#### Table of Contents
- [Object-Oriented Analysis](#Object-Oriented-Analysis)
- [Object-Oriented Design](#Object-Oriented-Design)
- [The Unified Modeling Language (UML)](#the-uml--the-unified-modeling-language)
    - [UML History](#UML-history)
- [The Unified Process (UP)](#the-up--the-unified-process)
    - [Difference between Unified Process model and Waterfall model](#difference-between-unified-process-model-and-waterfall-model)
    - [Unified Process Phases](#unified-process-phases)
        - [Inception](#inception)
        - [Elaboration](#elaboration)
- [System Behaviour](#system-behaviour)
    - [Use Cases](#use-cases)
    - [System Sequence Diagrams](#system-sequence-diagrams)
    - [Domain Models](#domain-models)    
        - [Domain Model: Conceptual Class](#domain-Model-Conceptual-Class)
            - [Specification or Description Conceptual Class](#Specification-or-Description-Conceptual-Class)
            - [Conceptual Class Hierarchy](#Conceptual-Class-Hierarchy)
        - [Domain Model: Associations](#Domain-Model-Associations)
        - [Domain Model: Attributes](#DomainModel-Attributes)
        - [Use Case Model: Operation Contracts](#Use-Case-Model-Operation-Contracts)
    - [Refining Domain Models](#refining-domain-models)


 
## Object-Oriented Analysis
During object-oriented analysis, there is an emphasis on finding and describing the objects—or concepts—in the problem domain.  
For example, in the case of the library information system, some of the concepts include Book, Library, and Patron. 
  
## Object-Oriented Design
During object-oriented design, there is an emphasis on defining software objects and how they collaborate to fulfill the requirements.   
For example, in the library system, a Book software object may have a title attribute and a getChapter method. 

Object-Oriented Analysis | Object-Oriented Design
------------------------ | ----------------------
find/describe objects/concepts | define software objects -> how they collaborate to fulfill requirement
defining/ describing domain concepts | visualizing domain concepts


## The UML :: The Unified Modeling Language 
A language for specifying, visualizing, constructing, and documenting the artifacts of software systems, business modeling and other non-software systems 
 
### UML History 
The UML was adopted as the standard diagramming notation for object-oriented modeling in 1997 by the OMG - Object Modelling Group.
 
## The UP :: The Unified Process
It combines commonly accepted best practices, such as an iterative lifecycle and risk-driven development, into a cohesive and well-documented description.  

### Difference between Unified Process model and Waterfall model
Unified Process model | Waterfall model
--------------------- | ---------------
An iterative process. | A sequential process with prescribed steps in which current phase is completed before going to the next phase
Develops the product in several stages based on feedback from the stockholders. | It does not develop the product in several stages based on feedback from the stockholders.
Because each Unified Process iteration produces an executable release, the customers get to realize benefits much earlier than Waterfall. | Benefits are realised at a later stage as compared to Unified Process.
An adaptable framework of software processes. | A prescriptive concrete process.
The disciplines (Analysis, Design, Coding, Testing etc) are done iteratively and concurrently. | The disciplines are generally done sequentially (e.g. Coding only starts once Requirements have been finalized and Design has been accepted).
Multi disciplinary phrases. e.g. In Inception, design and prototype coding are encouraged with requirements and analysis to reduce future risk and improve estimates. Still, construction phase may require further analysis.| The term phases (inception, elaboration, construction, transition) are dedicated to a single discipline or single deliverable.
promoted budgeting at a per-phase basis, e.g. the effort/cost for a phase would be known/iterated/improved as one of the deliverables of the preceding phase. | promoted the concept of a 'contractual' Software Requirement or Software Specification document, which defines the deliverables and basis for project budget or fixed price transaction.

 
### Unified Process Phases
1. **Inception**
    — A kind of feasibility phase, where just enough investigation is done to support a decision to continue or stop. Keywords: approximate vision, business case, scope, vague estimates. 
2. **Elaboration**
    — A phase which involves refined vision, iterative implementation of the core architecture, resolution/mitigation  of high risks, identification of most requirements and scope, more realistic estimates. 
3. **Construction**
    — iterative implementation of the remaining lower risk and easier elements, and preparation for deployment. 
4. **Transition**
    — beta tests, deployment.

#### Inception
The intent of inception is to 
- establish some initial common vision for the objectives of the project, 
- determine if it is feasible, and 
- decide if it is worth some serious investigation in elaboration. 

If it has been decided beforehand that the project will definitely be done, and it is clearly feasible (perhaps because the team has done projects like this before), then the inception phase will be especially brief. It may include the first requirements workshop, planning for the first iteration, and then quickly moving forward to elaboration. 

10-20% use cases should be written in detail to obtain some realistic insight into the scope of the problem.
 
##### Inception artifacts and issues addressed
Artifact | Comment
-------- | -------
Vision and Business Case | Describes the high-level goals and constraints, the business case, and provides an executive summary.
Use-Case Model | Describes the functional requirements, and related non-functional requirements.
Supplementary Specification | Describes other requirements.
Glossary | Key domain terminology.
Risk List & Risk Management Plan | Describes the business, technical, resource, schedule risks, and ideas for their mitigation or response.
Prototypes and proof-of-concepts | To clarify the vision, and validate technical ideas.
Iteration Plan | Describes what to do in the first elaboration iteration.
Phase Plan & Software Development Plan | Low-precision guess for elaboration phase duration and effort. Tools, people, education, and other resources.
Development Case | A description of the customized UP steps and artifacts for this project. In the UP, one always customizes it for the project.

#### Elaboration
Elaboration is the initial series of iterations during which:
- the majority of requirements are discovered and stabilized
- the major risks are mitigated or retired
- the core architectural elements are implemented and proven

##### Elaboration artifacts and issues addressed
Artifact | Comment
-------- | -------
Domain Model | This is a visualization of the domain concepts; it is similar to a static information model of the domain entities.
Design Model | This is the set of diagrams that describes the logical design. This includes software class diagrams, object interaction dia- grams, package diagrams, and so forth.
Software Architecture Document | A learning aid that summarizes the key architectural issues and their resolution in the design. It is a summary of the outstanding design ideas and their motivation in the system.
Data Model | This includes the database schemas, and the mapping strategies between object and non-object representations. 
Test Model | A description of what will be tested, and how.
Implementation Model | This is the actual implementation — the source code, executables, database, and so on.
Use-Case Storyboards, UI Prototypes | A description of the user interface, paths of navigation, usability models, and so forth.

## System Behaviour
**System behaviour** is a description of what a system does, without explaining how it does it.

Description includes:
- System Sequence Diagrams
- Use Cases
- System Contracts

### Use Cases
An **actor** is something with behaviour.

A **scenario** or **use case instance** is a specific sequence of actions and interactions between actors and the system under discussion.

A **use case** is a collection of related success and failure scenarios that describe actors using a system to support a goal. Use cases decribe how external actors interact with the software system we are interested in creating.

Types:
- brief: terse one paragraph summary - of the main success scenario.
- casual or informal
- fully dressed or formal, most elaborate.

#### Relating Use Cases
An organization mechanism to (ideally) 
 - improve communication and comprehension of the use cases, 
 - reduce duplication of text, and 
 - improve management of the use case documents.
 
##### Include Relationship
Include is used to extract use case fragments that are duplicated in multiple use cases. The included use case cannot stand alone and the original use case is not complete without the included one. This should be used sparingly and only in cases where the duplication is significant and exists by design (rather than by coincidence).

For example, the flow of events that occurs at the beginning of every ATM use case (when the user puts in their ATM card, enters their PIN, and is shown the main menu) would be a good candidate for an include.

When to use?

1. They are duplicated in other use cases.
2. A use case is very complex and long, and separating it into subunits aids comprehension.

##### Extend Relationship
Extend is used when a use case conditionally adds steps to another first class use case. The idea is to create an extending or addition use case, and within it, describe where and under what condition it extends the behavior of some base use case. 

For example, imagine "Withdraw Cash" is a use case of an ATM machine. "Access Fee" would extend Withdraw Cash and describe the conditional "extension point" that is instantiated when the ATM user doesn't bank at the ATM's owning institution. Notice that the basic "Withdraw Cash" use case stands on its own, without the extension.


### Use Case Model: System Sequence Diagrams
A system sequence diagram (SSD) shows, for a particular scenario of a use case, the events that external actors generate, their order, and inter-system events. All systems are treated as a black box; the emphasis of the diagram is events that cross the system boundary from actors to systems.
      
      An SSD should be done for the main success scenario of the use case, and frequent or complex alternative scenarios.
      
#### Relationship between SSD and Use Cases
A System Sequence Diagram shows system events for a scenario of a use case, therefore it is generated from inspection of a use case.


### Domain Models
**Domain models or Conceptual models or Analysis object models**
A **domain model** is a visual representation of conceptual classes or real-world objects in a domain of interest.

It is illustrated with a set of class diagrams in which no operations are defined. It may show:
- domain objects or conceptual classes
- associations between conceptual classes
- attributes of conceptual classes

#### Domain Model: Conceptual Class
A conceptual class may be considered in terms of its symbol, intension, and extension. It is an idea, thing, or object. 
 - Symbol—words or images representing a conceptual class.
 - Intension—the definition of a conceptual class.
 - Extension—the set of examples to which the conceptual class applies.

For example, consider the conceptual class for the event of a purchase transac- tion. I may choose to name it by the symbol Sale. The intension of a Sale may state that it "represents the event of a purchase transaction, and has a date and time." The extension of Sale is all the examples of sales; in other words, the set of all sales.
 
When creating a domain model, it is usually the symbol and intensional view of a conceptual class that are of most practical interest.

**Identification of Conceptual Classes**
1. Use a conceptual class category list.
2. Identify noun phrases.
3. Use of analysis patterns.

##### Specification or Description Conceptual Class
If someone asks, "How much do Object- Burgers cost?", no one can answer, because the memory of their price was attached to inventoried instances, which were deleted as they were sold.
 
**Cons of not using description classes:**

_{Consider for an ObjectChocolate in a class Shop information like description, price, itemID is stored for each class instance ObjectChocolate as many as such instances exist in the class or chocolates exist in the Shop. }_
1. The memory of crucial objects will get deleted which also contained the object's description. Hence, description information like price and item_source of the object will be inaccessible until the object is recreated.
2. The model contains duplicate data and hence is space-inefficient.

**Solution?**

Description conceptual class, _ProductSpecification_, which represents only the description of the Item or Product and not the item as a whole. _{ Here, ChocolateDescription }_

In a domain model, it is common to state that an XSpecification Describes an X as they are meant to be strongly related to one another.

Domains specially requiring specification conceptual classes : sales, product, manufacturing,  et cetera.

**When are ProductSpecification like description conceptual class required (or their advantages)?**

1. There needs to be a description about an item or service, independent of the current existence of any examples of those items or services.
2. Deleting instances of things they describe (for example, Item) results in a loss of information that needs to be maintained, due to the incorrect association of information with the deleted thing.
3. It reduces redundant or duplicated information.

##### Conceptual Class Hierarchy
All the members of a conceptual subclass set are members of their superclass set. A potential subclass should conform to these rules to be considered as correct conceptual class:
 - 100% Rule (definition conformance)
 - Is-a Rule (set membership conformance)

**Conceptual Subclass Definition Conformance or the 100% rule**
100% of the conceptual superclass's definition should be applicable to the sub- class. The subclass must conform to 100% of the superclass's:
 - attributes
 - associations

**Conceptual Subclass Set Conformance**
1. Statements about _Superclass_ apply to _Subclass_
2. **Is-a-Kind-of Rule**: A conceptual subclass should be a member of the set of the superclass. _Conceptual Subclass is a kind of Superclass_
3. **Is-a Rule**: All the members of a subclass set must be members of their superclass set. Informally, Subclass is a Superclass_
4. More tersely, _is-a-kind-of_ is called _is-a_.

**Create a conceptual subclass of a superclass when:**
1. The subclass has additional attributes of interest.
2. The subclass has additional associations of interest.
3. The subclass concept is operated on, handled, reacted to, or manipulated differently than the superclass or other subclasses, in ways that are of interest.
4. The subclass concept represents an animate thing (for example, animal, robot) that behaves differently than the Superclass or other Subclasses, in ways that are of interest.

**Create a conceptual superclass in a generalization relationship to subclasses when:**
1. The potential conceptual subclasses represent variations of a similar concept.
2. The subclasses will conform to the 100% and Is-a rules.
3. All subclasses have the same attribute which can be factored out and expressed in the superclass.
4. All subclasses have the same association which can be factored out and related to the superclass.

##### Generalize Relationship
**generalization-specialization class hierarchy**
Generalization is the activity of identifying commonality among concepts and defining superclass (general concept) and subclass (specialized concept) relationships. It is a way to construct taxonomic classifications among concepts which are then illustrated in class hierarchies.

For example, a _Vehicle_ is a generalized concept and a superclass of _Bus_, _Car_, and _Bicycle_, which are subclasses and specialized concepts of _Vehicle_. THerefore, _Bus_ is-a _Vehicle_ as well as _Bus_ is-a-kind-of _Vehicle_.

#### Domain Model: Associations
An **association** is a relationship between types (or more specifically, instances of those types) that indicates some meaningful and interesting connection.

An association is represented as a line between classes with an association name. The association is inherently bidirectional, meaning that from instances of either class, logical traversal to the other is possible.

**Role**: each end of an association. It may optionally have:
- name 
- multiplicity expression 
- navigability

**Criteria for Useful Associations:**
1. Associations for which knowledge of the relationship needs to be preserved for some duration ("need-to-know" associations).
2. It is more important to identify conceptual classes than to identify associations.
3.  Too many associations tend to confuse a domain model rather than illuminate it. Their discovery can be time-consuming, with marginal benefit.
4. Avoid showing redundant or derivable associations.

#### Domain Model: Attributes
An **attribute** is a logical data value of an object. 

Example: A objectReceipt or a Sale conceptual class need attributes as Price, Date and Time. This information is frequently a used by the management.

**Criteria for Useful Attributes:**
1. Attributes for which the requirements (for example, use cases) suggest or imply the need to remember information.
2. The attributes in a domain model should preferably be simple attributes or data types.
3. Very common attribute data types include: Boolean, Date, Number, String (Text), Time
4. Other common types include: Address, Color, Geometries (Point, Rectangle), Phone Number, Social Security Number, Universal Product Code (UPC), SKU, ZIP or postal codes, enumerated types

### Use Case Model: Operation Contracts
**Contracts** describe detailed system behavior in terms of state changes to objects in the Domain Model, after a system operation has executed.

**Creation of the contracts leads to:**

1. Identify system operations from the SSDs.
2. For system operations that are complex and perhaps subtle in their results, or which are not clear in the use case, construct a contract.
3. To describe the postconditions, use the following categories:
    - instance creation and deletion
    - attribute modification
    - associations formed and broken
4. Record new conceptual classes, attributes, or associations in the Domain Model if needed.
 
_Example for point 2:_

Consider an airline reservation system and the system operation _addNewReservation_. 
 - The complexity is very high regarding all the domain objects that must be changed, created, and associated. 
 - Writing these fine-grained details in the use case associated with this operation will make the use case extremely detailed.
 - In such situations were there is high complexity and detailed precision adds value, contracts are another requirements tool.
 
**Common mistakes in creating Contracts**: Forgetting to include the forming of associations. When new instances are created, it is very likely that associations to several objects need be established.

### Refining Domain Models

#### Aggregation
Aggregation is a kind of association used to model whole-part relationships between things. The whole is called the composite. This association exhibits a _Has-part_ relationship.

For instance, physical assemblies are organized in aggregation relationships, such as a Hand aggregates Fingers.

Aggregation is shown in the UML with a hollow or filled diamond symbol at the composite end of a whole-part association. 

Composite aggregation, or composition | Shared Aggregation
------------------------------------- | ------------------
Part is a member of only on composite object. | Part may be simultaneously in many composite objects.
There is an existence and disposition dependency of the part on the composite. | There is no such dependency of part on the aggregate.
Represented by Filled Diamond. | Represented by Hollow Diamond.
For example, a hand is in a composition relationship to a finger. | For example, Fingers would exist in Hand as well as Legs (if not called Toes).

**Consider showing aggregation when:**
1. The lifetime of the part is bound within the lifetime of the composite — there is a create-delete dependency of the part on the whole.
2. There is an obvious whole-part physical or logical assembly.
3. Some properties of the composite propagate to the parts, such as the location.
4. Operations applied to the composite propagate to the parts, such as destruction, movement, recording.

#### References:
[1] Applying UML and Patterns by Craig Larman
