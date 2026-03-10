# Chapter 2 — Structured Methodologies

---

## 1 Introduction to Structured Methodologies

Structured methodologies are traditional approaches used to develop information systems in a **step by step and highly organized manner**.

They emphasize:

• Detailed planning  
• Clear system requirements before development  
• Sequential development stages  
• Extensive documentation

Structured methodologies are often used in projects where the system requirements are **clear and stable**.

These methodologies became popular before Agile development methods.

---

## 2 Characteristics of Structured Methodologies

Structured methodologies follow several important principles.

| Characteristic | Explanation |
|-----|-----|
| Sequential development | Development follows a fixed order of stages |
| Heavy documentation | Each stage produces detailed reports |
| Fixed requirements | Requirements must be clearly defined before development |
| Strict process control | Each phase must be completed before moving to the next phase |
| Formal management | Structured meetings and approvals are required |

Example

A government system project often uses structured methodologies because requirements must be clearly documented and approved before development.

---

## 3 Traditional Development Flow

Structured methodologies usually follow a **linear process**.

Typical development sequence:

1 Planning  
2 Analysis  
3 Design  
4 Implementation  
5 Testing  
6 Deployment  
7 Maintenance

Each phase must be completed before the next phase begins.

This approach reduces uncertainty but makes changes difficult later.

---

## 4 Waterfall Model

The **Waterfall Model** is one of the earliest and most widely known structured methodologies.

The model is called waterfall because development flows **downward through stages**, similar to water flowing over a waterfall.

Each phase must be completed before the next phase begins.

### Waterfall Stages

| Stage | Purpose |
|-----|-----|
| Requirements | Define system requirements |
| System Design | Create system architecture |
| Implementation | Develop software |
| Testing | Verify system functionality |
| Deployment | Deliver system to users |
| Maintenance | Support and update system |

Flow example

Requirements → Design → Implementation → Testing → Deployment → Maintenance

---

## 5 Why the Waterfall Model is Called "Waterfall"

The name comes from the visual structure of the model.

Each development phase flows downward into the next phase without returning to the previous phase.

Key idea

Once a phase is completed, the development team moves forward and rarely revisits earlier stages.

This is similar to water flowing downward in a waterfall.

---

## 6 Advantages of the Waterfall Model

| Advantage | Explanation |
|-----|-----|
| Clear structure | Development stages are clearly defined |
| Easy project management | Progress is easy to track |
| Good documentation | Every phase produces detailed documentation |
| Suitable for stable projects | Works well when requirements are fixed |

Example

Government system development  
Banking systems with strict regulations  
Large enterprise systems

---

## 7 Disadvantages of the Waterfall Model

| Disadvantage | Explanation |
|-----|-----|
| Difficult to change requirements | Changes require returning to earlier stages |
| Late error detection | Problems may only appear during testing |
| Limited customer involvement | Customers mainly involved at beginning |
| Slow delivery | Working software appears late in the project |

Example problem

If customers realize the system design is wrong during testing, developers may need to redesign the system, causing delays and increased costs.

---

## 8 V Model

The **V Model** is an extension of the Waterfall Model.

The name comes from the V shaped structure of the development process.

The left side of the V represents development phases.  
The right side represents testing phases.

Each development stage has a corresponding testing stage.

---

### V Model Structure

| Development Phase | Corresponding Testing Phase |
|-----|-----|
| Requirements | Acceptance Testing |
| System Design | System Testing |
| Architecture Design | Integration Testing |
| Module Design | Unit Testing |

Explanation

Every design stage has a testing activity planned early.

This improves software quality and allows earlier defect detection.

---

## 9 Advantages of the V Model

| Advantage | Explanation |
|-----|-----|
| Early testing planning | Testing begins during design stage |
| Higher software quality | Errors can be detected earlier |
| Clear relationship between development and testing | Each development phase links to testing phase |

Example

Safety critical systems such as

Medical systems  
Airplane control systems  
Defense systems

These systems require strict testing.

---

## 10 Disadvantages of the V Model

| Disadvantage | Explanation |
|-----|-----|
| Rigid development structure | Difficult to modify requirements |
| High documentation requirement | Large amount of documentation required |
| Limited flexibility | Changes become expensive |
| Late system prototype | Users cannot see system early |

---

## 11 SSADM (Structured Systems Analysis and Design Methodology)

SSADM is a structured methodology developed in the United Kingdom for large government projects.

The goal of SSADM is to ensure that information systems are designed based on **business needs and structured analysis**.

SSADM focuses heavily on documentation and detailed analysis.

---

### Key Features of SSADM

| Feature | Explanation |
|-----|-----|
| Structured analysis | Uses diagrams and models to describe system |
| Data driven approach | Focus on data and system processes |
| Extensive documentation | Produces many reports |
| Formal methodology | Strict development stages |

---

## 12 Tools Used in Structured Methodologies

Structured methodologies use several modeling tools.

### Data Flow Diagram (DFD)

A diagram used to show how data moves through a system.

Components

| Component | Description |
|-----|-----|
| Process | Activity that transforms data |
| Data store | Storage location |
| Data flow | Movement of data |
| External entity | External system or user |

Example

Customer order system

Customer → Order request → Processing system → Order database

---

### Entity Relationship Diagram (ERD)

ERD describes relationships between data entities.

Example

| Entity | Relationship |
|-----|-----|
| Student | Enrolls in |
| Course | Contains students |

ERD helps designers create database structures.

---

### Structure Charts

Structure charts show relationships between program modules.

Example

Main program  
→ Input module  
→ Processing module  
→ Output module

This helps developers understand system architecture.

---

## 13 Comparison Between Waterfall and V Model

| Feature | Waterfall Model | V Model |
|-----|-----|-----|
| Development structure | Linear | V shaped |
| Testing | Done after development | Planned early |
| Flexibility | Low | Low |
| Error detection | Late | Earlier |
| Documentation | Heavy | Heavy |

---

## 14 Traditional vs Agile Methodologies

Structured methodologies represent **traditional development approaches**.

Agile methodologies represent **modern flexible approaches**.

| Feature | Structured Methodologies | Agile Methodologies |
|-----|-----|-----|
| Development style | Sequential | Iterative |
| Requirements | Fixed at beginning | Can change |
| Documentation | Heavy | Lightweight |
| Customer involvement | Limited | Continuous |
| Flexibility | Low | High |

Structured methods work well when requirements are stable.

Agile methods work better when requirements frequently change.

---

## 15 When to Use Structured Methodologies

Structured methodologies are suitable for projects with the following characteristics.

| Situation | Reason |
|-----|-----|
| Stable requirements | Changes are minimal |
| Large government projects | Require strict documentation |
| Safety critical systems | Require high reliability |
| Highly regulated industries | Require formal approval processes |

Example

Banking systems  
Healthcare systems  
Government information systems

---

## Chapter Summary

Structured methodologies are traditional approaches for developing information systems.

They emphasize sequential development, detailed documentation, and strict planning.

Major structured methodologies include:

Waterfall Model  
V Model  
SSADM

These methodologies are reliable for projects where requirements are stable and well defined.

However, their lack of flexibility led to the development of modern Agile methodologies.
