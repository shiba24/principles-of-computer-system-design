# Principles of Computer System Design: An Introduction

This is outline and notes of essential parts in this [book](https://www.amazon.com/Principles-Computer-System-Design-Introduction/dp/0123749573). [part 2(online)](https://ocw.mit.edu/resources/res-6-004-principles-of-computer-system-design-an-introduction-spring-2009/online-textbook/)

---

- [Principles of Computer System Design: An Introduction](#principles-of-computer-system-design--an-introduction)
- [1. Systems](#1-systems)
  * [1.1 Systems and Complexity](#11-systems-and-complexity)
    + [1.1.1 Common problems of systems in many fields](#111-common-problems-of-systems-in-many-fields)
    + [1.1.2 Systems, Components, Interfaces, and Environments](#112-systems--components--interfaces--and-environments)
    + [1.1.3 Complexity](#113-complexity)
  * [1.2 Sources of Complexity](#12-sources-of-complexity)
    + [1.2.1 Cascading and interacting requirements](#121-cascading-and-interacting-requirements)
    + [1.2.2 Maintaining High Utilization](#122-maintaining-high-utilization)
  * [1.3 Coping with Complexity I](#13-coping-with-complexity-i)
    + [1.3.1 Modularity](#131-modularity)
    + [1.3.2 Abstraction](#132-abstraction)
    + [1.3.3 Layering](#133-layering)
    + [1.3.4 Hierarchy](#134-hierarchy)
    + [1.3.5 Putting it back together: Names make connections](#135-putting-it-back-together--names-make-connections)
  * [1.4 Computer systems are the same but different](#14-computer-systems-are-the-same-but-different)
    + [1.4.1 Computer systems have no nearby bounds on composition](#141-computer-systems-have-no-nearby-bounds-on-composition)
    + [1.4.2 d(technology)/dt is unprecedented](#142-d-technology--dt-is-unprecedented)
  * [1.5 Coping with complexity II](#15-coping-with-complexity-ii)
    + [1.5.1 Why modularity, abstraction, layering, and hierarchy aren't enough](#151-why-modularity--abstraction--layering--and-hierarchy-aren-t-enough)
    + [1.5.2 Iteration](#152-iteration)
    + [1.5.3 Keep it simple](#153-keep-it-simple)
  * [Exercises 1](#exercises-1)
- [2. Elements of Computer System Organization](#2-elements-of-computer-system-organization)
  * [2.1 The three fundamental abstractions](#21-the-three-fundamental-abstractions)
    + [2.1.1 Memory](#211-memory)
      - [2.1.1.1 Read/Write coherence and atomicity](#2111-read-write-coherence-and-atomicity)
      - [2.1.1.2 memory latency](#2112-memory-latency)
      - [2.1.1.3 Memory names and addresses](#2113-memory-names-and-addresses)
      - [2.1.1.4 Exploiting the memory abstraction: RAID](#2114-exploiting-the-memory-abstraction--raid)
    + [2.1.2 Interpreters](#212-interpreters)
      - [2.1.2.1 Processors](#2121-processors)
      - [2.1.2.2 Interpreter layers](#2122-interpreter-layers)
    + [2.1.3 Communication links](#213-communication-links)
  * [2.2 Naming in computer systems](#22-naming-in-computer-systems)
    + [2.1.1 The naming model](#211-the-naming-model)
    + [2.2.2 Default and explicit content references](#222-default-and-explicit-content-references)
    + [2.2.3 Path names, naming networks, and recursive name resolution](#223-path-names--naming-networks--and-recursive-name-resolution)
    + [2.2.4 Multiple lookup: searching through layered contexts](#224-multiple-lookup--searching-through-layered-contexts)
    + [2.2.5 Comparing names](#225-comparing-names)
    + [2.2.6 Name discovery](#226-name-discovery)
  * [2.3 Organizing computer systems with names and layers](#23-organizing-computer-systems-with-names-and-layers)

---

# 1. Systems

## 1.1 Systems and Complexity

### 1.1.1 Common problems of systems in many fields

- Emergent properties
- Propagation of effects
- Incommensurate scaling
- Trade-offs

### 1.1.2 Systems, Components, Interfaces, and Environments

- A system is a set on interconnected components that has an expected behavior observed at the interface with its environment.

### 1.1.3 Complexity

- Large number of components
- Large number of interconnections
- Many irregularities
- A long description
- A team of designers, implementers, or maintainers

## 1.2 Sources of Complexity

### 1.2.1 Cascading and interacting requirements

- **Principle of escalating complexity**

*Adding a requirement increases complexity out of proportion*

- **Avoid excessive generality**

*If it is good for everything, it is good for nothing.*

### 1.2.2 Maintaining High Utilization

- **The law of diminishing returns**

*The more one improves some measure of goodness, the more effort the next improvement will require.*

## 1.3 Coping with Complexity I

### 1.3.1 Modularity

- **The unyielding foundations rule**

*It is easier to change a module than to change the modularity.*

### 1.3.2 Abstraction

- **The robustness principle**

*Be tolerant of inputs and strict on outputs.*

- **The safety margin principle**

*Keep track of the distance to the cliff, or you may fall iver the edge.*

### 1.3.3 Layering

### 1.3.4 Hierarchy

### 1.3.5 Putting it back together: Names make connections

- **Decouple modules with indirection**

*Indirection supports replaceability.*

## 1.4 Computer systems are the same but different

### 1.4.1 Computer systems have no nearby bounds on composition

### 1.4.2 d(technology)/dt is unprecedented

- **The incommensurate scaling rule**

*Changing any system parameter by a factor of 10 usually requires a new design.

## 1.5 Coping with complexity II

### 1.5.1 Why modularity, abstraction, layering, and hierarchy aren't enough

### 1.5.2 Iteration

- **Design for iteration**

4. And another item.

*You won't get it right the first time, so make it easy to change.*

   Take small steps  
   Don't rush  
   Plan for feedback  
   Study failures

- **Keep digging**

*Complex systems fail for complex reasons.*

   Continue looking for other contributing or more basic causes.  
   Don't ignore unexplained behavior.

### 1.5.3 Keep it simple

- **Adopt sweeping simplifications**

*So you can see what you are doing.*

## Exercises 1

 1. B
 2. E
 3. False
 4. C
 5. 1,600 lines, 16 x 15 / 2 = 120, 2,000 lines, 4 x 3 / 2 x 5 = 30, Good - because interconnections are reduced.


# 2. Elements of Computer System Organization

Three well-defined classes: the memory, the interpreter, and the communication link.

A primary method by which the abstract components of a computer system interact is *reference*, the usual way for one component to connect to another by *name*.

## 2.1 The three fundamental abstractions

### 2.1.1 Memory

- Memory (storage) is the system component that remembers data values for use in computation,

- `WRITE(name, value)`, `value <- READ(name)`

- A *volatile* memory is one whose mechanism of retaining information consumes energy. By connecting a volatile memory to a battery or an uninterruptible power supply, it can be made *durable*, which means that it is designed to remember for at least some specified period, known as *durability*.

- A *non-volatile* memory retains its content without power supply. Non-volatile memory devices are subject to eventualdeterioration, known as *decay*.

- Hardware layer memory devices READ and WRITE contiguous arrays of *bits*, usually fixed in length, known by various terms such as *bytes* (usually 8 bits), *words* (a small integer number of bytes, typically 2, 4, or 8), *lines* (several words), and *blocks* (a number of bytes, in the thousands). Whatever size, they are called *cell*.

#### 2.1.1.1 Read/Write coherence and atomicity

- *read/write coherence*: the result of the READ of a named cell is always the same as the most recent WRITE to that cell.

   Performance enhancements  
   Replicated storage

- *before-or-after atomicity*: the result of every READ or WRITE is as if that READ or WRITE occurred either completely before or completely after any other READ or WRITE.

   Concurrency  
   Remote storage  
   Cell size incommensurate with value size  
   Replicated storage

#### 2.1.1.2 memory latency

- It takes time for a READ or WRITE to complete, known as *latency* or *access time*.

- *Random access memory* is one for which the latency for memory cells chosen at random is approximately the same as the latency for cells chosen in the pattern best suited for that memory device.

- Large-block READ and WRITE operations are sometimes relabeled GET and PUT.

#### 2.1.1.3 Memory names and addresses

- Conseutive integers for mapping geometric coordinates as names are called *addresses*, amd they form the *address space* of the memory device.

- A memory system that accepts unconstrained names is called an *associative memory*. Assiciativity layer is abstraction of *location-addressed memory* (physical layer).

- *cache* is sometimes implemented as an associative memory, either in software or hardware.

#### 2.1.1.4 Exploiting the memory abstraction: RAID

- RAID is an acronym for Redundant Array of Independent (Inexpensive) Disks.

- A RAID system consists of a set of disk drives and a controller configured with an electrical and programming interface that is identical to the interface of a single disk drive.

   Improved performance, by reading or writing disks concurrently  
   Improved durability, by writing information on more than one disk

### 2.1.2 Interpreters

- Interpreters are the active elements of a computer system; they perform the actions that constitute computations.

 1. An *instruction reference*, which tells the interpreter where to find its next instruction

 2. A *repertoire*, which defines the set of actions the interpreter is prepared to perform when it retrieves an instruction from the location named by the instruction reference.

 3. An *environment reference*, which tells the interpreter where to find its environment, the current state on which the interpreter should perform the action of the current instruction.

- Using the environment reference to find the current environment, the interpreter retrieves from that environment the program instruction indicated in the instruction reference. Again using the environment reference, the interpreter performs the action directed by the program instruction.

- Certain events, called *interrupts*, may catch the attention of the interpreter, causing it, rather than the program, to supply the next instruction.

- Multiple interpreters are usually *asynchronous*, running on separate, uncoordinated clocks.

#### 2.1.2.1 Processors

- The processor's instruction reference is a *program counter*, stored in a fast memory register inside the processor.

- The repertoire of our general-purpose processor includes instructions for expressing computations such as adding two numbers `ADD`, subtracting one number from another `SUB`, comparing two numbers `CMP`, and changing the program counter to the address of another instruction `JMP`.

- `LOAD` = `READ` a value from a named memory cell into a register into a register of the processor.

- `STORE` = `WRITE` the value from a register into a named memory cell. These get two arguments, the name of a memory cell and the name of a processor register.

#### 2.1.2.2 Interpreter layers

- Interpreters are nearly always ofganized in layers.

- The lowest layer is usually a hardware engine that has a fairly primitive repertoire of instructionsm and successive layers provide an increasingly rich or specialized repertoire.

- A full- brown application system may involve four or five distinct layers of interpretation.

### 2.1.3 Communication links

- A communication link provides a way for information to move between physically separated components.

- `SEND(link_name, outgoing_message_buffer)`, `RECEIVE(link_name, incoming_message_buffer)`

- The lawest layer of a system has received a message, higher layers may acquire the message by calling a `RECEIVE` interface of the lower layer, or the lower layer may "upcall" to the higher layer, in which case the interface might be b etter characterized as `DELIVER(incoming_message)`.

- The *link_name* arguments of `SEND` and `RECEIVE` identify one of possibly several available communication links attached to the system.

- Communication links involve more than simple copying an array of bits from one memory to another memory over a wire using `READ` and `WRITE`.

- Many complications, such as unpredictable time to complete, threatening integrity of the data transfer, asynchronous operation, message not delivered.

- Three-layer model that organizes communication links into systems called *networks*.

## 2.2 Naming in computer systems

- Computer systems use names in many ways in their construction, configuration, and operation.

- The computer system manipulates *objects*.

- There are two ways to arrange for one object to use another as a component:

   create a copy of the component object and include the copy in the using object (use by *value*)  
   choose a name for the component object and include just that name in the using object (use by *reference*). The component object is said to *export* the name.

- When passing arguments to proceduresm use by value enhances modularity. But it does not easily permit two or more objects to share a component object whose value changes.

- One purpose of names is to allow use by reference and thus simplify the sharing of changeable objects.

- A second purpose is to allow a system designer to defer to a later time an important decision: to which object should this name refer.

- Decoupling one object from another by using a name as an intermediary is know as *indirection*.

- Deciding on the correspondence between a name and an object is an example of *binding*.

### 2.1.1 The naming model

- *Naming scheme* has three components: *name space* comprises an alphabet of symbols together with syntax rules that specify which names are acceptable. *name-mapping algorithm* associates some names of the name space with some values in a *universe of values*.

- A name-to-value mapping is an example of *binding*.

- The name-mapping algorithm *resolves* the name, discovering and returning the associated value.

- The name-mapping algorithm is usually controlled by an additional parameter, known as a *context*.

- value <- `RESOLVE(name, context)`

- status <- `BIND(name, value, context)`

- status <- `UNBIND(name, context)`

- list <- `ENUMERATE(context)`

- result <- `COMPARE(name1, name2)`

- In practice, one encounters three frequently used name-mapping algorithms:

   Table lookup  
   Recursive lookup  
   Multiple lookup

### 2.2.2 Default and explicit content references

- There are two ways to come up with a context with which to resolve the names found in an object: *default context reference*, supplied by the resolver, and *explicit context reference*, supplied by the object.

### 2.2.3 Path names, naming networks, and recursive name resolution

- In *recursive name resolution*, a path name can be thought of as a name that explicitly includes a reference to the context in which it should be resolved.

- Path names can also be thought of as identifying objects that are organized in what is called a *naming network*. In a naming network, contexts are treated as objects, and any context may contain a name-to-object binding for any other object, including another context.

- Multiple names for the same object are known as *synonyms* or *aliases*.

- The file system of a computer operating system is usually organized as a naming network, with directories acting as contexts.

- Many systems have many different cross-hierarchy links, called *symbolic link*, *soft link*, *alias*, and *shortcut*.

### 2.2.4 Multiple lookup: searching through layered contexts

- *The idea of *multiple lookup* is to abandon the notion of a single, default context and instead resolve the name by systematically trying several different contexts.

- Since a name may be bound in more than one context, multiple lookup can produce multiple resolutions, so some scheme is needed to decide which resolution to use. A common such scheme is called the *search path*, which is a specific list of contexts to be tried, in order. (like `$PATH`) Provides *user-dependent binding*.

- In a set of layered contexts, the *scope* of a name is the range og layers in which the name is bound to the same object.

- A name that is bound only in the outermost layer is known as a *global name*.

- A *path name* is a name that carries its own explicit context, and a *search path* is a context that consists of a list of contexts.

### 2.2.5 Comparing names

- result <- `COMPARE(name1, name2)` is for:

   Are the two names the same?  
   Are the two names bound to the same value?  
   If the value(s) are actually the indentifiers of storage containers, such as memory cells or disk sectors, are the contents of the storage containers the same?

- The second includes recursive search to the lower layer. The third is about understanding what it means to be the "same".

- In practice, systems and programming languages typically provide several `COMPARE` operations with different semantics.

### 2.2.6 Name discovery

- The *name discovery protocol* informs an object's prospective user of the name that the object exports: the exporter *advertises* the existence of the name, while the user *searches* for an appropriate advertisement.

- Any methods of name discovery may require first discovering some other name by any methods, but the recursion must terminate somewhere.

## 2.3 Organizing computer systems with names and layers

- The typical organization of a computer system has three layers. The bottom layer consists of hardware components, such as processors, memories, and communication links. The middle layer consists of a collection of software modules, called the *operating system*, that abstract these hardware resources into a convenient *application programing interface* (API). The top layer consists of software that implements application-specific functikons, such as a word processor or Web browser.

- The exact division of labor between the hardware layer and the software layers is an engineering trade-off and debate between hardware and software designers. In principle, every software module can be implemented in hardware.

- The operating system layer usually exhibits a phenomenon that we might call *layer bypass*, some features of the hardware layer pass through the OS layer.

### 2.3.1 A hardware layer: The bus



pp80

 