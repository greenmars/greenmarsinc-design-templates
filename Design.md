*This document is intentended to be a starting place for small-project to large-feature design efforts.  Larger projects may need something more, smaller efforts will need something less. While it's primary audience is the developers who implement the design, it also serves an important function in communicating to developers who come later and who have to make changes in a system that's new to them.*

*Instructions: When you are done, all the elements marked in italics in the original document should be replaced with the content being requested.  Of course, you can use italics in your own documents, but in this template, templates are only used to indicate instructions or places where you need to "fill in the blanks"*

*You may want to keep the template text until the document sections are all present. Remember to delete before publishing.*

*This document makes signifcant references to the design checklist, which you should read through while creating a design in any case.*



# Design Title

**Design Lead: Name** (readers will want to navigate from this document to individuals to ask questions of.  Git will be able to track down later changes, but it's still helpful to identify a point person for this doc.)


# Introduction

*A basic, readable introduction to the feature, perhaps with a little context about the project it is a part of.  This should identify who uses the feature, what the feature accomplishes, why that is valuable and should explain those things in general, straightfoward language, avodiing glossary terms (unless explained here) and marketing-speak.  One or two paragraphs wher possible, this does not replace more compete explanations  to come later.*

*A few words about project context can fit in nicely here. If the client is on an unusually tight budget or schedule, include that sort of basic scene-setting here.*

*A diagram may be included in this section, but should be included only if it is simple and accessible enough that a reader can make sense of what it's saying without the context provided further down in the document. Complex architectural diagrams are best included further down in the doc.*



#Glossary

*Focus here on terms that are specific and new to the feature/scope of this document.*  Less-frequently used tools or standards should be included here.  (e.g., a feature involving HL7 should probably have a quick description of what HL7 is here, even if only a single short sentence.)

* *key term 1: description of key term 1*
* *key term 2: description of key term 2*




# Background


## Requirements

*Links to formal requirements for the project or feature, including (but not limited to) requirements about functionality, data organization, environment, performance, privacy, security, and reliability.* *These should never be included in-line, but must be links to a separately-versioned and maintained store.*

## User Stories

*Links to user stories for the document.  User stories provide readable narratives that help developers quickly gain an intuition as to what they are being asked to build.*  *In a pinch, these can go in-line here.

Describe use cases in narrative form. Cover the actions that users (whether they are end users or API clients) need to be able to perform. Describe them in a way that a QA technician could validate them without understanding the code.*

## UI/UX

*If necessary, describe user interface interactions and affordances. Also include links to UI/UX prototypes. An inline picture is nice here too, if one or two will really provide context.*

## Performance, Scalability, and Reliability

*A summary description of performance, response, and scalability needs for the feature.  Basic UI/UIX response time expectations belong here, as do estimates of the scale of traffic that a server will need to handle (e.g,. 10 exams a minute, or 10,000?).  Uptime guarantees, if any, belong here. Think of this as a readable, executive summary of the key, relevant formal requirements, which should be linked.*

*Some questions to answer if they are relevant: Are there performance requirements? Characterize the volume or rate of inputs, outputs, and storage if relevant. Are any of the components especially CPU, memory, storage, or network intensive? Is load likely to be spiky? What is the desired behavior if capacity is exceeded? Is load testing required?*

## Privacy and Security

*A summary description of privacy/security issues relevant to this effort.  Think of this as a readable, executive summary of the relevant formal documents, which should be linked.*



# Design

## Overall Architecture

*Broad server communications, data flow and/or data model diagrams go here. In efforts where established parts of the architecture are being modified, include before and after diagrams where possible.*

## System Infrastucture

*Describe supporting infrastructure needs. What server resources will be required?*

### Deployment

Gee it would be nice if stuff was written here.

## Connected Systems

*What other parts of the application or third-party systems does this one connect to?*

### System List

*List systems that provide input to or take input from this system. If they have design docs, provide links.*

### Interfaces

*Describe HTTP or code APIs that will be used to interact with this design.*

***At this point, we FINALLY get to the detailed design.  This will be most of the document when it's complete, since there will usually be several new data structures and functions for a new effort.***


## Domain Objects
*What are the data types? What behaviors do they support? Which objects interact?*

## Data Flow/Interaction Sequence
*Give a temporal view of program behavior. How does data flow through the system?*

## Algorithms
*Are there complex, non-trivial algorithms required by the design?  Are they relatively unique to the project (e.g., patient reconcilation for eXo), or instead are they relatively common needs (say, a fast fourier transform)?  Describe unique algorithms in detail.  For other algorithms, either use existing libraries/tools (and explain why you bleieve they're sufficient to the task) or provide a good engineering justification for not making use of existing tools.*

## Concurrency and Interactivity
*Are there processes that happen concurrently or asynchronously? Are there resulting race conditions? Is locking required?*

## Fault Tree Analysis
*How are exceptions and other faults handled?  (An example of a fault tree analysis can be found in our eXo Cloud Architecture document.)


# Open Questions

*Use this section to record design risks during the design process  Usually most of these questiosn will be resolved before development begins.  What still needs to be decided or described? This section can be omitted if irrelavant.*



# Concerns and Risks

## High-Level Risks

*Any substanital risk that could threaten the feasability of the effort should be listed here, even if the risk is of a type addressed in a later section.  (It's fine to simply say "See the section on such-and-such below."  It is very important that devs have the biggest concerns pointed out to them during the engineering process so that those risks can be resolved as quickly as possible.

## Technical Debt (Existing)

*Are there particularly tricky modules in the code our design plans to change? Who are the subject matter experts for those modules? Are there modules whose experts are no longer available?** Omit this section if irrelevant.*

## Technical Debt (New)

*Does our design create fragiilty or other points of concern?  For each identified problem, indicate whether the problem is solvable (perhaps with additional work that can't be done at the moment.)*

## Performance, Scalability, Reliability 

*Any discussion needed to explain, where it's not obvious, why the design will be able to meet the requirement targets for these factors should be placed in a section here.*

## Security and Privacy

*Any discussion needed to explain, where it's not obvious, why the design will be able to meet the requirement targets for these factors should be placed in a section here.* *Omit this section if irrelevant, but be sure it's irrelevant.*

## Testability 

*This section isn't a test plan, but simply a short description of how the designer imagines that a QA engineer would be able to determine whether the feature works correctly or not. In some cases this will be very easy, in others, it will be more complex, but the section should provide the reader some confidence that the design provided can be verified.*

*This section should also include hints as to what sections of the design will, after coding, probably deserve greater scrutiny during the quality process.  e.g., "The mumbleFrtoz function probably will need careful testing because XYZ."*

*This section should also identify any recommended acceptance tests for the effort.*

*This section should address, at least in broad terms, needed resources for testing.  (e.g., Do we need a to set up a separate set of servers to support testing separately from development and/or deployment?)*

*Links to actual test documents/plans/etc. can be included here as well. but will usually not be available at the time the design is first created.*
