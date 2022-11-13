
***

## V-model is an [[SDLC]] model

***

![[Pasted image 20221017192049.png]]

***

## Also known as Verification & Validation model

- ##### Each process happens in sequential manner.

- ##### And each development stage associated with testing phase.

- ##### Development and Validation phases planned in parallel. This is because it called Verification & Validation

- ##### This is high-disciplined sdlc model, it means that next phase starts only after completion previous one.

- ##### V-model is extension of Waterfall model. 

***

## Verification Phases (Left side)

- #### Business requirement analysis.
	First stage of Verification phases and the most important. It includes work with customer to understand his expectations and requirements. 
	Acceptance test design is done at this stage and business requirements can be used as input for acceptance testing.

- #### System design 
	The system designing process means understanding and detailing the complete hardware and communication setup for the product. 
	System test plan developed based on the system desigh.

- #### Architectural design (High Level Design-HLD)
	The stage that contains choosing modules, data transfering, communication between systems etc.
	With this information integration tests can be designed.

- #### Module design (Low Level Design-LLD)
	This stage contains detailed design of all internal modules and units of the future system. 
	It allows to start unit test design.

- #### Coding phase 
	Process of coding in strong coding standarts and guideliness. Code must be reviewed and optimized for the best performance before final build will go to the main repository.

## Validation process (Right side)

- #### Unit testing
	Unit created while Module design phase are executed on the code while validation phase. It helps eliminate bugs at an early stage, but all defects can't be covered by unit testing.

- #### Integration testing 
	Process of testing coexistance and communication between internal modules

- #### System Testing
	System testing phase is exist to test whole system functionality, compability, communication, performance and load issues.

- #### Acceptance testing
	Associated with business requirement analysis phase and involves testing product in user environment

***

## Advantages and Disadvantages:

- #### Advantages:
	- Highly disciplened model, one phase at a time.
	- Works for small projects with simple and clear requirements.
	- Simply to understand and use.
	- Easy to manage.

- #### Disadvantages:
	 - High risk.
	 - Not for complex projects.
	 - Poor model for long and ongoing projects.
	 - Not for projects with mutable requirements.
	 - If project on test stage is too expensive to go back.





***

## [[Methodologies]]