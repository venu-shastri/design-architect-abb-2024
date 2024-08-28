# Who is an Architect ?
# Responsibilities of Architect

# What Influences the Architecture ?
- Architect's Ability , Skills, Knowledge
- Influential/ Significant  Functional Requirements
- Business constraints (Culture, Cost, Time , Market, People,....)
- Team's Ability , Skills , Knowledge
- Quality Attributes (lities) - better to have
- Standards
- Technology Trends 

# Requirement Classification
 - Functional
 - Non Functional 

# Documentation
- Requirement Document
	- Purpose and Scope(Describe System/Product From a Business Perspective
		- Business Context
			- StackHolders
			- Business Goals
	- Requirements
		- Influential Functional Requirements
			- Use Cases or User Stories
				- Activity and Use Case Diagrams
		- NFR
			- Define Qaulity Attributes
			- Capture Quality Attributes as Scenarios
			- Define Stimuls and Response
			- 
| Qaulity Attributes | Scenario |
|--|--|
|  Performance| A report must be generated within 5 seconds when the system is at peak load (~1000 users)|
 - Assumptions and Dependencies



- Architecture Document 
- System Landscape  (c4 System Landscape Diagram, Architetctural Reference Diagram) 
- Constraints (Condition or Limit )
	- Technical Constraints
		- Programming language choices
	- Business Constraints
		- Legal Constraints , TimeLine constraints
	- How to document Constraints
	- 
| constraint | Type | Origin |Context
|--|--|--|--|
|Product Must be ship by eod of Q3  | Business  | Product Owner/SH|Avoids end of fiscal year budget issues
|Must support Linux Platform|Technical | SH |Officially Supported OS Platform

- Context and Scope
	- c4 context diagram 
- Building Block View Level 1
	- c4 Container and Component Diagram
- Building Block View Level 2
	- c4 Code , LLD
- Deployment View
	- c4 Deployment Diagram
	- Describe how containers Deployed (technical stack, infrastructure)
- Runtime View
	- Realization of Use Case
	- Describe How building Block views interact in each use cas
	- Dynamic View - C4 , Communication Diagram (UML)
NFR Decisions
	- ADR (Architecture Decision Record)
		- Title
		- Context
		- Decision
		- Status
		- Consequences
- Solution Structure
	- - Project Structure
- Environments
	- staging 


- Verification Report Document
