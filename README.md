# Principles of Computer System Design: An Introduction

This is outline and notes of essential parts in this [book](https://www.amazon.com/Principles-Computer-System-Design-Introduction/dp/0123749573).

- [part 2(online)](https://ocw.mit.edu/resources/res-6-004-principles-of-computer-system-design-an-introduction-spring-2009/online-textbook/)

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


