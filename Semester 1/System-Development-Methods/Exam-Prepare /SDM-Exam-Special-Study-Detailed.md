# SDM Exam Tips Detailed Notes

---

## 1 Data Analysis Process

### Definition

Data analysis is the process of transforming raw data collected from multiple sources into useful information that helps system analysts understand system problems and define system requirements.

The results of data analysis are normally used to prepare the System Requirements Specification (SRS).

---

### Stages of the Data Analysis Process

| Stage | Description | Purpose | Example |
|---|---|---|---|
| Data Collection and Compilation | Gathering and combining data from multiple sources | Understand the current system | Collecting feedback from system users |
| Data Cleaning | Removing incorrect, duplicate, or incomplete data | Improve data accuracy | Removing repeated survey responses |
| Data Analysis | Examining data to identify patterns or problems | Discover system weaknesses | Identifying frequent login failures |
| Data Visualization | Presenting results using charts, tables, or reports | Improve understanding of results | Graph showing system usage |
| Conclusions | Interpreting analysis results | Support creation of system requirements | Concluding the system requires improved security |

---

### Advantages of Data Analysis

- Helps identify real system problems  
- Improves quality of system requirements  
- Supports data based decision making  

### Disadvantages

- Requires reliable data sources  
- Cleaning data may take significant time  

---

## 2 System Requirements Specification (SRS)

### Definition

System Requirements Specification is a formal document describing all requirements that the system must satisfy.

It acts as an agreement between stakeholders and developers regarding system functionality and constraints.

---

### Purpose of SRS

- Clearly defines system requirements  
- Prevents misunderstanding between stakeholders and developers  
- Serves as a reference for system design and development  

---

### Types of System Requirements

| Requirement Type | Description | Example |
|---|---|---|
| Functional Requirements | Describe what the system must do | User login function |
| Non Functional Requirements | Describe system quality attributes | System response within two seconds |
| Technical Requirements | Describe technical environment needed | System must run on Linux server |
| Security Requirements | Protect system data and access | Password encryption |
| Interface Requirements | Interaction with other systems | Payment gateway connection |
| User Requirements | Requirements from user perspective | Simple search function |
| Business Requirements | Business goals supported by system | Increase online sales |

---

### Advantages of SRS

- Provides clear system documentation  
- Improves communication between stakeholders  
- Helps guide system development  

### Disadvantages

- Documentation preparation takes time  
- Requirements may change during development  

---

## 3 Types of Prototypes

### Definition

A prototype is an early version of a system developed to demonstrate system functionality and collect feedback before building the final system.

---

### Prototype Types

| Prototype Type | Description | Advantages | Disadvantages |
|---|---|---|---|
| Throw Away Prototype | Temporary prototype used to understand requirements | Quick development | Prototype discarded |
| Evolutionary Prototype | Prototype gradually improved until it becomes final system | Continuous improvement | May produce poor architecture |
| Incremental Prototype | System built from several smaller prototypes | Modular development | Integration complexity |
| Extreme Prototype | Prototype developed in stages for web systems | Effective for web systems | Mainly used for web applications |

---

### Extreme Prototype Stages

| Stage | Description |
|---|---|
| Stage 1 | Create static interface pages |
| Stage 2 | Develop system logic |
| Stage 3 | Integrate database and external services |

---

## 4 Coding Strategies

Coding strategies refer to planning decisions made before writing program code in order to ensure efficient system development.

---

### Software Architecture Strategy

Software architecture defines the overall structure of a system and how system components interact with each other.

---

### Types of Software Architecture

| Architecture | Description | Example |
|---|---|---|
| Monolithic Architecture | All system components combined into one system | Small applications |
| Client Server Architecture | Clients communicate with centralized server | Banking system |
| Layered Architecture | System divided into layers such as presentation, logic, and database | Web application |
| Microservices Architecture | System divided into independent services | Cloud based systems |

---

### Advantages of Good Architecture

- Improves system scalability  
- Simplifies system maintenance  
- Supports modular development  

### Disadvantages

- Requires careful planning  
- Poor architecture may cause system redesign  

---

### Programming Language Selection Strategy

Selecting a programming language depends on several factors.

| Factor | Explanation |
|---|---|
| System Performance | High performance systems may require efficient languages |
| Platform Compatibility | Language must support the target platform |
| Developer Expertise | Developers must be familiar with the language |
| System Complexity | Complex systems require advanced languages |

---

### Advantages

- Improves system efficiency  
- Supports maintainability  

### Disadvantages

- Incorrect language selection may create compatibility issues  

---

### Coding Standards Strategy

Coding standards define rules developers must follow when writing code.

Examples include naming conventions, formatting rules, and documentation guidelines.

---

### Advantages

- Improves readability of code  
- Simplifies debugging and maintenance  
- Supports teamwork in large projects  

### Disadvantages

- Requires discipline from developers  
- May slow development during early stages  

---

### Testing Strategy Before Coding

Testing strategies are planned to ensure system reliability and quality.

---

### Types of Testing

| Testing Type | Description |
|---|---|
| Unit Testing | Testing individual components |
| Integration Testing | Testing interaction between modules |
| System Testing | Testing the complete system |
| Acceptance Testing | Testing system with real users |

---

### Advantages

- Detects errors early  
- Improves system quality  

### Disadvantages

- Requires additional development effort  

---

## 5 Packaging Software

Packaging software prepares the system for installation and deployment.

---

### Packaging Activities

| Activity | Description |
|---|---|
| Source Code Protection | Secure and prepare system code |
| Installation Package Creation | Create setup installation files |
| File Compression | Reduce file size for distribution |
| System Deployment | Upload system to server |
| User Manual Preparation | Provide guide for system users |
| Technical Documentation | Provide guide for administrators |

---

### Advantages

- Simplifies system installation  
- Improves system distribution  

### Disadvantages

- Requires additional preparation work  

---

## 6 Mirror Swapping Strategy

### Definition

Mirror swapping is a maintenance strategy used to update systems without causing service downtime.

---

### Process

| Step | Description |
|---|---|
| Step 1 | Create duplicate mirror server |
| Step 2 | Perform maintenance on mirror server |
| Step 3 | Replace main server with mirror server |

---

### Advantages

- No system downtime  
- Continuous system availability  
- Safer maintenance process  

### Disadvantages

- Requires additional hardware infrastructure  
- Higher operational cost  

---

## 7 System Changeover Strategies

System changeover refers to replacing the old system with the new system.

---

### Direct Changeover

| Feature | Description |
|---|---|
| Definition | Old system immediately replaced by new system |
| Advantages | Fast implementation and low cost |
| Disadvantages | High risk if new system fails |
| Suitable For | Small systems |

---

### Parallel Operation

| Feature | Description |
|---|---|
| Definition | Old and new systems run at the same time |
| Advantages | Very low risk |
| Disadvantages | High operational cost |
| Suitable For | Critical systems |

---

### Pilot Operation

| Feature | Description |
|---|---|
| Definition | New system implemented in one department first |
| Advantages | Problems detected early |
| Disadvantages | Slower deployment |
| Suitable For | Systems replacing manual operations |

---

### Phased Operation

| Feature | Description |
|---|---|
| Definition | System implemented module by module |
| Advantages | Gradual transition |
| Disadvantages | Long implementation time |
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

## 9 Outsourcing in System Development

### Definition

Outsourcing refers to hiring external service providers to perform IT related tasks instead of performing them internally.

---

### Reasons for Outsourcing

| Reason | Explanation |
|---|---|
| Lack of Time | Internal team may not have enough time |
| Lack of Skills | Organization may lack technical expertise |
| Cost Reduction | External providers may reduce development cost |
| Focus on Core Business | Company can focus on main business goals |
| Resource Limitations | Internal staff may already be overloaded |

---

### Advantages of Outsourcing

- Access to expert knowledge  
- Reduces internal workload  
- Allows focus on core business activities  
- Faster development in some situations  

---

### Disadvantages of Outsourcing

| Disadvantage | Explanation |
|---|---|
| High Long Term Cost | Contract changes may increase costs |
| Communication Barriers | Language or time zone differences |
| Security Risks | Sharing system data may cause breaches |
| Less Control | Organization has less control over project |

---

## 10 Risk Management

### Definition

Risk management is the process of identifying, analyzing, and managing risks that may affect the success of a system development project.

---

### Risk Management Process

| Step | Description |
|---|---|
| Risk Identification | Identify potential risks |
| Risk Description | Describe each risk |
| Risk Analysis | Evaluate risk impact |
| Risk Prioritization | Classify risk severity |
| Risk Response Planning | Develop strategies to handle risks |
| Risk Monitoring | Monitor risks during project |

---

### Risk Management Strategies

| Strategy | Description |
|---|---|
| Risk Transfer | Transfer risk to another party such as vendor |
| Risk Avoidance | Change plan to eliminate risk |
| Risk Reduction | Reduce likelihood or impact of risk |
| Risk Acceptance | Accept risk and prepare contingency plan |

---

### Importance of Risk Management

- Reduces project failure risk  
- Improves planning and decision making  
- Helps teams prepare solutions before problems occur  

---

## Quick Revision Summary

### Data Analysis Process

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

### Changeover Strategies

- Direct Changeover  
- Parallel Operation  
- Pilot Operation  
- Phased Operation  

---
