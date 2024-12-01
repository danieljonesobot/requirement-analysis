# Requirement Analysis in Software Development


The purpose of this Repository is to understand and master the principles and methodologies of Requirement Analysis in the software development lifecycle (SDLC). The Requirement Analysis Project focuses on crafting a comprehensive foundation for software development by documenting, analyzing and structuring requirements.

This project simulates a real-world development scenario, emphasizing clarity, precision and structure in defining requirements to set the stage for successful project execution.

---



# What is Requirement Analysis?

Requirement Analysis is a critical phase in the Software Development Lifecycle (SDLC) that involves understanding, documenting, and managing the needs and expectations of stakeholders for a software system. This process ensures that the software being developed meets the functional and non-functional requirements of the users and aligns with business goals.

---



# Importance of Requirement Analysis in SDLC
- Foundation for Development:

    - Requirement Analysis serves as the blueprint for the design, development, and testing phases.
    - Well-documented requirements reduce ambiguities and ensure developers have a clear understanding of what to build.


- Alignment with Business Goals:

    - Ensures the software aligns with the organization’s objectives and adds value to stakeholders.


- Improved Communication:

    - Acts as a bridge between technical teams and non-technical stakeholders, fostering better collaboration and understanding.


- Reduction in Development Costs and Time:

    - Identifying and addressing issues early in the SDLC minimizes costly changes later in the development process.


- Enhanced Quality Assurance:

    - Clear requirements provide a basis for creating accurate test cases, ensuring the final product meets quality standards.


- Minimized Risks:

    - Proper analysis identifies potential technical and business risks early, enabling proactive mitigation.


- Customer Satisfaction:

    - Meeting user requirements ensures the software fulfills its intended purpose, leading to higher satisfaction levels.




---



# Key Activities in Requirement Analysis
## Requirement Gathering: Requirement Gathering involves collecting high-level needs and objectives from stakeholders to understand what the software system must achieve.

Key aspects include:

- Purpose: To collect all relevant information about the desired features, constraints, and goals of the system.
- Techniques: Interviews, surveys, workshops, observation, and document reviews.
- Outcome: A preliminary list of requirements, which serves as the starting point for further refinement.



## Requirement Elicitation: Requirement Elicitation is a deeper process of actively engaging with stakeholders to uncover explicit, implicit, and even hidden requirements.

Key aspects include:

- Purpose: To extract detailed, actionable, and clear requirements from various stakeholders.
    
- Techniques:
    - Interviews: One-on-one discussions with users and stakeholders.
    - Focus Groups: Facilitated sessions with multiple stakeholders.
    - Use Case Analysis: Defining specific user scenarios.
    - Prototyping: Demonstrating initial designs to gain feedback.
    
- Outcome: A refined and comprehensive set of requirements.



## Requirement Documentation: Requirement Documentation involves organizing and recording the gathered and elicited requirements in a structured format for easy reference and communication.

Key aspects include:

- Purpose: To create a single source of truth for all requirements.
    
- Common Formats:
    - Software Requirements Specification (SRS): A detailed document describing functional and non-functional requirements.
    - User Stories: High-level descriptions of system functionality from a user's perspective.
    
- Outcome: Well-structured and clearly written documentation to guide development and testing teams.


## Requirement Analysis and Modeling: Requirement Analysis and Modeling refine, clarify, and evaluate the requirements to ensure they are feasible, consistent, and aligned with business goals.

Key aspects include:

- Purpose: To analyze requirements for technical and business feasibility, identify conflicts, and model the system’s behavior.
    
- Techniques:
    - Gap Analysis: Comparing current capabilities with desired goals.
    - Modeling: Visual representations using diagrams like:
    - Use Case Diagrams: To show interactions between users and the system.
    - Data Flow Diagrams (DFD): To illustrate data processes.
    - Entity-Relationship Diagrams (ERD): To define database structure.
    
- Outcome: A clear understanding of how the system will work, addressing ambiguities and inconsistencies.



---

## Requirement Validation: Requirement Validation ensures that the documented requirements accurately reflect the stakeholders’ needs and are feasible within the project constraints.

Key aspects include:

- Purpose: To confirm requirements are complete, clear, achievable, and in alignment with the project’s goals.
    
- Techniques:
    - Reviews and Walkthroughs: Stakeholders and developers review the documented requirements.
    - Prototyping: Creating mock-ups to verify requirements.
    - Test Case Generation: Writing test cases to validate requirements during testing.

- Outcome: Stakeholder-approved requirements ready for design and development.



---



# Types of Requirements

## Functional Requirements
These are the features and functionalities that the system must support:

1. Hotel Management Service
    - Allow hotel managers/owners to manage hotel information, including room availability, pricing, and promotions.
    - Provide an API for hotel managers to update hotel-related data.
    - Synchronize updates between the master and slave databases for consistency.

2. Customer Service (Search + Booking)
    - Enable customers to search for hotels using filters such as location, price, and amenities.
    - Allow customers to book hotels and receive confirmations.
    - Integrate with third-party payment services for seamless transactions.
    - Provide recommendations and offers based on the user's location and preferences.

3. View Booking Service
    - Display current and historical booking details for both customers and managers.
    - Send notifications to managers for new bookings and to customers for promotions or booking confirmations.
    - Archive older booking data to ensure system scalability.

4. Notification System
    - Notify users about new offers, updates, and booking confirmations.
    - Deliver notifications efficiently using messaging queues and Kafka.

5. Data Storage and Archival
    - Store search and booking data in ElasticSearch for faster retrieval.
    - Archive older booking data in Cassandra to manage database growth and optimize query times.


## Non-functional Requirements

These define the quality attributes and operational capabilities of the system:

1. Performance
    - Handle high volumes of user traffic without delays or interruptions.
    - Optimize search and booking responses using caching systems like Redis and ElasticSearch.

2. Scalability
    - Use a microservices architecture to allow independent scaling of services like search, booking, and notifications.
    - Employ a CDN to distribute content geographically and reduce server load.

3. Reliability
    - Ensure system availability through a load balancer to distribute traffic across multiple servers.
    - Use master-slave database architecture to maintain data consistency and backup.

4. Data Consistency
    - Synchronize updates between master and slave databases.
    - Ensure real-time updates to customers and managers through Kafka messaging queues.

5. Security
    - Secure customer and payment data during transactions.
    - Authenticate access to manager and customer portals.

6. Maintainability
    - Modularize the system using microservices to make updates and maintenance easier.
    - Use standardized APIs for interaction between services.

7. Big Data Support
    - Use Apache Streaming and Hadoop for Big Data analysis, enabling insights like customer segmentation and business trends.

8. User Experience
    - Minimize booking and search response times using Redis for caching.
    - Provide real-time updates and notifications to enhance user satisfaction.




---


# Acceptance Criteria
Acceptance Criteria define the conditions that a feature or functionality must meet to be considered complete and accepted by stakeholders. These are critical in Requirement Analysis as they ensure alignment between stakeholders and the development team, setting clear expectations for deliverables.



1. Importance of Acceptance Criteria:
- Clear Scope Definition: Acceptance criteria eliminate ambiguity by providing specific requirements for feature completion, ensuring the team understands what needs to be built.

- Alignment with Business Goals: They bridge the gap between technical implementation and business objectives, ensuring the product delivers value to users and stakeholders.

- Improved Testing and Validation: Serve as a foundation for creating test cases, helping QA teams verify that the feature functions as expected.

- Facilitate Communication:Provide a shared language between technical and non-technical stakeholders, enhancing collaboration.

- Reduced Rework:Clear criteria minimize misunderstandings and misaligned expectations, reducing the chances of rework or feature changes later in the development process.

- Informed Decision-Making: Help product managers and stakeholders decide whether a feature meets the desired standards for release.




2. Example of Acceptance Criteria for a Checkout Feature in the Booking Management System
Feature: Hotel Booking Checkout
Acceptance Criteria:

- Payment Processing: 
    - The system must support multiple payment methods (e.g., credit cards, debit cards, PayPal).
    - Payment should be processed securely through a third-party payment gateway.
    - An error message must be displayed for failed transactions with reasons (e.g., insufficient funds, invalid card).


- Invoice Generation:
    - A digital invoice must be generated immediately after payment confirmation.
    - The invoice should include booking details (e.g., hotel name, booking ID, check-in and check-out dates, total cost).


- Booking Confirmation:
    - After a successful payment, the system must send a confirmation email to the user with booking details.
    - A notification must also be sent to the hotel manager about the booking.


- Cart Functionality:
    - Users should be able to review their selected room(s), pricing, and applicable taxes before confirming the payment.
    - Users can modify or cancel items in the cart before final checkout.


- Validation:
    - All mandatory fields (e.g., payment details, guest information) must be validated before proceeding.
    - The system must prevent overbooking by checking room availability in real-time before completing the transaction.


- Timeout Handling:
    - If the user is inactive for more than 15 minutes on the checkout page, the system must display a timeout message and release the selected room for others.


- Responsiveness:
- The checkout feature must function seamlessly across web and mobile platforms.


By defining acceptance criteria, the development team can clearly understand the definition of done for the checkout feature, reducing ambiguity and ensuring stakeholder satisfaction.
