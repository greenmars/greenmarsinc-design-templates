*This document is intentended to be a starting place for small-project to large-feature design efforts.  Larger projects may need something more, smaller efforts will need something less. While it's primary audience is the developers who implement the design, it also serves an important function in communicating to developers who come later and who have to make changes in a system that's new to them.*

*Instructions: When you are done, all the elements marked in italics in the original document should be replaced with the content being requested.  Of course, you can use italics in your own documents, but in this template, templates are only used to indicate instructions or places where you need to "fill in the blanks*

*This document makes signifcant refernces to the design checklist, which you should read through while creating a design in any case.*



*Effortname* **Design**

**Lead Author:** *Name* *(not "green mars", readers will want to navigate from this document to individuals to ask questions of.)  Git will be able to track down later changes, but it's still helpful to identify the point person for this doc.*



**Introduction**

*A basic, readable introduction to the feature, perhaps with a little context about the project it is a part of.  This should identify who uses the feature, what the feature accomplishes, why that is valuable and should explain those things in general, straightfoward language, avodiing glossary terms (unless explained here) and marketing-speak.  One or two paragraphs wher possible, this does not replace more compete explanations  to come later.*

*A few words about project context can fit in nicely here. If the client is on an unusually tight budget or schedule, include that sort of basic scene-setting here.*

**A diagram may be included in this section, but should be included only if it is simple and accessible enough that a reader can make sense of what it's saying without the context provided further down in the document. Complex architectural diagrams are best included further down in the doc.*



**Glossary**

*Focus here on terms that are specific and new to the feature/scope of this document.*  Less-frequently used tools or standards should be included here.  (e.g., a feature involving HL7 should probably have a quick description of what HL7 is here, even if only a single short sentence.)

* *key term 1:  description of key term 1*
* *key term 2: description of key term 2*



**People**

*Key people to include in this section are whoever at the client is responsible for resolving questions about client requirements around the feature, and who at the client is responsible for QA'ing the work.* *Include the go to person for access needs (VPN, repo, etc.)*

	* *client person 1:  role description*
	* *client person 2: ...*



**BACKGROUND**

**Basics**

*Does the code we're working on live in particular repos, etc, or have unusual (for this project environmental requirements)?*

**Requirements**

*Links to formal requirements for the project or feature, including (but not limited to) requirements about runctionality, data organization, environment, performance, privacy, security, and reliability.* *These should never be included in-line, but must be links to a separately-versioned and maintained store.*

**User Stories**

*Links to user stories for the document.  User stories provide readable narratives that help developers quickly gain an intuition as to what they are being asked to build.*  *In a pinch, these can go in-line here.*

**Mockups**

*Links to UI/UX prototypes.*  *An inline picture is nice here too, if one or two will really provide context.*

**Performance, Scalability, and Reliability**

*A summary description of performance, response, and scalability needs for the feature.  Basic UI/UIX response time expectations belong here, as do estimates of the scale of traffic that a server will need to handle (e.g,. 10 exams a minute, or 10,000?).  Uptime guarantees, if any, belong here. Think of this as a readable, executive summary of the key, relevant formal requirements, which should be linked.*

**Privacy and Security**

*A summary description of privacy/security issues relevant to this effort.  Think of this as a readable, executive summary of the releavnt formal documents, which should be linked.*




**DESIGN**

**Architecture**

*Broad server communications, data flow and/or data model diagrams go here. In efforts where established parts of the architecture are being modified, include before and after diagrams where possible.*


***At this point, we FINALLY get to the detailed design.  This will be most of the document when it's complete, since there will usually be several new data structures and functions for a new effort.***

**Data**

*Descriptions, with diagrams where helpful, of new data structures. Each new data structure or data type should be given a specific and complete description.*

**Functions**

*Descriptions, with diagrams where helpful, of new methods/functions/actions Each new data structure or data type should be given a specific and complete description.* Previous templates focused on o


**OPEN QUESTIONS**

*This section is a useful place to record design risks during the process of devloping design.  Usually most of these questiosn will be resolved before development begins, however.  This section can be omitted if irrelavant.*



**CONCERNS AND RISKS**

**High-Level Risks**

*Any substanital risk that could threaten the feasability of the effort should be listed here, even if the risk is of a type addressed in a later section.  (It's fine to simply say "See the section on such-and-such below."  It is very important that devs have the biggest concerns pointed out to them during the engineering process so that those risks can be resolved as quickly as possible.

**Technical Debt (Incoming)**

*Are there particularly tricky modules in the code our design plans to change? Who are the subject matter experts for those modules? Are there modules whose experts are no longer available?** Omit this section if irreleavnt*.

**Technical Debt (Outgoing)**

*Does our design create fragiilty or other points of concern?  Omit this section if irreleavnt.*

**Performance, Scalability, Reliability**

*Any discussion needed to explain, where it's not obvious, why the design will be able to meet the requirement targets for these factors should be placed in a section here.*

**Security and Privacy**

*Any discussion needed to explain, where it's not obvious, why the design will be able to meet the requirement targets for these factors should be placed in a section here.* *Omit this section if irreleavnt, but be sure it's irrelevant.*

**Testability**

*This section isn't a test plan, but simply a short description of how the designer imagines that a QA engineer would be able to determine whether the feature works correctly or not. In some cases this will be very easy, in others, it will be more complex, but the section should provide the reader some confidence that the design provided can be verified.*

*This section should also include hints as to what sections of the design will, after coding, probably deserve greater scrutiny during the quality process.  e.g., "The mumbleFrtoz function probably will need careful testing because XYZ."*

*This section should also identify any recommended unit tests for the effort.*

*This section should address, at least in broad terms, needed resources for testing.  (e.g., are special versions of some servers needed?)*

*Links to actual test documents/plans/etc. can be included here as well. but will usually not be available at the time the design is created.*
