# Report
## Table of Contents

## Acknowledgments

## Executive Summary
This report presents an analysis and evaluation of a new information system for a major travel company.

### Problem Definition
The current system for a Call Management Centre is inefficient. Both potential and existing customers are matched to Relationship Managers according to availability. As a result, the time of the Relationship Managers is not being used efficiently and customers have to wait longer to talk to a Relationship Manager. Consequently, customers are less likely to accept an offered product and sales are reduced. A new system is to be developed to increase the amount of customers and the likelihood of customers purchasing products.

### Objectives
- Reduce the average customer waiting time
- Reduce the amount of customers hanging up from a busy line
- Increase the total target customers purchasing products
- Increase the total existing customers purchasing products
- Increase the total customer intake

### Methods and Data Sources
The methods of analysis and evaluation used are Use Cases, Use Case Diagrams, Activity Diagrams, Class Diagrams and Collaboration Diagrams.

### Key Findings
### Conclusions

## Body of the Report
### Stakeholders
### Empathy Maps
### Point of View Statements
### How Might We statements
### Reflection
### User Stories
Relationship Manager
User Story ID | User Story
-- | --
UD01 | As a Relationship Manager, I want to take a questionnaire so that a personalised profile can be made.
UD02 | As a Relationship Manager, I want the system to build a profile and skill matrix so that the customers can be matched more appropriately.
UD03 | As a Relationship Manager, I want the system to adjust the profile according to my results so that I can be matched with customers that are within my skill level.
UD04 | As a Relationship Manager, I want the customer details to be displayed to me so that I can adjust my advertisement to better suit the customer.
UD05 | As a Relationship Manager, I want the Interactive Voice Response unit to prompt customers with their options and their call reasons so that I know why they are calling. 
UD06 | As a Relationship Manager, I want guidelines and a script to be generated for each customer so that the I have a reference to use.

Company Owner
User Story ID | User Story
-- | --
UD07 | As a Company Owner, I want a customer target list to be generated so that we can reach more potential customers.
UD08 | As a Company Owner, I want to be able to retrieve customer details so that conversations can be personalised and Relationship Managers can be matched efficiently. 
UD09 | As a Company Owner, I want the guidelines and the script to be used by the Relationship Managers so that the Relationship Managers can provide a better service.
UD10 | As a Company Owner, I want a skill score to be generate for each Relationship Manager based on their history so that they are matched up with customers who are in their skill range.
UD11 | As a Company Owner, I want a score to be generated for each customer based on their likelihood to buy a product so that the most appropriate Relationship Manager can be designated to them.
UD12 | As a Company Owner, I want the customers with the highest score to be called first so that more products are likely to be purchased overall.
UD13 | As a Company Owner, I want each customer to be matched with a Relationship Manager based on their profiles so that the time of the Relationship Managers is used efficiently.
UD14 | As a Company Owner, I want the system to direct customers to the Interactive Voice Response unit when a Relationship Manager is unavailable so that they do not hang up.

Customer
User Story ID | User Story
-- | --
UD15 | As a Customer, I want to be rerouted to a matched Relationship Manager as soon as possible so that I do not have to wait to talk.

### Backlog
### Use Cases
User Case Name | Complete Profile Questionnaire
-- | --
Use Case ID | UC001
User Stories | UD01, UD02, UD03, UD10
Goal | Build Relationship Manager profile based on questionnaire
Priority | Moderate
Actors | Relationship Managers
Pre-conditions | 
Post-conditions | Relationship Manager has personalised profile
Trigger | Relationship Manager is hired
Main Flow | 1. Relationship Manager is given questionnaire to complete<br>2. Relationship Manager takes 10 minutes to complete questionnaire<br>3. A skill matrix and profile is generated based on questionnaire results
Exceptions | 
Includes/Extends/Inherits |
Non-Functional Requirements | Current employees will additionally have to take the questionnaire to get a custom profile established

User Case Name | Outbound Call
-- | --
Use Case ID | UC002
User Stories | UD04, UD09
Goal | Connect Relationship Manager to customer
Priority | High
Actors | Relationship Managers, Potential Customers
Pre-conditions | There are available customers that match the Relationship Manager's profile
Post-conditions | Relationship Manager is connected to customer
Trigger | Relationship Manager calls Potential Customer
Main Flow | 1. The Relationship Manager calls the customer<br>2. The customer details are displayed to the Relationship Manager<br>3.The Relationship Manager uses the script and guidelines to talk to the customer
Exceptions | Customer does not take call<br>Customer hangs up
Includes/Extends/Inherits | Includes Match Relationship Manager to Customer
Non-Functional Requirements |

User Case Name | Inbound Call
-- | --
Use Case ID | UC003
User Stories | UD05, UD12, UD14, UD15
Goal | Connect customer to Relationship Manager
Priority | High
Actors | Relationship Managers, Existing Customers
Pre-conditions | 
Post-conditions | Customer is connected to Relationship Manager
Trigger | Customer calls Call Management Centre
Main Flow | 1. The customer calls the Call Management Centre<br>2. Customer is routed the the most appropriate Relationship Manager. If no appropriate Relationship Managers are available see "Alternate Flow 1"
Exceptions | Customer hangs up
Includes/Extends/Inherits | Includes Match Relationship Manager to Customer
Non-Functional Requirements |

Alternate Flow 1 | Initiate Interactive Voice Response
-- | --
Trigger | No available appropriate Relationship Managers
Steps | 1. The Interactive Voice Response unit prompts the customer for options<br>2. The Interactive Voice Response unit prompts the customer for call reasons<br>3. The customer is directed to the Automatic Call Distributor
Post-conditions	| Customer is connected to an appropriate Relationship Manager
Exceptions | Customer hangs up

User Case Name | Generate Customer Profile
-- | --
Use Case ID | UC004
User Stories | UD06, UD07, UD08
Goal | Customer profile is generated base on background
Priority | Moderate
Actors | 
Pre-conditions | The customer details are available
Post-conditions | The customer has a personalised profile
Trigger | Potential buyer is discovered
Main Flow | 1. A customer target list is generated<br>2. The customer details are retrieved from a database<br>3. A script and a guidelines is generated for each customer
Exceptions | Customer details are not able accessible 
Includes/Extends/Inherits | Extends Outbound Call
Non-Functional Requirements | Existing customer will additionally have to have a custom profile established

User Case Name | Update Customer Profile
-- | --
Use Case ID | UC005
User Stories | UD11
Goal | Customer profile is updated
Priority | Low
Actors | 
Pre-conditions | Customer has an existing profile
Post-conditions | Customer profile has been appropriately updated
Trigger | Customer makes a purchase
Main Flow | 1. Retrieve customer profile<br>2. Update customer profile to indicate increase in likelihood of purchases
Exceptions | 
Includes/Extends/Inherits | Extends Inbound Call
Non-Functional Requirements |

User Case Name | Match Relationship Manager to Customer
-- | --
Use Case ID | UC006
User Stories | UD13
Goal | Customer is matched is most appropriate Relationship Manager
Priority | High
Actors | 
Pre-conditions | Relationship Manager profile exists<br>Customer profile exists
Post-conditions | Customer is matched to Relationship Manager
Triggers | Customer needs to be matched to Relationship Manager<br>Relationship Manager needs to be matched to Customer
Main Flow | 1. Retrive customer profile<br>2. Retrieve Relationship Manager profiles<br>3. Match most appropriate Relationship Manager to customer
Exceptions | 
Includes/Extends/Inherits |
Non-Functional Requirements |

### Use Case Diagram
![Use Case Diagram](https://cdn.discordapp.com/attachments/639469570838626334/716308844791332954/usecasediagram.png)
### Activity Diagrams
### Class Diagram
![Class Diagram](https://cdn.discordapp.com/attachments/639469570838626334/716536222385831956/Class_Diagram3.png)
### Collaboration Diagrams

## References

## Appendices
