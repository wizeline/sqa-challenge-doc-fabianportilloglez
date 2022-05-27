# **Test Plan**

1. ### **Scope, objectives, approach and risks**

2. ### **Test Basis** 

(use cases, diagrams, requirements, source code, data model, business processes)

3. ### **Scheduling of internal test activities**

(analysis, design, implementation, execution):

Agile practices worked in the project by iterations.

___
4. ### **Entry Criteria and Exit Criteria**

#### **Entry Criteria:**

*	Availability of:
    * testable requirements, user stories, and/or models (e.g., when following a model based testing strategy) 
    *	test items that have met the exit criteria for any prior test levels
    *	test environment 
    *	necessary test tools 
    *	test data and other necessary resources

#### **Exit Criteria:**

*	Planned tests have been executed 
*	A defined level of coverage (e.g., of requirements, user stories, acceptance criteria, risks, code) has been achieved 
*	The number of unresolved defects is within an agreed limit 
*	The number of estimated remaining defects is sufficiently low 
*	The evaluated levels of reliability, performance efficiency, usability, security, and other relevant quality characteristics are sufficient
___

### **Test Design Techniques:**

**Types of techniques:**

1. Equivalence Partitioning
2. Boundary Value Analysis
3. Decision Table Testing
4. Error guessing

### **Test Levels:**

1. Component testing
2. Integration testing
3. System testing
4. User Acceptance testing
___
___
# **Test Strategy**

Manual or automated it depends of the type of test.

### **Main points:**

**Some factors to consider as main factors of success are:**

* Project complexity
* Project goals
* Type of product being developed
* Product Risk Analysis 

**Other considerations depending of the context are:**

* Risks
* Safety
* Available resources and skills
* Technology
* Nature of the system
* Test objectives
* Regulations

### **Automation Strategy**

### **Best practices**

* Design the tests before automate them
* Automate the repetitive tasks (but those to be executed once not)
* If testing environments are unestable, don’t automate (could create “false positive”)
* The tests include logs and screenshots any time 
* Tests run without any other test dependency or process
* Avoid testing 3rd party processes or systems
* Keep your tests in only one repo or cluster
* Use the same coding standards as developers 
* Run the tests must be fast, if not; exclude them or run in parallel)
* Create tests that can run in any environment (consider even those that don’t exist yet but will be used)

**Test case automation priority:**

* Consider existing manual tests over creating new test cases
* Consider API tests over UI tests
* Consider work on the services with more frequent deployments first and used by customer workflows 

