## Organization structure
Dividing the company into smaller parts so everyone knows their roles in managing the materials 
Client 
Company code 
Plant
Purchasing organization
Storage location 
Purchasing Group 

## Company code 
Company code is a unique key for representing the company or legal entity within the larger organization 
Smallest organization unit within the client 
4 digit 

Plant 
Plant is physical location in company where work happens. It could be factory, warehouse, office or any other place where materials can be stored, produced, managed




Plants helps managing and organize the material in the specific location. It also the where the activities like purchainsg, inventory management, production takes place 

It can be assigned to company code 

Purchasing organization 
Purchasing organization is a team or department in company which is responsible for buying of materials and also inclues negotiating with supplier, managing contracts, and make sure the compay gets the material or services needs 
The company buys materials at the best prices.
Purchase orders are properly managed.
Vendors are selected and evaluated.
P org can be assigned to company code or plant based on the business requirement 

Storage location 
Storage location is a organizational unit and subdivision of plant 
Lowest organizational level which helps to differentiate the level of stocks 

Purcahsing group
A Purchasing Group is a small team or even a single person responsible for specific buying activities.
Responsible for certain type of material or service procurement 
Deals with vendor monitoring the purchasing activities 
Purchasing organxition not directly assigned to purcahsign org
If a Purchasing Organization is the department managing all company purchases, the Purchasing Group divides the work into smaller tasks or categories, like:
One group handles electronics.
Another group handles office supplies.
Yet another focuses on raw materials

Number assignment
Number Assignment is the process of giving each vendor or material a unique ID (number) in SAP. This ID helps the system identify and track vendors or materials easily.
Internal Number Assignment:
SAP generates the number automatically.
Example: When you create a vendor, SAP might assign it a number like 500001.
External Number Assignment:
You manually enter the number while creating the vendor or material.
Example: You might assign a vendor ID like ABC001 if you want a custom format.
MATERIAL MASTER 
Material master is a central repository for managing all the information about the materials like which material is it like raw, finished goods, semi finished  used in company 
Its like master database for handling the details about material to handle effectively across all the material like purchasing, sales, production and inventory 
 that contains all relevant information about materials used within an organization.
While creating material it contains views like 
Basic data,
Purchasing 
Sales 
Mrp 1,2,3,4
Accounting
General based plant data
Transaction code to create material → MM01








Levels of material master 
Data at client level, data at plant level, data at storage location level, company code level 

Mm01 - creating material 
Mm02 → changing material
Mm03 → display material 
Mm04 → display material changes 
Mm06 → delete material master 
Mm17 – mass maintenance 
Mmam – change material type 
Mm11 – schedule creation of material master 
Mm50 → extend material view 
Mm60 – material list 


Purchase info record 
which stores the information between the material and vendor It helps the system remember important details about buying that material from that specific vendor.
Purchasing info record can be created for purchasing related information for the combination of material and vendors 
Inclues 	
Price 
Delivery time 
Quantity details 
It can be maintained at purchasing orgaznition level or plant specific 
When you create the purchase order the system search for info record for purchasing 
Maintained at different proceuremtne type 
Standard 
Consignment 
Subcontracting 
Pipeline 
Price, tax, order unit 
Planned delivery time, tolerance, conference control data
Level of purchase info record 
General data
Purchasing organiztion data
Plant data
PIR can be created automatically from contract
PIR can be updated from outline agreement 
Me11 – manual creation 

Source list 
Used to Vendor (supplier) are  autohrized to supply the specific material adn within the specific period of time. It helpds manages the relationship between the material and vendors by listing the approved vendors. And validity period for vendor and materials 
In source list contains list of material in a particualra plant for particular period 
We have fix or block the source of material and vendor s
Me01 – creation of source list 
Me05 - source list automatic 
Source list is a list of approved vendor for a specific material. It tells which vendor to buy from and which time they will supply the material 
Ensure you to buy material from trusted vendors 
Automatically picks vendor while creating a purchase order or purchase requisition
Types of stocks 
Unrestricted stock 
Quality inspection stock 
Blocked stock 

Business partner 
A Business Partner in SAP is like a contact record that stores all the important information about someone or something your company works with, such as a supplier, customer, or employee.
QUOTA (MEQ1)
Quota is used to split the procurement of material between the different vendors. This helps companies to buy materials from more than one suppliers 
Quota arragement is a master data used for source determination
Quota arrangement helps to manage and distribute the material purchase from different vendors in a controlled manner. It helps to allocate the
In quota arragement we can give quantity and percentage for a vendor . if we maintain many vendor in source list 
Quota rating = quota allocated quantity + quota based quantity / quota 

Pre requisite for quota master 
Material, plant 
Vendor master 
Purchase info record 
Source list 
MEQ1 – creation of quota management  
Material type 
Material type defines that what kind of material are you dealing with and how it should be treated on the system 
Raw material – roh
Semi finished - halb
Finished goods – FERT 
"In SAP MM, Material Types categorize materials into groups like Raw Materials, Finished Goods, or Trading Goods. Each material type defines how the material is treated, including its data fields and the rules for purchasing, storing, or selling it."

Purchasing requisition 
Purchase requisition is a internal document that created by the user or material to request the purchase of materials or service within the organization 
A Purchase Requisition (PR) in SAP MM is a request or an internal document that asks the purchasing department to buy a material or service. It is created when a department or employee needs something, and they need to get approval before making the purchase.


Can be created directly and indirectly 
Purchase requisition can be created for stock or for direct consumption 
Standard
Subcontracting
Consignment
Stock Transfer
External Service


Methods of creating purchase requisition 
Standard
Consignment
Subcontracting 
Stock transfer 
External service 

ME51N - creation of purchase requisition 

RFQ 
RFQ 
An RFQ is a document sent to vendors asking them to provide a quote for supplying specific goods or services. The RFQ includes details like:
Material or service requirements.
Quantities.
Delivery dates.
Any specific terms and conditions.
Vendors respond with their quotations, which the purchasing team evaluates to select the best supplier.
Price comparison is the process of comparing the price from the quotation receievede from the vendors 

Collective number → you can link multiple rfq that belogn together using a collective numebr 

Quotation → vendor response, in which total quantity and delivery date 

Creating rfq – me41

Purchase order 
It is a formal request sent to the vendor to procure goods and services upon agreed terms by the organization 
What you want to buy
How much quantity 
What price 
Delivery details 
After RFQ or PR the purchase department creating po
"A Purchase Order (PO) in SAP MM is a formal document sent to a supplier to order materials or services. It specifies the material, quantity, price, and delivery details, ensuring that both the company and supplier agree on what’s being purchased."
Pre requisite 
Vendor master,  p org, company code, p grps, plant, material, 

1. Manual purchase order: In this case you need to enter all the required details in purchase order.
2. Automatic purchase order: _It can be created with reference to purchase requisition

Me21n → purchase order 
Me25 → suggest to select possible vendor 
Me58, me59, me59n → creation of PO from assigned requisition 
Me21n (stock transfer) → not from vendor but from plants 

Conditions 
Conditions used to represents pricing elements like price, discounts, subcharges, taxes, delivery costs
Conditions can be maintained while creating quotations, info record, outline agreement, po
PB00, PBXX - gross price 
RA01 - discount 
FRA1 - freight 
Gross price → price without any discounts, surcharges in account 
Net price → price taking after discounts and surcharges
Effective price → net price after deduction of cash discount 

Time dependent and time independent 

1. Time-Independent Conditions
These conditions don’t change based on time. The price or discount is fixed, no matter when you make the purchase.
2. Time-Dependent Conditions
These conditions change depending on the time, such as special offers or discounts available only for certain periods.

//////////////
Outline agreement 
Outline agreement is a long term agreement with the vendor regarding the procurement of material or services 
Types 
Contract agreement 
Scheduling agreement 
Long term agreement between the purchase organization and vendor for procurement of material or service 

Feature
Contract
Scheduling Agreement
Delivery Dates
Not fixed; delivery can happen anytime
Delivery dates are specified
Quantity/Value
Defined total quantity or value
Defined total quantity with specific schedules
Use Case
General agreement for future purchases
Specific agreement with detailed delivery plan



 contract
scheduling
ME31K
ME31L
Does not contain delivery schedule 
Contain delivery schedule
We have to make release order 
Quantity, scheduling date ✅
Release order ❌
Goods receipt cannot be done 
After release order goods receiprt can be done 
Po can be created with respect to contract called release orders 
SA acts as release order 
Cannot be created through MRP
Cna be created through MRP


## CONTRACT 
Contract is a long-term agreement with the vendor for the supply of goods and services at specific prices and terms but the exact delivery schedule and quantity is not confirmed at the time of creation. 

Inform material / service quantity 
Types 
Quantity contract 
Value contract 
Distributed contracts
Centrally agreed contracts

Feature
Quantity Contract
Value Contract
Defined by
Total quantity of materials
Total value (money) to be spent
Example
Purchase 1000 Steel Rods over a year
Spend $10,000 on various materials
Flexibility
Allows ordering materials in any quantity
Allows buying materials with total value limit
Usage
Fixed quantity but flexible delivery schedule
Flexible quantity, but total cost is limited



Me31k - create contract
Me32k - change contract
ME33K - display contract
ME35K - approve contract

Quantity Contract: This type specifies a total quantity of materials to be supplied. The contract is fulfilled when the agreed quantity is delivered.
Value Contract: This type specifies a total monetary value for materials or services. The contract is fulfilled when the total value of the orders reaches the agreed amount.


Centrally agreed contract 
A Centrally Agreed Contract is a type of contract that is negotiated and created at the corporate level (central purchasing organization) and made available for use by multiple purchasing organizations or plants.
Distributed contract
A Distributed Contract refers to a contract that is created and replicated across different systems or instances of SAP using SAP Central Procurement or Application Link Enabling (ALE). Distributed contracts are typical in organizations with decentralized procurement systems.0


SCHEDULING AGREEMENT 
The scheduling agreement is also a long-term agreement with the vendor but it also includes the pre-defined delivery schedule for specific quantities and specific dates.
Used to procure material / services based on pre determined dates 
Standard
Consignment 
Subcontracting 
Stock transfer 
Materials are procured on the predetermined dates
Type 
With release documentation 
Without release documentation

With release documentation
Without release documentation
Document type -> LPA
LP






With release documentation 
Release order is created for each delivery. And details of the delivery documented as release 
This release order used to trigger the actual order 
Not directly send to the vendor until user explicitly create scheduling agreement 
Release documentaiton
Without release documentation 
There is no separate release order created 
Scheduling lines created immediately transmitted to vendors
No release documentation 


Release Orders
New purchase orders (release orders) are created for each delivery
No new purchase orders are created


Tracking Deliveries
Each delivery is tracked separately with release documentation
Deliveries are tracked directly through the scheduling agreement


Process Complexity
More formal and detailed, with multiple documents
Simpler, no need for separate release orders


Advantages
Scheduling agreemnet with the vendor is negotiated and entered in the system 
ME31L - shceduling agreement 
Purchase requistuion
RFQ
Other scheduling agreement 
Centerally agreed contracts 



ME31L - create scheduling agreement 
ME32L → change scheduling agreement 
ME33L → display scheduling agreement 
ME35L → approve scheduling agreement 
ME38 → maintain scheduling agreement 

Automatic purchase order 
Auto po is a process of creating purchase order with referecing to purchase requisituoin 
This saves time and reduces the risk during procurement process 
System create purchase based on the requirements like when the stocks are low 
Pre requisite 
Material master 
Vendor master 
Info record 
Source list 
Purchase requistuoin 
Me59n

Source determination
Source determination is a process of finding the right supplier for the materila or service when creating purchasing requisition or purchase order. 
When the company buys something sap helps finding the best supplier through 
Purchase info record 
Source list 
Quota arrangement 
Outlien agreement 
Auotmaticaly picks vendor instead of manual selections 
Use only approved vendors 
Reduce time 
Adopted using bp using quota arrangement 
MRP run
Purchase requisition
Planned order 
Production order 

background job
In SAP MM, a background job is a task or process that runs automatically in the background without user interaction. It’s typically used to perform regular or time-consuming tasks, like report generation, data updates, or stock checks, during off-peak hours.
It will run parallel without any disturbance
It can be run as per user choice 
Reduce manual effort and automate tasks  
Time saving
Repetitive task
Common example background job
MRP run
Stock reports 
Price update 
Document archiving 
How to set background job
Access the job scheduler 
Define job name 
Specify program/task

Set schedule 
Save and activate 

Priority 
Class A (high priority)
Class  B medium priority
Class C low priority
Status of background job 
Scheduled 
Job is planned but not started
Released 
Job is ready to execute and is waiting for its turn in the system 
Ready 
The job is queued and will start shortly
Active 
The job is currently running in background
Finished 
The job completed successfully 
Cancelled 
The job was stopped before compilation due to errors, system issues, manual intervention 



T code: SM36
SPECIAL PROCUREMENT PROCESS 
Special stock is a stock that do not belong to the company as they are not stored in your company or any other particular location
Consignment 
Subcontracing 
Stock transfer 
Third party procurement 
Returnable transport packaging 
Pipeline handling 
Sales order stock 
Project stock 

CONSIGNMENT STOCK
Consignment stock is a type of stock where vendor(supplier) keeps all the goods in our location like organization in which we only have to pay for the amount used them.

STOCK TRANSFER ORDER 
Stock transfer order is used to move materials from one plant to another plant within the same company code



SUBCONTRACTING STOCK 
In this we have to send the raw materials to the vendor, then vendor used to manufacturing the finished product and send the product to the company 


STOCK IN TRANSIT 
In SAP Materials Management (SAP MM), Stock in Transit refers to inventory that is being transferred from one location to another within the company, but which has not yet been received at the destination location. It typically arises during inter-plant stock transfers, or when goods are being transferred from a supplier or warehouse to a plant.

PIPELINE STOCK
Pipeline Stock refers to the stock that is not physically stored in a company's warehouse but is available for use directly from a vendor or supplier's pipeline, such as gas, water, or electricity.

PROJECT STOCK 
Project Stock is a special type of stock in SAP used exclusively for a specific project. It ensures that materials are reserved and only used for that particular project, preventing their use in other operations or sales orders.
It is managed as valuated or on valuated project stock 



RETURNABLE TRANSPORT PACKAGING
Returnable Transport Packaging (RTP) is a special procurement process where reusable packaging materials, such as pallets, containers, crates, or barrels, are sent along with goods. These packaging materials do not belong to the buyer and must be returned to the vendor after use.

THIRD PARTY PROCESSING 
Materials are delivered directly to the customer by your vendor, skipping your warehouse. The sales order not processed by the company but by the vendor 

SALES ORDER STOCK 
Sales Order Stock is a special stock type in SAP that is reserved for a specific sales order. It ensures that the materials procured or produced for a particular customer’s order are exclusively used to fulfill that order, preventing their use for other purposes.










SERVICE MASTER 
The Service Master in SAP MM is a centralized database that stores information about services provided by external vendors or performed internally
Consulting, maintainance, labour 
Services are non-physical and cannot be stored in inventory, so the Service Master helps in managing

After service entry sheet created one or more person responsible can check 
Service entry sheet then approved 
Once the service entry sheet is accepted and posted accounting entries are posted 
Cancel service netry sheet → ML81N


PRICING PROCEDURE 
Pricing procedure is a mechanism used to define the pricing how material or services is determined in purchasing process. 
It determines conditions like discounts, surcharges, taxes, final price during process activities
Pricing procedure is a sequence of condition type in specific order used to calcualte the final price 







Elements in pricing procedure 
Condition
Used to define pricing elements base price, discounts, surcharges, taxes 
PB00: Basic price (the main price for the material)
RA01: Discount
MWST: Sales tax
FRB1: Freight

Gross price: price excluding the discounts and subcharges 
Net price: price taking discounts, surcharges, taxes
Effective price: net price plus delivery cost, cash discounts

Pricing procedure is the process in which how the price was determined for the purchasing document like purchase requisition and RFQ 
It involves various steps on how the price was calculated and has various conditions 


Key components 
Condition types 
Access sequence 
Condition tables 
Calculation schema 
Schema groups 
Schema determination 

Condition types 
Specific types of pricing elements like base price, discounts, taxes, subcharges, PB00, FRA1, RA01

Access sequence 
It contains two or more condition table in which searched and find applicable pricing conditions 

Condition tables 
This table stores the actual condition records that links specific vendors, materials 

Calcaultion schema 
Calculation schema group together various condition type to define how price are calculated 

Schema groups 
Used to categorize the vendor and purchasing organization 

Determiantion process 
Which pricing can be used based on the combination of vendor schema group and purchasing organization schema groups 

PRICE DETERMINATION 
The Price Determination Process in SAP MM (Materials Management) is the mechanism used to calculate the price of materials or services when a purchase order or goods receipt is created. 
Vendor price of a material made up 
Gross price 
Surcharges
Freight
Taxes

Condition table is created to group together fields for which we want to maintain condition record
Assign the condition tables to access sequence
Define condition type and assign access sequence to condition type
Define pricing procedure in calculation schema
Define vendor and purchasing Org. schema
Assign Calculation schema to vendor and purchasing organization schema combination
Maintain condition records in the condition table

Message determination
Message determination is process of generating and send message related to various procurement activities such as order confirmation, purchase order, goods receipt 
This message can be in the form of printouts, emails, or other communication forms 

Key components 
Message type 
Specifies the type of message 
NEU → purchase order message 
ORDER → purchase order 
FAX → fax
MAIL - mail 

Message schema 
The message schema defines the sequence of messages that are triggered during different procurement processes. For example, when a purchase order is created, the schema determines if a message is generated for confirmation or printout.

Message determination procedure 
The message determination procedure is a set of rules that define how messages are determined based on various parameters like document type, message type, and recipient. 

Condition records are the actual data that controls how the message determination will work. These records define details such as:
Who the recipient of the message is (e.g., the vendor).
How the message should be sent (e.g., print, email, fax).
Specific data that should be included in the message (e.g., purchase order details).
Partner Roles
Partner roles are used to define the business partners involved in the procurement process, such as the vendor or purchaser. The message determination procedure uses partner roles to decide who should receive the messages.


NACE — OUTPUT CONTROL
MNO04 — CREATE PO OUTPUT MESSAGE CONDITION RECORD
WE20 — PARTNER PROFILE DEFINITION
WE21 - DOC PORTS
WEO2 —- IDOC DETAILS
MESF — PO MESSAGE OUTPUT

RELEASE STRATEGY
It is a approval process for the purchasing documents like purchase requisition and purchase order. It ensures that the purchases are approved before they are processed.
It ensure the purchasing document is approvred by the right person before they are begin processed

Types
Release strategy with classification
Release strategy without classification 

Key components 
Release code 
Release group 
Release indicator 
Release strategy
Release procedure 






Release code 
Release code represents approval who are responsible for approving the document 

Release group
Set of release code that define group of approvals

Release indicator 
Represents the status of document → blocked or release 

Release strategy 

Release procedure 
Defines how the release strategy is applied to a purchasing document 

Release procedure can be defined 
Purchase requisition 
Po, contract, scheudling agreement, RFQ service entry sheet





Release strategy
Creation of characteritics 
Grouping the characteristics in class 
Defining the release procedure 
Definition of release group 
Definition of release codes 
Definition of release indicator
Creation of release strategies
Defining the release pre requisites 
Specify the release status for each release code 
Classification 
Simulation of releaase strategy

Define characteristics 
Define class 
Define release procedure 
Define release group 
Define release code 
Define release indicator
Define release strategy
Release pre requisites
Release status
Release simulation
Release classification
INVENTORY MANAGEMENT 
Inventory management is a process of tracking and controlling  the movement of goods and services within the company. 
It tracks the quantity and value of a materila 
It ensures the accurate stokc levels 
This module helps manage goods movemnet like goods issue, goods receipt, stock transfer
This managing stocks like consignme
nt, subcontracting, stock transfer order, sales order stock, third party, pipeline, returnable transport packing, project stock 
Key functions of inventory management 
Goods issue 
Goods receipt 
Stock transfer 
Physical inventory 
Stock types 
Quality inspection stock 
Unrestricted stock 
Blocked stock 
Management of stock by value 
Quantity and value 
Account assignment for cost accounting 
G/L account 

GOODS MOVEMENT 
Goods movement refers to the physical and logical movement of material in and out of the inventory 
It includes receiving, issuing, transferring, 

Goods movement is a physcial or logical movement of goods or service leads to changing in stock levels or resulting in consumption of the material 

Goods receipt 
Records the receipt of materials from a vendor 
Increase stock levels in inventory

Goods issue
Records the issue of materials for consumption, sales, or production 
Reduce stock level for inventory 

Stock transfer 
Movement of material from between from one plant to another within the same company 
Stock quantity remain the same but location changes 

Transfer posting 
Logical movement of stock from one status to another 

Movement type 
Each goods movement is associated with movement type (3 digit code)
101 → goods receipt for purchase order 
201 → goods issue for cost center consumption
301 → stock transfer between plants 
309 → transfer posting to change material type 

Movement type
Movement type is a 3 digit code used to identify the goods movement
It helps diffrentiate the various goods movement 

movement type controls many functions:
+ Controls quantity update
+ Stock and value update for material
+ Field selection control for the inventory documents in system
+ Determination of g/l account
+ Printing gi/gr slips

Each movement type can defines the different action in movement of stock 
1** → GR against reference document 
2** → goods issue for consumption
3** / 4** → transfer posting 
5** → goods movement without reference 
6** → goods movement with reference 
7** → physical inventory 

Goods receipt 
Goods receipt is a goods movemnet in which we have post the receipt of goods from a vendor or from production. 
Goods receipt leads to increase in warehouse stock 
All transaction are entered in real time R/3
Stock is updated at real time at the time of posting 
Goods receipt are process against open purchase quantity 
Movement type is a 3 digit key used to identify the goods movement like goods receipt, goods issue, transfer posting 

Planned goods receipt 
Unplanned goods receipt 

Planned goods receipt 
Planned goods receipt is happen when the receipt of materils is tied with 
Purchase order 
Productipon order 
Scheduling agreement 

Unplanned goods receipt
Occurs when the materials are received without any prior documents like po or production order 




Feature
Planned Goods Receipt
Unplanned Goods Receipt
Reference Document
Linked to PO, production, or agreement
No prior document required
Movement Type
Example: 101 for PO receipt
Example: 501 for manual receipt
Automation
System auto-updates inventory and finance
Manual updates required
Use Case
Regular procurement
Emergency or unexpected deliveries



Effects of goods receipt 
Material document created 
Accounting document created 
Stock and value updated in material master 
Po history updated 

Goods receipt stock types 
Unrestricted stock 
Quality inspection stock 
Blocked stock 

Movement Type Description of Movement Type
101 Goods receipt for purchase order or order
103 Goods receipt for purchase order into GR blocked stock
105 Release from GR blocked stock for purchase order
107 Goods Receipt to Valuated Goods Receipt Blocked Stock
109 Goods Receipt from Valuated Goods Receipt Blocked Stock


Reference documents for goods receipt 
Purchase order 
Order 
Reservation
Inbound delivery 
Outbound delivery 
Other 

Financial entries can be posted once the goods receipt is done 
Accounting entries for stock material 
Stock material - material (BSX) - debit 
GR/IR - material (WRX) - credit 

Accounting entries for account assigned PO 
Consumption account - debit 
GR/IR account - credit 

Goods receipt can be created without reference by using option “others”
“Others” used like stock upload, free sample, free goods, free service 

Functions goods receipt without reference document 
Initial entry of inventory data 
External goods receipt without a purchase order 
Internal goods receipt without a production order 
Goods receipt of by products 
Delivery free of charges
Return from customer 

Movement Type Description of Movement ype |
501 Goods receipt without purchase order - unrestricted-use stock
503 Goods receipt without purchase order - stock in quality inspection
505 Goods receipt without purchase order - blocked stock
511 Free-of-charge delivery from vendor
521 Goods receipt without order - unrestricted-use stock
523 Goods receipt without order - stock in quality inspection
561 Initial entry of stock - unrestricted-use stock
563 Initial entry of stock - quality inspection
565 Initial entry of stock - blocked stock


Accounting entries goods receipt without reference 
MT561 - initial stock entry 
Stock account - material (BSX) - debit 
Offsetting entry for stock posting - GBB - credit 

MT501 - GR without purchase order 
Stock account - material (BSX) - debit 
Offsetting entry for stock posting - GBB - credit 

GOODS ISSUE
Records the issue of material like consumption, sales, production order 
Which leads to reduce in stock levels 

Planned goods issue 
In this system automatically created reservation for the components planned in this order 

Unplanned goods issue 
It is determined during production process that an additional material or additional quantity of a component already withdrawn is required for an order 

Goods issue without refernece 
While goods issue without reference we need to manually input detailed such as document date, posting date, material number, quantity, movement types, account assignment, plant, storage location 

Goods issue is posted system create material document

MovementType Desagton
201 Goods issue for a cost center
221 Goods issue for a project
261 Goods issue for an order
281 Goods issue for a network
551 Scrapping from unrestricted-use stock
601 Goods Issue for Delivery (Shipping)
641 Goods issue for a stock transport order (Shipping)
643 Goods issue for a cross-company stock transport order (Shipping)


Results of goods issue posting 
Creation of material document 
Creation of accounting document 
Creation of goods receipt 
Stock update 
Update of GL accounts 
Consumption update 
Reservation update
Order update 



Stock transfer 
‘Stock transfer order is a process of moving materials from one plant to another plant, or storage location within the same company code 
Delivery types 
NL → same company code - intra-company 
NLCC → cross-company code → inter-company

1**------GR against reference document

2**------Goods Issue for consumption

3**/4**-- Transfer Posting

5**------Goods movement without reference

6**---- Goods movement with reference to deliveries ( EX- Stock Transport Order )

7**---  Physical Inventory
 
9**/Y**/Z**-  Custom movement type by referring standard mov type


  STO Levels



  1. Plant to plant transfer within same company code


  2. Plant to plant transfer, both plants belong to different company code


  3. Storage location to storage location stock transfer within same plant
Types 
Unrestricted stock 
Quality inspection stock 
Blocked stock 

Unrestricted stock 
This stock is available and immediate use in production, sales or other operation without any restrictions

 

Quality inspection stock 
This stock is under quality inspection and not available for immediate and unrestricted use 

Blocked stock 
This stock cannot be used for any purpose due to issue like defect or legal restrictions 

Levels 
Company code to company code 
Plant to plant 
Storage location to storage location 

One step procedure 
Stock is transferred from the sending location to the receiving location and inventory updated in both location immediately 

2 step procedure 
Stock movement is recorded in 2 separate steps. 
1 goods are issued from the sending location
2 goods are received at the receiving location 
TRANSFER POSTING 
Transfer posting refers to process of chaging the status, type, location of stock in the sytem without any physical movement. It is a logical movement used to update the inventory records 





Special procurement process 

In standard procurement process the customer purchases material from the vendor, the ordered goods is the property of the customer 

Special stock is a stock that are managed separately because they do not belong to your company or being stored at a particular location 

The goods do not necessarily flow from vendor to the customer 

CONSIGNMENT STOCK
Consignment stock is a type of stock where vendor(supplier) keeps all the goods in our location like organization in which we only have to pay for the amount used them.

STOCK TRANSFER ORDER 
Stock transfer order is used to move materials from one plant to another plant within the same company code

SUBCONTRACTING STOCK 
In this we have to send the raw materials to the vendor, then vendor used to manufacturing the finished product and send the product to the company 




STOCK IN TRANSIT 
Materials that are being transferred from one location to another and are not yet received

PIPELINE STOCK
Pipeline Stock refers to the stock that is not physically stored in a company's warehouse but is available for use directly from a vendor or supplier's pipeline, such as gas, water, or electricity.
Material type PIPE

PROJECT STOCK 
Project Stock is a special type of stock in SAP used exclusively for a specific project. It ensures that materials are reserved and only used for that particular project, preventing their use in other operations or sales orders.


RETURNABLE TRANSPORT PACKAGING
Returnable Transport Packaging (RTP) is a special procurement process where reusable packaging materials, such as pallets, containers, crates, or barrels, are sent along with goods. These packaging materials do not belong to the buyer and must be returned to the vendor after use.
Indicator  M



THIRD PARTY PROCESSING 
Materials are delivered directly to the customer by your vendor, skipping your warehouse. The sales order not processed by the company but by the vendor 

SALES ORDER STOCK 
Sales Order Stock is a special stock type in SAP that is reserved for a specific sales order. It ensures that the materials procured or produced for a particular customer’s order are exclusively used to fulfill that order, preventing their use for other purposes.










Physical inventory 
Physical inventory is a process of counting and verifying the physical stock in a warehouse and comparing it with the stock which is recorded in sap system 
This ensures accurate inventory management by identifying any difference 
Transaction code: MI01
MI01
MMBE
Enter inventory count – Mi04
Post inventory difference - mi07  


Preparation 
Count of delivery 
Inventory check

Preparation 
In this step physical inventory document is created 

Count of delivery 
Inventory is counted and updated in hard copy of physical inventory and transferred to the system 

Inventory check 
The difference between the actual and system count is checked and if the difference is acceptable the posted teh stock in this system 

Types 
Periodic inventory 
Continous inventory 
Cycle counting 

Periodic inventory 
All stocks are counted at specific time 
Cycle counting 
Different stocks counted at different time, based on their importance or movement
MICN
Continuous counting 
Stocks are counted throughout the year during normal operation 

Inventory sampling 
Only a sample of a stock is counted 	
Randomly selected stock are counted 

Periodic inventory sampling 
Continous inventory sampling 



Batch management 
Batch Management is a feature in SAP that allows you to manage and track products in "batches." A batch refers to a group of materials produced or received at the same time, and they are treated as a single unit for storage, tracking, and management.
For example, if you receive 1,000 bottles of a product, all those bottles might be assigned to the same batch number if they were produced at the same time or have the same expiry date. Batch management helps you monitor the quality, location, and shelf life of products, especially in industries like pharmaceuticals, chemicals, or food.
Msc1n -> t code batch

Levels in batch management 
Plant level 
Client 
Material 
Types 
Batch with classification 
Batch without classification 


Logistic invoice verification 
Logistic invoice verification is the process of verifying the invoice received from the vendors 
It ensurest the invoice are correct and in line with purchase order and goods receipt 
It is last step in material procurement process where invoice entered in the system and information is passed to the finance for vendor payment 
We check invoice verification in po history 

If GR based IV is ticked 
The system will compare the PO, GR and invoice document 
Posting of document is mandatory before posting the invoice 

If GR based IV is not ticked
System will compare the PO document and invoice document 
Invoice document can be posted before GR posted 

Each material is maintained in material master with 2 types of price 
Standard price 
Moving average price 

Information of invoice document 
Layout 
Balance 
Simulate 
Hold 
Message 
Transaction
Screen layout 
Basic data 
Po reference 

Credit memo
Credit memo is the correction of documents when there is a overcharge or return of goods to the vendor 

Invoicing plan 
It is tool that automates the creation of invoices for recurring service over a period of time. Instead of posting invoice manually for each payment. The invoice plan defines the schedule and rules for generating invoices 

in invoice plan is a tool that allows you to schedule the dates and amounts for future invoices, even before receiving the actual goods or services. 

Periodic invoice plan
the total value of the purchase order item is invoiced at regular intervals 



Partial invoice plan 
The total value of the item is divided into installments, and invoices are created for each installment on specified dates.

Like rentals 

Partial invoicing plan 
Used when the total payment is split into fixed amounts 
payment made in installment 

Subsequent credit debit 
Are adjustment made to correct teh financial document after invoice posted.
This adjustment are either increase or decrease of cost initial invoice has been processed 
subsequent credit and debit are used to adjust the value of an already posted invoice without affecting the quantity. 
Subsequent Debit: Used to increase the invoice amount due to additional charges like freight, taxes, or handling fees.
Subsequent Credit: Used to decrease the invoice amount due to price adjustments, discounts, or overcharges.

Debit 
Used to increase the total invoice amount after the original invoice posted liek additional cost 

Credit 
Is used to decrease the total invoice amoutn after original invoice posted 

ERS
ERS is a process in which system automatically generated invoice based on the goods receipt for vendor. It eliminates the need of vendor to send invoice manually
Advantages 
Purchasing transaction are closed more quickly 
Communication error are avoided  
There is no price and quantity variance in invoice verification 


Sub topic
ERS must be flagged in the purchase order item 
In vendor master flagged ERS 

Invoice planning 
Invoice planning is used to manage and schedule recurring planned payments for long term agreement and services 
Instead of posting individual invoice for every payment 

Types 
Partial invoice planning 
Periodic invoice planning 


Periodic invoice planning 
The payments are made within the due date 

Partial invoicing planning 
The payments are made with parts 


Valuation class 
Link the material to GL accounts for automatic posting of financial transactions 

Material valuation
Material valuation is link between the material and financial accounting 

Split valuation 
businesses to manage and value different segments of the same material with varying prices within the same valuation area (like a plant or company code)

Material to be managed at different valuation type within the same material number 

Materials procured internally and externally may have different costs.
New stock and old stock may have different values.
Materials from different vendors may have different pricing.


Standard price 
The material has a fixed price maintained in material master. This price does not change 

For finished goods or materials for fixed production cost 


Moving average price 
The material price is calculated dynamically based on the weighted average all receipt 
For raw materials or goods without fixed production cost 

Consumption based planning 
Planning of materials that focuses of past consumption data to determine the future material requirements

AUTOMATIC ACCOUNT DETERMINATION 
It is a process of automatically determines the g/l account during any transaction like goods issue, goods receipt, stock transfer 

Automatic account determination means account automatically determines where there is goods movement takes place 

Valuation area 
It determines at which level materials are valuated 
It is a area where the value and cost of the material is determined 
To maintain multiple price for a single material 

BSX: Inventory Posting (e.g., stock account).
WRX: GR/IR Clearing Account.
GBB: Offset for Inventory Posting (e.g., goods issue, consumption).
PRD: Price Differences.





It automatically picks general ledger account (G/L) during financial posting like 
Goods issue 
Goods receipt 
Invoice posting 

It means you dont need to enter the G/L account manually during transaction happens
It ensures the accuracy 
It saves by automatic repetitive tasks 
Reduce errors 

Valuation class 
It is used to determine which GL accounts are updated during financial transaction involving materials 
Valuation class categorizes based on materials based on accounting 
Each material is associated with specific valuation class 
Raw material → 3000
FERT → 7920
When a transaction occurs, the system checks the valuation class linked to the material to determine which G/L account should be updated. OBYC

////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

Standard material type → ROH, FERT, 
At what level we maintain purchase info order → plant, purchase organization, material, vendor 
Quotation → quotation refers to an offer from a vendor in response to a request for quotation (RFQ). it contains details about price, terms, and conditions for supplying specific materials or services (ME41)
Can we reject quotation YES (ME47)
Centralized purchase organization
Can we assign single plant to multiple company code → YES

Inter-company STO (stock transfer order)  → when the companies are different 
Intra-company STO → when the companies are the same 


Viva: if you want to check manual purchase req or automatic 
Ans: there is a creation indicator at the item details in a contact person if the indicator R there is manual otherwise it is automatic  

Viva: What are the types of procurement
Ans: internal and external


Viva: methods of procurement
Ans: procurement for stock and direct consumption

Viva: at what level physical inventory takes place 
Ans: storage location level 

Viva: purchasing group to organization element 
Ans: no  

What are the types, forms, and times  of procurement
One-time purchase order 
Longer terms contract with the subsequent issue of release order 
Longer terms scheduling agreements and delivery schedules 

Forms of procurement            
One-time purchase order 
Contract and release orders 
Scheduling agreement 

Procurement types
Standard 
Subcontracting 
Consignment 
Stock transfer
External service 

Vendor known → me21n
Vendor unknown → me25
Stock transfer → me21n

Display purchase order → me42
PB00 / PBXX → Gross price 
RA01 → discount 
FRA1 → Freight 








Subcontracting accounting entries 
BSX → finished material stock account – debit 
BSV → change in subcontracting stock → credit 
FRL → subcontracting charges → debit 
WRX → GR IR clearing account → credit
BSX → raw materials stock account → credit
GBB → VBO → consumption 


1. BSX-  finished material stock account-  debit

	2. BSV- change in subcontracting stock- credit

	3. FRL- Subcontracting charges- debit

	4. WRX- GR IR clearing account- credit

	5. BSX- raw material stock account - credit

	6. GBB- VBO- consumption account for components - debit

If you want cancel invoice verification → MR8M

In po based invoice verfi which check box should be unchecked 
Ans: GR based IV


Procuremnet types 
Internal procuremnet 
External procuremnet 

Procurement for stock 
Procurement of stock involves  acquires material for future use 
Characteristics 
Material master 
Goods movement 
Automatic account assignment 
Inventory management 
Procurement for direct consumption 
acquiring materials or services that are intended to be consumed immediately upon receipt, rather than being stored in inventory.



/////////q
Transaction keys 
Plays a crucial role in automatic account determination for various material movement 
 They help the system identify the appropriate General Ledger (G/L) accounts for specific transactions.
BSX - INVENTORY POSTING 
This transaction key is used for all postings to inventory accounts.
Goods receipts: When materials are received into stock, the inventory account is debited using the BSX key.
Goods issues: When materials are issued from stock (e.g., for production or sales), the inventory account is credited using the BSX key.

WRX - GR/IR CLEARING ACCOUNT
This transaction key is used for the Goods Receipt/Invoice Receipt (GR/IR) clearing account.
Goods receipt against a purchase order: When materials are received, the system creates an entry in the GR/IR clearing account. This account acts as a temporary holding account until the corresponding invoice is received.


/////////////////////////

BSX: Inventory Posting - Used for all postings to inventory accounts, including goods receipts, goods issues, and stock adjustments.
WRX: GR/IR Clearing Account - Used for the Goods Receipt/Invoice Receipt (GR/IR) clearing account. This account holds the temporary value of goods received until the invoice is received.
GBB: Goods Issue/Scrapping/Delivery of Goods - Used for the consumption of materials, such as when materials are issued to production or scrapped.
PRD: Price Difference - Used to record price differences that arise when the actual price of a material differs from the standard price.
ZOB: Goods Receipts Without Purchase Orders - Used to record goods receipts when there is no corresponding purchase order, such as in the case of returns or free goods.
VBR: Internal Goods Issues - Used for internal transfers of materials within the organization, such as from one warehouse to another.
VNG: Scrapping/Destruction - Used to record the scrapping or destruction of materials.
VKA: Sales Order Account Assignment - Used for goods issues for sales orders with specific account assignments.
VKP: Project Account Assignment - Used for goods issues for projects with specific account assignments.

QUOTA ARRANGEMENT

Quota arrangement divides the total requirement of material among certain sources of supplies i.e. vendors and then assigns quota to each source.
This particular quota specifies the portion of material that is to be procured from assigned vendor or source.
Source list should exists for that materila 
T code: MEQ1 
Mm02 → purchasing → source list ✅

RT1 HON 
BUCF
SAP Reference IMG → Cross-Application Components → SAP Business Partner → Basic Settings → Number Ranges and Groupings → Define Groupings and Assign Number Ranges.
Number range → &B
