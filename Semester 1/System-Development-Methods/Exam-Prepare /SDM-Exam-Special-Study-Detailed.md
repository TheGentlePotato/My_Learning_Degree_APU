
# SDM Exam Tips Detailed Notes

---

## 1 Data Analysis Process

### Definition

Data analysis is the process of transforming raw data collected from different sources into meaningful information that helps system analysts understand system problems and define accurate system requirements.

The results of data analysis are normally used when preparing the System Requirements Specification (SRS).

---

### Stages of Data Analysis Process

| Stage | Description | Purpose | Example |
|---|---|---|---|
| Data Collection and Compilation | Collect data from different sources such as interviews, questionnaires, observation, documents, and databases | Understand the current system | Collecting feedback from system users |
| Data Cleaning | Remove duplicate, incorrect, incomplete, or irrelevant data | Improve data accuracy | Removing duplicate survey responses |
| Data Analysis | Identify patterns, relationships, and trends | Discover system problems | Identifying that most users complain about login errors |
| Data Visualization | Present results using charts, graphs, and reports | Help stakeholders understand results | Pie chart showing system issues |
| Conclusions | Interpret the results and determine system improvements | Support system requirement development | Deciding to improve authentication system |

---

### Advantages of Data Analysis

- Helps analysts understand real system problems
- Improves accuracy of system requirements
- Supports data driven decision making

### Disadvantages

- Requires large amount of reliable data
- Data cleaning can be time consuming

---

## 2 System Requirement Specification (SRS)

### Definition

System Requirements Specification is a formal document describing all system requirements and constraints that must be satisfied by the system.

It serves as an agreement between stakeholders and developers.

---

### Purpose of SRS

- Defines system functionality clearly
- Reduces misunderstandings between stakeholders
- Serves as reference for system design and development

---

### Types of System Requirements

| Requirement Type | Description | Example |
|---|---|---|
| Functional Requirements | Specific operations the system must perform | User login system |
| Non Functional Requirements | Quality attributes such as performance or reliability | System response within 2 seconds |
| Technical Requirements | Technical environment required to run system | Linux server |
| Security Requirements | Protection mechanisms for system data | Data encryption |
| Interface Requirements | Interaction between systems or devices | Payment gateway integration |
| User Requirements | Expectations from system users | Easy search function |
| Business Requirements | Organizational goals supported by system | Increase online sales |

---

### Advantages of SRS

- Provides clear system specification
- Helps developers understand system requirements
- Improves development planning

### Disadvantages

- Requires extensive documentation
- Requirements may change during development

---

## 3 Types of Prototypes

### Definition

A prototype is an early version of a system developed to demonstrate system functionality and collect feedback before building the final system.

---

### Prototype Types

| Prototype Type | Description | Advantages | Disadvantages |
|---|---|---|---|
| Throw Away Prototype | Temporary prototype built only to understand requirements | Quick development | Prototype discarded |
| Evolutionary Prototype | Prototype continuously improved until final system | Continuous improvement | Architecture may become messy |
| Incremental Prototype | System built using several smaller prototypes | Modular development | Integration complexity |
| Extreme Prototype | Used mainly for web systems with staged development | Efficient for web systems | Limited to web applications |

---

### Extreme Prototype Stages

| Stage | Description |
|---|---|
| Stage 1 | Create static web interface |
| Stage 2 | Develop application logic |
| Stage 3 | Integrate database and services |

---

## 4 Coding Strategies

Coding strategies are planning approaches used before writing software code to ensure efficient, maintainable, and scalable system development.

---

### Software Architecture Strategy

#### Definition

Software architecture refers to the overall structure of a system and the way system components interact.

---

### Common Architecture Types

| Architecture | Description | Example |
|---|---|---|
| Monolithic Architecture | All components integrated into one system | Small applications |
| Client Server Architecture | Client communicates with centralized server | Banking systems |
| Layered Architecture | System divided into layers such as presentation, logic, database | Web applications |
| Microservices Architecture | System divided into independent services | Cloud platforms |

---

### Advantages of Good Architecture

- Improves system scalability
- Simplifies maintenance
- Allows modular development

### Disadvantages

- Requires careful planning
- Poor architecture leads to system redesign

---

### Programming Language Selection Strategy

Developers must select programming languages suitable for system requirements.

---

#### Factors to Consider

| Factor | Description |
|---|---|
| System performance | Some languages provide higher performance |
| Platform compatibility | Language must support target platform |
| Developer expertise | Developers must understand the language |
| System complexity | Complex systems require advanced languages |

---

### Advantages

- Efficient system development
- Better performance and scalability

### Disadvantages

- Incorrect language choice causes compatibility issues

---

### Coding Standards Strategy

Coding standards define rules developers follow when writing software code.

Examples include formatting rules, naming conventions, and documentation practices.

---

### Advantages

- Improves code readability
- Simplifies debugging
- Supports team collaboration

### Disadvantages

- Requires developer discipline
- May slow development initially

---

### Testing Strategy Before Coding

Testing strategies ensure system quality during development.

---

### Types of Testing

| Testing Type | Description |
|---|---|
| Unit Testing | Testing individual components |
| Integration Testing | Testing interaction between modules |
| System Testing | Testing complete system |
| Acceptance Testing | Testing with real users |

---

### Advantages

- Detects errors early
- Improves system reliability

### Disadvantages

- Requires additional development time

---

## 5 Packaging Software

Packaging software prepares the system for installation and deployment.

---

### Packaging Activities

| Activity | Description |
|---|---|
| Source Code Protection | Secure and prepare source code |
| Installation Package Creation | Create setup installation files |
| File Compression | Reduce file size for distribution |
| System Deployment | Upload system to server |
| User Manual Preparation | Guide for system users |
| Technical Documentation | Guide for administrators |

---

### Advantages

- Simplifies installation
- Supports system distribution

### Disadvantages

- Requires additional preparation work

---

## 6 Mirror Swapping Strategy

### Definition

Mirror swapping is a maintenance strategy that allows system updates without interrupting system operations.

---

### Process

| Step | Description |
|---|---|
| Step 1 | Create duplicate mirror server |
| Step 2 | Perform updates on mirror server |
| Step 3 | Replace main server with mirror server |

---

### Advantages

- No system downtime
- Continuous service availability
- Safe maintenance process

### Disadvantages

- Requires extra server infrastructure
- Higher operational cost

---

## 7 System Changeover Strategies

System changeover refers to replacing the old system with the new system.

---

### Direct Changeover

| Feature | Description |
|---|---|
| Definition | Immediate replacement of old system |
| Advantages | Fast implementation and low cost |
| Disadvantages | High risk if new system fails |
| Suitable For | Small and non critical systems |

---

### Parallel Operation

| Feature | Description |
|---|---|
| Definition | Old system and new system run simultaneously |
| Advantages | Very low risk |
| Disadvantages | High operational cost |
| Suitable For | Critical systems |

---

### Pilot Operation

| Feature | Description |
|---|---|
| Definition | System implemented in one department first |
| Advantages | Problems detected early |
| Disadvantages | Slower full deployment |
| Suitable For | Systems replacing manual processes |

---

### Phased Operation

| Feature | Description |
|---|---|
| Definition | System implemented module by module |
| Advantages | Gradual transition |
| Disadvantages | Longer implementation time |
| Suitable For | Large complex systems |

---

## 8 Parallel Operation vs Phased Operation

| Feature | Parallel Operation | Phased Operation |
|---|---|---|
| Implementation | Entire system runs simultaneously | Module by module |
| Risk | Very low | Low |
| Cost | High | Lower |
| Speed | Faster | Slower |
| Suitable For | Critical systems | Large systems |

---

## Quick Revision Summary

### Data Analysis

- Data Collection
- Data Cleaning
- Data Analysis
- Data Visualization
- Conclusions

---

### Prototype Types

- Throw Away Prototype
- Evolutionary Prototype
- Incremental Prototype
- Extreme Prototype

---

### System Changeover Strategies

- Direct Changeover
- Parallel Operation
- Pilot Operation
- Phased Operation
