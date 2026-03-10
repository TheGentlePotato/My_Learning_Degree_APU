
# Chapter 10 — System Analysis Part 2

---

## 1 Introduction to System Analysis Part 2

System Analysis Part 2 continues the system analysis stage by focusing on modeling and documenting system requirements. After analysts collect and analyze requirements in the previous stage, they must represent those requirements in structured models that describe how the proposed system will function.

System models help developers, analysts, and stakeholders understand system processes, data structures, and user interactions before the system is designed and implemented.

This stage therefore focuses on process modeling, data modeling, use case modeling, and requirement verification.

---

## 2 Requirement Modeling

Requirement modeling is the process of representing system requirements in a structured and visual format. Instead of relying only on written descriptions, analysts create diagrams and models that describe system processes, data structures, and interactions.

Requirement models help simplify complex systems and improve communication between stakeholders.

Benefits of requirement modeling include:

| Benefit | Explanation |
|---|---|
| Improved system understanding | Visual models simplify complex systems |
| Better communication | Stakeholders can discuss system behavior clearly |
| Reduced development errors | Models reveal missing or incorrect requirements |
| Support for system design | Designers use models as the foundation for design |

Requirement modeling transforms system requirements into structured representations that developers can follow.

---

## 3 Process Modeling

Process modeling describes how the system processes data and performs tasks. It shows how information flows through the system and how different processes transform data.

Process modeling helps analysts understand how business processes operate and how the proposed system will improve them.

Process models focus on:

• Data input  
• Data processing  
• Data output  
• Data storage

One of the most commonly used tools for process modeling is the Data Flow Diagram.

---

## 4 Data Flow Diagrams (DFD)

A Data Flow Diagram is a graphical tool used to represent how data moves through a system.

DFDs illustrate how data flows between processes, data stores, and external entities.

Components of a Data Flow Diagram include:

| Component | Description |
|---|---|
| Process | Activity that transforms data |
| Data flow | Movement of data between system components |
| Data store | Location where data is stored |
| External entity | External source or destination of data |

Example

Customer → Order Processing → Order Database → Shipping Department

DFDs help analysts understand system processes clearly.

---

## 5 Levels of Data Flow Diagrams

Data Flow Diagrams are developed in different levels to show system processes with increasing detail.

| Level | Description |
|---|---|
| Context diagram | Shows the entire system as a single process |
| Level 0 DFD | Shows major system processes |
| Level 1 DFD | Shows detailed sub processes |
| Level 2 DFD | Shows further breakdown of processes |

Using multiple levels allows analysts to represent complex systems gradually.

---

## 6 Process Description Tools

After creating process models, analysts often use process description tools to explain system logic in more detail.

Common process description tools include:

| Tool | Description |
|---|---|
| Structured English | Uses simple English statements to describe system processes |
| Decision Tables | Shows logical conditions and corresponding actions |
| Decision Trees | Graphical representation of decision making logic |

These tools help analysts clearly describe how system processes operate.

---

## 7 Data Modeling

Data modeling describes how data is structured and organized within the system. It focuses on identifying data entities, attributes, and relationships.

Data modeling helps analysts understand how information is stored and accessed.

The most common tool used for data modeling is the Entity Relationship Diagram.

---

## 8 Entity Relationship Diagrams (ERD)

An Entity Relationship Diagram represents the structure of data used in a system.

ERDs show entities, attributes, and relationships between entities.

| Component | Description |
|---|---|
| Entity | Object or concept represented in the system |
| Attribute | Property that describes an entity |
| Relationship | Association between entities |

Example

Entity: Student  
Attributes: Student ID, Name, Course

Relationship  
Student enrolls in Course

ERDs help developers design the system database structure.

---

## 9 Use Case Modeling

Use case modeling describes how users interact with the system.

Use cases identify system functions from the user's perspective.

A use case diagram usually includes:

| Component | Description |
|---|---|
| Actor | Person or system interacting with the system |
| Use case | Function performed by the system |
| System boundary | Defines the scope of the system |

Example

Actor: Student  
Use case: Register for course

Use case diagrams help analysts understand system functionality from the user's perspective.

---

## 10 Logical System Design

Logical system design describes how the system will operate without specifying the physical implementation details.

Logical design focuses on system processes, data structures, and user interactions.

Logical system design answers questions such as:

• What processes the system performs  
• What data the system stores  
• How data flows through the system

Logical design forms the foundation for physical system design.

---

## 11 Prototyping in System Analysis

Prototyping involves building an early model of the proposed system to demonstrate system functionality.

Users can interact with the prototype and provide feedback.

Advantages of prototyping include:

| Advantage | Explanation |
|---|---|
| Early user feedback | Users can evaluate system features |
| Improved requirement accuracy | Developers better understand user needs |
| Reduced development risk | Problems are discovered early |

Prototypes help analysts refine system requirements.

---

## 12 User Involvement in System Analysis

User participation is important during system analysis because users understand how the current system operates.

Users contribute by:

• Explaining business processes  
• Identifying system problems  
• Reviewing system models  
• Evaluating prototypes

User involvement ensures that the final system meets organizational needs.

---

## 13 Requirement Verification

Requirement verification ensures that the identified system requirements are correct and complete.

Verification activities include:

• Reviewing requirement documents  
• Confirming requirements with users  
• Checking requirement consistency  
• Evaluating system prototypes

Requirement verification prevents errors from continuing into later development stages.

---

## 14 Importance of System Modeling

System modeling is essential for successful system development.

Benefits include:

| Benefit | Explanation |
|---|---|
| Improved understanding | Visual models simplify complex systems |
| Better communication | Stakeholders understand system behavior |
| Reduced development errors | Problems are identified early |
| Support system design | Models guide system architecture |

System modeling helps developers transform system requirements into system design.

---

## Chapter Summary

System Analysis Part 2 focuses on modeling and organizing system requirements. Analysts use requirement modeling techniques to represent system behavior and structure in visual form. Process modeling describes how data flows through the system using tools such as Data Flow Diagrams, while data modeling describes how information is structured using Entity Relationship Diagrams. Analysts also use use case diagrams to represent user interactions with the system. Process description tools such as Structured English, decision tables, and decision trees are used to describe system logic. Prototyping and user involvement help analysts refine and validate system requirements. Proper system modeling ensures that system requirements are clearly understood before the system design stage begins.
