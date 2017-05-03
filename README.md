# DDD Dojo Part 1
Clone these when you attend my Dojo.

Please Follow the examples as specified by the presenters:



## Section 1 
**Domain Driven Design Dojo - Example**

This section refers to the following:
* `src/1. Intro and Moddeling/1.Animic` and `src/1. Intro and Moddeling/2.RichDomain` - This Example shows an Anemic Domain and Rich Domain implementing the same set of Business Rules.
* `src/1. Intro and Moddeling/3.Animic.Changed` and `src/1. Intro and Moddeling/4.RichDomain.Changed` - A rule change is then introduced with the changes reflected in each implementation.

**Business Rules Reflected in the 1.Anemic and 2.RichDomain Projects:**

* As an **Employee** I want to
    * Capture Leave
    * Capture Different Types of Leave
        * Annual
        * Study
    * Escalate leave to a different approver. Approver sequence for each leave type is as follows
        * Annual - Team Lead -> Account Manager -> General Manager
        * Study - Account Manager -> General Manager
    * Change My Leave Type. This returns it to a pending status
* As an **Approver** I want to
    * Approve Leave that is assigned To me
* As a **Manager** I want to finalize leave that has been approved

**Rule Change Reflected in the 3.Anemic and 4.RichDomain Projects**

Introduce a new **Sick Leave** type

* Use the same Approver Sequence as Annual Leave
* Can only be finalized if a sick note is provided
___

## Section 2
**Practical Example - Gym Loyalty**

A Member on a Loyalty program qualifies for discounts on Gym Fees based on the Gym Club Type and the length of the Gym Membership. The business needs to calculate the refund amount monthly based on the following rules.

* There are three Club Types
    * Silver
    * Gold
    * Platinum
* If a member has been going to the gym for less than 12 Months, they get refunded a 	percentage.
    * Silver -> 40%
    * Gold -> 60%
    * Platinum -> 80%
* If a member has been going to the gym for more than 12 Months, they get refunded an amount 	per visit up to the total gym cost, but are required to visit the gym a minimum of 6 times 	per month to be eligible for a refund
    * Silver -> R30 per visit up to R500
    * Gold -> R50 up to R600
    * Platinum -> R75 up to R1000
* Assume you are provided with the monthly visits, club types and start date.

**Change 1**

Add a new **Blue** club type.
Cost R400
Gets Refunded R35 per visit up to R400 for a minimum of 6 visits per month from the start. (No initial % discount rule exists for the first month)

**Change 2**

Members can change club type.

___

## Section 3
**Moddeling an Example**

As an online shopping store **Globaltrade Pty Ltd** we sell products to customers.


**We would like to see a focus around the *PRODUCT* entity.**


* **Customer** details are maintained in the system.
* **Customers** place **products** in a **shopping cart**, and can then create an **orde**r.
* Some **products** might be on **special** via some marketing venture.
* **Orders** are finalised by a **payment**, which issues an **invoice** for the **order**.
* **Invoices** and **orders** are stored against a **customer** as sales history.
* **Orders** that are invoiced gets shipped to a **customers**' chosen shipping **address**.
* **Marketers** are chosen by the company to run **campaigns** and promote **products** by adjusting pricing, bundling **products**, **Coupons** etc.
* These Marketing specials or **campaigns** can have **Coupons** that can be redeemed to further reduce prices for **products**.
* **Products** are stored in **warehouses** around the world.
* **Products** are shipped to **customers** from the closest **warehouse** where stock is available.
* Some **products** have special **storage requirements**. (for example electronics need to stay dry.)
* **Warehouses** are aware of the number of items available for each **Product**.
* **Products** have packaged **dimensions** which helps **warehouse** staff plan and optimize how much and where the **product** can be stored.
* New **products** are supplied from **suppliers**.
* All inbound stock from **suppliers** is tracked so that **customers** can be notified when stock will be available (Destination **warehouses**, **transport method**, ETA etc).
____