# Principles of Computer System Design: An Introduction

This is outline and notes of essential parts in this [book](https://www.amazon.com/Principles-Computer-System-Design-Introduction/dp/0123749573). [part 2(online)](https://ocw.mit.edu/resources/res-6-004-principles-of-computer-system-design-an-introduction-spring-2009/online-textbook/)

---

# Table of contents

- [Principles of Computer System Design: An Introduction](#principles-of-computer-system-design--an-introduction)
- [Table of contents](#table-of-contents)
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

*You won't get it right the first time, so make it easy to change.*
⋅⋅⋅Take small steps
⋅⋅⋅Don't rush
⋅⋅⋅Plan for feedback
⋅⋅⋅Study failures

- **Keep digging**

*Complex systems fail for complex reasons.*
⋅⋅⋅Continue looking for other contributing or more basic causes.
⋅⋅⋅Don't ignore unexplained behavior.

### 1.5.3 Keep it simple

- **Adopt sweeping simplifications**

*So you can see what you are doing.*

## Exercises 1

 1. B
 2. E
 3. False
 4. C
 5. 1,600 lines, 16 x 15 / 2 = 120, 2,000 lines, 4 x 3 / 2 x 5 = 30, Good - because interconnections are reduced.



