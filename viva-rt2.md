## ⭐ organization structure 

The organizational structure in SAP MM (Materials Management) defines how a company is structured for procurement, inventory management, and material planning. It consists of different organizational units

| **Level** | **Description** |
|-----------|---------------|
| **Client** | Highest-level organization, representing a corporate group. |
| **Company Code (CC)** | Legal entity for financial reporting (FI module). |
| **Plant** | Physical location for production, storage, or distribution. |
| **Storage Location (SLoc)** | Subdivision of a plant for material storage. |
| **Purchasing Organization (POrg)** | Responsible for procurement activities. |
| **Purchasing Group (PGrp)** | Group of buyers responsible for procurement. |

---

**client** 

* data  in client may not accessed by another client

* client refers to single group of company

**company code**

* organization unit within the client

* where financial entries are produced 
* Producing its own balance sheets and Profit/loss statements
* Several company codes can be set up within the client
* Company code is defined as 4-digit Alpha numeric key ( e.g. SAP1)

**plant** 

* Is an operating unit, within a Company
Code, mostly defined for Production Center
or Material Requirements Planning or
simply a grouping of several Storage
Locations.

* Is assigned to a company code; many
plants can be assigned to one company
code.

* Is a place where either materials are
produced or goods/services are handled.

* it has own material master data

**Purchasing organization** 

* A purchasing organization is an organization unit which
is responsible for procuring material/Service

* The way in which purchasing organization is assigned to
company codes and plants will determine the
procurement method.

* Purchasing organization can be assigned to either
Company code or Plant based on the business
requirement

**What is a Reference Purchasing Organization?**

A Reference Purchasing Organization is a special type of purchasing organization in SAP MM that allows companies to centralize contract negotiations while enabling multiple purchasing organizations to use the same contract terms for procurement.


**storage location** 

* A storage location is an organizational unit
and Subdivision of a plant.

* Storage location defines a location for
materials.

* Stocks of material can be managed within a
plant in different storage locations for
differentiation

* Storage Location is the lowest organizational
level in MM and it helps to differentiate the
stocks.

* stocks of the material are physcially managed 

* stocks are managed at storage location in quantity level only, not an value basis

* storage location always belongs to plants 

* 4 digit alphanumberic key 

**purchasing group** 

* A purchasing group is an organization unit which is
responsible for procuring a class of materials for internal
units.

* **Responsible for certain type of material or service
procurement**

* Deals with the vendor by monitoring the purchasing
activities

* It is defined as 3 - digit alpha numeric key in the system.

* purchasing group is not directly assigned to purchasing organization

* purchasing group assigned to a maetrial in material master 

Here are **50 SAP MM Organizational Structure questions with answers** categorized into **Easy, Medium, and Hard** levels.

---

**🟢 EASY LEVEL (1-20)**  
1. **What is a Client in SAP MM?**  
   - The **Client** is the highest level in the SAP hierarchy and represents an independent unit with its own data and configuration.

2. **What is the purpose of a Company Code in SAP MM?**  
   - A **Company Code** is the smallest legal entity in SAP FI (Finance) for which financial statements are prepared.

3. **What is a Plant in SAP MM?**  
   - A **Plant** is an organizational unit that represents a manufacturing location, distribution center, or warehouse.

4. **What is a Storage Location used for?**  
   - A **Storage Location** is a subdivision of a Plant where materials are stored.

5. **What is the role of a Purchasing Organization?**  
   - A **Purchasing Organization** is responsible for procurement activities and contract negotiations.

6. **What is a Purchasing Group in SAP MM?**  
   - A **Purchasing Group** represents the buyers responsible for procurement transactions.

7. **Can multiple Plants be assigned to a single Company Code?**  
   - **Yes**, multiple Plants can be assigned to a single Company Code.

8. **How do you define a Plant in SAP MM? (T-Code)**  
   - T-Code: **OX10**

9. **What T-Code is used to assign a Plant to a Company Code?**  
   - T-Code: **OX18**

10. **Can a single Purchasing Organization serve multiple Company Codes?**  
   - **Yes**, if it is a **Cross-Company Code Purchasing Organization**.

11. **What is the highest level in the SAP MM Organizational Structure?**  
   - **Client**

12. **What is the transaction code to define a Storage Location?**  
   - T-Code: **OMMM**

13. **How many Purchasing Groups can be assigned to a Purchasing Organization?**  
   - **Multiple** Purchasing Groups can be assigned.

14. **Can a Plant exist without being assigned to a Company Code?**  
   - **No**, every Plant must be assigned to a Company Code.

15. **What T-Code is used to assign a Purchasing Organization to a Plant?**  
   - T-Code: **OX17**

16. **Can a Storage Location be assigned to multiple Plants?**  
   - **No**, a Storage Location is Plant-specific.

17. **What is the purpose of a Reference Purchasing Organization?**  
   - A **Reference Purchasing Organization** is used for **central contract negotiations** while multiple Purchasing Organizations use the contracts.

18. **What is the transaction code for editing a Plant in SAP MM?**  
   - T-Code: **OX10**

19. **What T-Code is used to create a Purchasing Organization?**  
   - T-Code: **OX08**

20. **What is the default factory calendar assigned at the Plant level?**  
   - The default **Factory Calendar** depends on country-specific working days.

---

 **🟡 MEDIUM LEVEL (21-40)**  

21. **Explain the relationship between Plant and Company Code.**  
   - A **Company Code** can have **multiple Plants**, but a **Plant belongs to only one Company Code**.

22. **Can multiple Storage Locations be assigned to a single Plant?**  
   - **Yes**, multiple Storage Locations can be assigned.

23. **What is the difference between a Standard Purchasing Organization and a Reference Purchasing Organization?**  
   - A **Standard POrg** handles procurement, while a **Reference POrg** only negotiates contracts.

24. **How does a Centralized Purchasing Organization work?**  
   - A single **Purchasing Organization** handles procurement for multiple Company Codes.

25. **Can a Purchasing Organization be assigned to multiple Plants?**  
   - **Yes**, a **Purchasing Organization** can serve multiple Plants.

26. **What is the purpose of a Cross-Company Code Purchasing Organization?**  
   - It allows a **Purchasing Organization** to manage procurement across **multiple Company Codes**.

27. **What are the main data fields required when defining a Plant in SAP MM?**  
   - Plant Name, Address, Factory Calendar, Region, Country Code.

28. **What is the impact of changing the Company Code assignment of a Plant?**  
   - It can impact **accounting, procurement, and inventory management**.

29. **Can a Storage Location exist without a Plant?**  
   - **No**, every Storage Location must belong to a Plant.

30. **How is a Plant linked to Material Master data?**  
   - Through **Plant-Specific Views** in the Material Master.

31. **What are the key tables storing Organizational Structure data in SAP MM?**  
   - **T001W** (Plants), **T024E** (Purchasing Organizations), **T001K** (Company Codes).

32. **How does a Purchasing Organization influence procurement processes?**  
   - It defines **vendor selection, contract terms, and purchasing conditions**.

33. **What happens if a Purchasing Organization is not assigned to a Plant?**  
   - Procurement cannot be carried out at that Plant.

34. **What are the limitations of a Reference Purchasing Organization?**  
   - It cannot directly create Purchase Orders.

35. **How can you check the assignment of a Plant to a Company Code?**  
   - Using T-Code **OX18**.

36. **What is the role of a Factory Calendar in a Plant?**  
   - It defines **working days and holidays** for material planning.

37. **How do you transfer materials between two Storage Locations within the same Plant?**  
   - Using a **Transfer Posting (T-Code: MIGO / MB1B)**.

38. **What is the difference between a Plant-specific POrg and a Company-specific POrg?**  
   - A **Plant-specific POrg** is limited to a Plant, while a **Company-specific POrg** covers multiple Plants in a Company Code.

39. **How do you configure a new Plant in SAP MM?**  
   - Using **OX10** → Assign it to a Company Code in **OX18**.

40. **How does the organizational structure impact the procurement process?**  
   - It defines **who procures, where goods are stored, and how invoices are processed**.

---

 **🔴 HARD LEVEL (41-50)**  

41. **How do you change a Plant assignment without affecting open Purchase Orders?**  
   - Ensure **Purchase Orders are completed or reassigned** before making changes in **OX18**.

42. **Explain how a Cross-Company Code Purchasing Organization affects financial transactions.**  
   - It enables **inter-company procurement** while managing costs at different levels.

43. **What are the real-time scenarios where a Reference Purchasing Organization is useful?**  
   - In **global procurement**, where contracts are negotiated centrally but executed locally.

44. **How can you set up a Global Purchasing Organization for multiple Company Codes?**  
   - Create a **Cross-Company Code POrg** and assign it to multiple Company Codes.

45. **Explain the dependencies between a Plant and a Storage Location in Inventory Management.**  
   - **Storage Locations** are specific to a **Plant**, affecting inventory tracking.

46. **How does the organizational structure in SAP MM integrate with SAP SD and SAP FI?**  
   - **MM → FI**: Stock valuation  
   - **MM → SD**: Stock availability for sales  

47. **How would you approach merging two Plants under one Company Code?**  
   - Transfer materials, update master data, and reassign configurations.

48. **What is the impact of deleting a Storage Location in SAP MM?**  
   - It affects **stock availability and historical transactions**.

49. **What is the relationship between Company Code, Controlling Area, and Plant in SAP?**  
   - A **Company Code** belongs to a **Controlling Area**, and **Plants belong to a Company Code**.

50. **What are the challenges in configuring a new organizational structure in SAP MM for a multinational company?**  
   - Legal compliance, multi-currency handling, and logistics complexity.

---

## ⭐ procurement cycle 


![demo](./photos/1.png)
![demo](./photos/2.png)
![demo](./photos/3.png)
![demo](./photos/4.png)
![demo](./photos/5.png)
![demo](./photos/6.png)
![demo](./photos/7.png)

⭐ **types of procurement** 

* internal 

* external 

---

 **1️⃣ External Procurement**

**External Procurement** involves acquiring goods or services from external vendors or suppliers outside the organization. This is the most common method of procurement and includes the process of sourcing, purchasing, and receiving materials from external sources.

**Key Points in External Procurement**:
- **Source of Supply**: The materials are obtained from third-party vendors or suppliers.
- **Stock Procurement**: The goods are bought and stored in the company's inventory.
- **Consumption-Based Procurement**: The goods are consumed immediately or used directly in production.
- **Subcontracting**: Semi-finished goods are sent to an external supplier for processing, and the finished goods are returned.
- **Third-Party Procurement**: Goods are directly delivered from a vendor to the customer, bypassing the company’s inventory.

---

 **2️⃣ Internal Procurement**

**Internal Procurement** involves moving goods or materials from one plant, warehouse, or storage location to another within the same organization. This is commonly referred to as **Stock Transfer** or **Inter-Plant Transfer**.

 **Key Points in Internal Procurement**:
- **Source of Supply**: The goods are obtained from the organization's own plants or storage locations, not external suppliers.
- **Stock Transfer**: Material is moved from one location to another within the organization.
- **No Purchase Order**: Since the transaction happens within the same organization, there is no need for a formal purchase order.
- **No Vendor Involvement**: No external vendor is involved in the process.
  

---

 **Key Differences Between Internal and External Procurement:**

| Aspect                          | **External Procurement**                                       | **Internal Procurement**                                      |
|----------------------------------|---------------------------------------------------------------|---------------------------------------------------------------|
| **Source of Supply**             | External vendors/suppliers                                   | Internal plants or storage locations                          |
| **Transaction Involvement**      | Involves a purchase order (PO), vendor, and payment process. | Involves stock transfer between locations, no vendor.          |
| **Materials Movement**           | Materials are received from external suppliers into stock.   | Materials are moved between different plants or storage locations. |
| **Procurement Process**          | Full procurement process (PO, GR, Invoice, Payment).         | Simple stock transfer or consignment process.                 |
| **Example**                      | Buying raw materials or finished goods from an external supplier. | Transferring finished goods from one warehouse to another.    |

---

 **Use Cases:**

 **External Procurement**:
- Used when the organization needs materials or services from outside suppliers, such as raw materials, finished goods, or services like consulting.
  
 **Internal Procurement**:
- Used for internal transfers, where materials need to be moved from one location or plant to another within the same organization (e.g., moving raw materials from warehouse A to production plant B).


![demo](./photos/8.png)
![demo](./photos/9.png)

### methods for procurements 

1. procurement for stock

2. procurement for direct consumption 

**procurement for stock** 

* Stock Procurement involves purchasing materials from external vendors and storing them in the company’s inventory or stock. This method is used when the organization wants to maintain control over the materials in stock and keep them available for future use.

key components

* goods receipt

* stock management 
* purchasing order 
* invoice verification 

material must have material master 

**procurement for direct consumoption**

Direct Consumption Procurement (also known as Consumption-Based Procurement) involves purchasing materials or services directly for immediate use or consumption, rather than storing them in inventory. In this method, goods are procured, but they are not stocked—they are directly consumed by production or other operations.

* goods receipt 

* no stock update 

* no stock management 

material may have master 

* one time purchase order

* longer terms contract 

* longer terms scheduling agreement 

### MM integration with other module 

![alt text](./photos/10.png)


**forms of procurement**

* purchase order 

* purchase requisition
* goods receipt 
* invoice verification 
* stock transfer order 
* RFQ

Here are the **answers** to the 50 questions on the **procurement cycle in SAP MM**:

---

 **Easy Questions (1-10)**

1. **What is the first step in the procurement cycle in SAP MM?**
   - The first step is **creating a Purchase Requisition (PR)**.

2. **Which SAP transaction code is used to create a Purchase Order (PO)?**
   - The transaction code is **ME21N**.

3. **What document is created after a Purchase Requisition (PR) is approved in SAP?**
   - After approval, a **Purchase Order (PO)** is created.

4. **What is the role of Goods Receipt (GR) in the procurement cycle?**
   - **Goods Receipt (GR)** is used to record the physical receipt of goods into the inventory.

5. **How do you verify the receipt of materials in the procurement process?**
   - The receipt of materials is verified using the **Goods Receipt (GR)** document.

6. **What is the purpose of a Purchase Order (PO) in the procurement cycle?**
   - A **Purchase Order (PO)** serves as an agreement between the company and the vendor, specifying the details of goods or services to be supplied.

7. **What is the difference between a Purchase Requisition (PR) and a Purchase Order (PO)?**
   - A **PR** is an internal request to procure materials, while a **PO** is a formal external document sent to the vendor.

8. **In which document is the vendor's payment processed after Goods Receipt?**
   - **Invoice Verification (IV)** document is used to process vendor payments.

9. **What is the significance of Invoice Verification (IV) in the procurement cycle?**
   - **Invoice Verification (IV)** ensures that the vendor's invoice matches the Goods Receipt and Purchase Order for accurate payment.

10. **What is the purpose of the 'MIGO' transaction in SAP MM?**
   - The **MIGO** transaction is used to post Goods Receipt (GR), Goods Issue (GI), or Stock Transfers.

---

 **Medium Questions (11-30)**

11. **What is a Stock Transport Order (STO), and when is it used in the procurement cycle?**
   - **STO** is used for transferring materials from one plant to another within the same company code or different company codes.

12. **How does SAP manage external procurement versus internal procurement?**
   - **External procurement** involves ordering from vendors, while **internal procurement** involves transferring materials between plants within the organization.

13. **What is the role of the vendor master record in the procurement process?**
   - The **vendor master record** stores essential information about the vendor, such as payment terms, contact details, and materials supplied.

14. **What document is used for requesting quotations from vendors in SAP MM?**
   - **Request for Quotation (RFQ)** is used to request quotes from vendors.

15. **How can you track the status of a purchase order in SAP?**
   - The status of a **PO** can be tracked using transaction code **ME23N** or by checking the document flow.

16. **Explain the purpose of a framework agreement in SAP MM.**
   - A **framework agreement** is a long-term agreement between the company and vendor, defining the terms for future purchases over a certain period.

17. **What is the difference between a standard Purchase Order and a Scheduling Agreement?**
   - A **Scheduling Agreement** is a type of framework agreement with predefined delivery schedules, whereas a **PO** is for individual purchase transactions.

18. **How does SAP handle partial deliveries in the procurement cycle?**
   - SAP allows **partial deliveries** by updating the **Goods Receipt** for each partial delivery and adjusting the quantity in the PO.

19. **What happens if the quantity of materials received differs from the quantity ordered in SAP MM?**
   - SAP will allow you to post a **partial Goods Receipt** and notify the discrepancies, which can be adjusted during Invoice Verification.

20. **How do you perform the Goods Issue (GI) in SAP when transferring stock between plants?**
   - The **Goods Issue (GI)** is posted using the **MB1B** or **MIGO** transaction code, and the stock is removed from the sending plant.

21. **What is a consignment stock, and how is it handled in the procurement cycle?**
   - **Consignment stock** refers to goods stored in the company's warehouse but owned by the vendor until they are used. It's handled by posting GR without creating a PO.

22. **How is third-party procurement different from regular procurement in SAP MM?**
   - In **third-party procurement**, the vendor ships goods directly to the customer, bypassing the company’s inventory. In regular procurement, the goods are delivered to the company first.

23. **What is the purpose of creating a Purchase Requisition (PR) in SAP MM?**
   - A **Purchase Requisition (PR)** is created to request the purchase of goods or services within the organization.

24. **How do you process a return of goods in SAP MM?**
   - Goods returns can be processed using transaction code **MIR7** for **Invoice Returns** and **MIGO** for **Goods Returns**.

25. **How does SAP handle procurement with a subcontractor in SAP MM?**
   - In subcontracting, materials are sent to a subcontractor for processing. A **Subcontracting PO** is created, and the processed goods are received from the vendor.

26. **What are the key differences between stock procurement and direct consumption procurement?**
   - In **stock procurement**, goods are stored in inventory, while in **direct consumption procurement**, goods are immediately consumed after receipt.

27. **How is invoice verification (IV) different from goods receipt (GR)?**
   - **Goods Receipt (GR)** is the receipt of materials into stock, while **Invoice Verification (IV)** is the matching of the invoice to the GR and PO for payment.

28. **What is the role of the "MB1B" transaction in the procurement cycle?**
   - **MB1B** is used for posting material movements, such as transferring goods between plants or moving goods from stock to consumption.

29. **How can you monitor stock in transit during the procurement cycle?**
   - Stock in transit is monitored by tracking the **stock transport orders (STOs)** and checking the material status in the system.

30. **What is the purpose of maintaining the vendor evaluation system in SAP MM?**
   - The **vendor evaluation system** helps assess vendor performance based on criteria like quality, delivery time, and price, ensuring effective vendor selection.

---

 **Hard Questions (31-50)**

31. **How can you resolve discrepancies between Goods Receipt and Invoice Receipt in SAP MM?**
   - Discrepancies can be resolved by reviewing the PO, Goods Receipt, and Invoice details, adjusting the data, and posting necessary adjustments in the system.

32. **Explain the impact of procurement in SAP on inventory management and financial accounting.**
   - Procurement affects inventory by updating stock levels. It impacts financial accounting by posting financial entries related to the purchase, such as expenses, payables, and inventory value.

33. **How is the purchase order item category determined in SAP MM?**
   - The **item category** is determined based on the type of goods or services being procured, such as standard items, consignment, or subcontracting.

34. **What are the key differences between a stock transfer order (STO) and a purchase order (PO)?**
   - A **STO** is for transferring stock between plants, while a **PO** is for ordering goods from external vendors.

35. **Describe the process of subcontracting in SAP MM and the associated purchase order types.**
   - Subcontracting involves sending materials to a vendor for processing. A **subcontracting PO** is created, and the processed goods are returned from the vendor.

36. **How do you handle the procurement of materials that are not available in stock but need to be procured urgently?**
   - Urgent procurement can be handled by creating an urgent **Purchase Order (PO)** or using **express delivery** methods with specific conditions.

37. **What are the various stock types in SAP MM, and how are they managed during procurement?**
   - Stock types include **Unrestricted Stock**, **Quality Inspection Stock**, and **Blocked Stock**, and each is managed based on goods receipt and stock posting rules.

38. **How does SAP MM handle the procurement process when multiple vendors are involved?**
   - SAP handles multiple vendors by creating multiple POs or RFQs for each vendor and selecting the best vendor based on price, terms, and conditions.

39. **What are the configuration steps for creating a framework agreement in SAP MM?**
   - The configuration steps include defining agreement types, conditions, and vendor details, and setting up the agreement validity period and terms.

40. **Explain how SAP handles different vendor payment terms during procurement.**
   - **Payment terms** are defined in the vendor master record and determine how payments are processed, including discounts and payment due dates.

41. **How is procurement integrated with SAP Financial Accounting (FI) and Controlling (CO)?**
   - Procurement processes are integrated with **FI** for accounting the purchase and invoice transactions, and **CO** for assigning costs to specific cost centers or orders.

42. **How do you manage batch management in SAP MM during the procurement process?**
   - **Batch management** allows tracking of materials by batches. During procurement, batches can be specified in the PO and tracked during receipt and storage.

43. **What is the role of the "MIR7" transaction code in the procurement cycle?**
   - **MIR7** is used for **Invoice Returns** to reverse or adjust invoices when

 the goods returned differ from the original invoice.

44. **How does SAP handle partial payments for vendors in the procurement cycle?**
   - SAP allows partial payments by posting partial invoices or creating separate payment runs for each partial amount.

45. **Explain the impact of tax codes and tax calculation during the procurement cycle in SAP.**
   - **Tax codes** define the tax rates applicable to goods and services during procurement, ensuring accurate tax calculation during Goods Receipt and Invoice Verification.

46. **How do you handle procurement for international vendors in SAP MM?**
   - International procurement involves setting up **foreign vendor master records**, managing currency differences, and considering import duties, taxes, and shipping details.

47. **What are the different types of procurement methods in SAP MM, and how are they configured?**
   - Types include **standard procurement**, **subcontracting**, and **third-party procurement**. Configuration involves defining the procurement type in the material master and vendor setup.

48. **How can you ensure that goods receipts are properly matched with purchase orders and invoices in SAP MM?**
   - This is done using **three-way matching** between the PO, Goods Receipt (GR), and Invoice (IR) to ensure accuracy before posting the final payment.

49. **How is the process of procurement handled when a material is procured for multiple cost centers in SAP?**
   - Materials can be procured for multiple cost centers by distributing the procurement costs across different cost objects during PO creation.

50. **What are the consequences of posting an invoice without the corresponding Goods Receipt in SAP MM?**
   - Posting an invoice without the corresponding **Goods Receipt** will cause discrepancies, leading to errors in stock management, financial accounting, and payment processing.

---

These answers will guide you through various scenarios in the procurement cycle within SAP MM. Let me know if you need further details!

---

## ⭐ Material Master 

The Material Master in SAP MM is a **central repository** of information related to materials that an organization procures, manufactures, or sells. It contains all the key data about materials, which is needed for procurement, production, sales, and other functions in SAP.

**STRUCTURE**

1. basic data 

2. purchasing view 

3. MRP 
4. storage view 
5. accounting view 
6. sales view 

**KEY DATA**

1. material type 

2. material group 
3. base unit of measure 
4. valuation class 
5. price control
6. stock type 

**material master in procurement process**

* procuremnet 

* inventory management 
* valuation and accounting 

**LEVELS**

* client level 

* plant 
* storage location 
---

* List of material → `MM60`

* `MM04` → track changes in material 
* MM06 → deletion of material 
* MM17 → mass maintenance 
* MMAM → change material type 
* MM50 → extend material view 

### ⚡ MRP 


The MRP (Material Requirements Planning) View in the Material Master is crucial for planning and managing material procurement and production. It defines how a material is planned, procured, and replenished in SAP MM.
## ⭐ VENDOR MASTER 

The Vendor Master in SAP MM is a central repository of all vendor-related information required for procurement, invoice processing, and payment transactions. It contains key data that is used across various SAP modules such as Materials Management (MM), Financial Accounting (FI), and Sales & Distribution (SD).

**LEVELS**

* client 

   * Vendor Name and Address
   * Contact Information (Phone, Email, Fax, etc.)
   * Bank Details (Bank Account, IBAN, SWIFT Code, etc.)
   * Tax Information (GST, VAT, PAN, etc.)
Industry Classification

* company code 

   * Reconciliation Account (Links vendor to G/L Accounting in FI)

   * Payment Terms (Cash discounts, due dates, etc.)
   * Dunning Procedures (Overdue payment reminders)
   * Withholding Tax Information
* purchasing organization 

   * Order Currency

   * Terms of Delivery (Incoterms, Freight Conditions, etc.)
   * Partner Functions (Ordering Address, Invoicing Party, etc.)
   * Purchase Order History (Previous transactions, performance evaluation, etc.)


   ### ⚡ **ACCOUNT GROUP** 

   An Account Group in SAP MM is a classification tool used to define the characteristics and number ranges of Vendor Master Records. It determines which fields are mandatory, optional, or hidden when creating a vendor.

 * Controls the number range (internal/external) assigned to vendors.

 *  Defines which fields are required when creating a vendor (e.g., bank details, tax information).
* Determines the type of vendor (e.g., regular supplier, one-time vendor).
* Helps in data consistency by standardizing vendor information across the system

* has control functions 

![ddewe](./photos/11.png)
![ddewe](./photos/12.png)

### ⚡ NUMBER ASSIGNMENT

![ddewe](./photos/13.png)

Define Account Groups: `OBD3`

Assign Number Ranges to Vendor Account Groups: `OBAS`


### ⚡**FIELD SELECTION**

Field Selection in SAP MM controls which fields appear as mandatory, optional, display-only, or hidden when maintaining master data (e.g., Material Master, Vendor Master, Purchasing Documents, etc.).

![frmo](./photos/14.png)

### ⚡ **RENCONCILIATION**

What is a Reconciliation Account?
A Reconciliation Account in SAP is a General Ledger (G/L) account that connects sub-ledgers (e.g., Vendor Accounts in Accounts Payable) to the main ledger (General Ledger - FI module).

🔹 It ensures that all vendor transactions (purchases, invoices, payments) are automatically posted to the correct G/L accounts in Financial Accounting (FI).

🔹 Vendors do not post directly to G/L accounts; instead, they post to vendor sub-ledgers, which in turn update the reconciliation account in FI.

* ✅ Ensures real-time financial integration between MM & FI.

* ✅ Helps in automatic financial posting for vendor transactions.
* ✅ Eliminates the need for manual entries in the General Ledger.
* ✅ Maintains data consistency across FI and MM modules.

1️⃣ A Purchase Order (PO) is created in SAP MM.

2️⃣ A Goods Receipt (GR) is posted, and inventory accounts are updated.

3️⃣ An Invoice is received → The vendor account is credited.

4️⃣ The Reconciliation Account (FI) is updated automatically with the vendor balance.

5️⃣ Vendor Payment is made → The amount is cleared from the Reconciliation Account.

🔹 Example: If a vendor invoice of ₹10,000 is posted, SAP automatically updates:

Vendor Account (Credit ₹10,000) → Sub-ledger
Reconciliation Account (G/L) (Credit ₹10,000) → Main Ledger

![demo](./photos/15.png)

### ⚡ PARTNER ROLES 

In SAP MM (Materials Management), Partner Roles are used to define the different roles that an entity (like a vendor or customer) plays in a business process. These roles help determine the relationship between the business partner (e.g., vendor, customer) and the company in various transactions.

| **Partner Role**       | **Description**                                                                |
|------------------------|--------------------------------------------------------------------------------|
| **VN (Vendor)**         | The main partner in procurement; the entity supplying the goods/services.      |
| **WE (Goods Supplier)** | The partner who delivers goods (could be different from the vendor in some cases). |
| **RE (Payee)**          | The partner receiving payments (often the vendor or an agent).                |
| **OA (Ordering Address)**| The partner who receives the order (can be the vendor or a specific department). |
| **IV (Invoice Address)** | The partner who receives invoices related to the transaction.                |
| **GR (Goods Receipt)**  | The partner associated with goods receipt (not always used in every business scenario). |

---

**CONFIGURATION OF VENDOR MASTER**

* account groups for vendors 

* field selection 
* number assignment 
* levels for vendor data 
* partner roles 

 **1. Different Organization Levels of Vendor Master**

The **Vendor Master** in SAP MM is structured into different levels based on the scope and relevance of the data. The organization levels define where the data will be applicable, ranging from a global level (valid for all company codes) to more specific levels.

The main **organization levels** for vendor master records are:

- **Client Level**: Data at the client level is global and applicable across all company codes. Information such as the **vendor's name** and **address** is maintained at this level.
- **Company Code Level**: Data specific to each company code is maintained at this level. It includes the **vendor’s bank details**, **payment terms**, and **reconciliation accounts**.
- **Purchasing Organization Level**: Data at this level is relevant to procurement activities and includes **partner functions** like **ordering address**, **invoice address**, and **payment terms**.

---

 **2. Significance of Account Group**

The **Account Group** in the vendor master is a crucial element in SAP MM, and its significance lies in:

- **Defining the Number Range**: The account group determines the **number range** for vendor accounts, allowing automatic assignment of vendor account numbers (either internal or external).
- **Controlling Fields**: The account group controls which fields are required, optional, or suppressed when creating or maintaining a vendor master record. Different account groups allow for different sets of required fields based on business needs.
- **Determining Vendor Type**: It helps in categorizing vendors into groups like **external vendors**, **one-time vendors**, and **internal vendors**. The account group helps configure the behavior of the vendor in terms of financial and procurement processes.

---

 **3. Functionality of Partner Functions**

In SAP MM, **Partner Functions** define the different roles a business partner (like a vendor) can play in a transaction. The main functionality of partner functions includes:

- **Role Assignment**: Each partner (vendor) can be assigned multiple roles like **Ordering Address**, **Invoice Address**, **Payee**, **Goods Supplier**, etc. This ensures that the correct party is associated with each part of the process.
- **Transaction Control**: Partner functions control how transactions are handled, such as whether a vendor is used for ordering goods or receiving payments.
- **Flexibility**: They enable flexibility by allowing different partners to handle different parts of the business process (e.g., one partner can be the supplier, another the invoice address).
  
For example, in a **purchase order (PO)**, the **vendor** plays the role of the **ordering address**, but the **invoice address** could be a different entity, allowing separation of responsibilities.

---
 **4. Reconciliation Account and Uses**

A **Reconciliation Account** is a **general ledger (G/L) account** used to aggregate subledger balances from specific vendors. It ensures that transactions are properly reflected in the general ledger for **accounting purposes**.

#### **Uses of Reconciliation Account**:
- **Automatic Posting**: When vendor transactions (like invoices or payments) are posted in the system, the reconciliation account is automatically updated, making financial reporting and analysis easier.
- **Financial Integration**: It links **Material Management (MM)** to **Financial Accounting (FI)**, ensuring that vendor transactions are reflected correctly in the financial statements.
- **Tracking Vendor Balances**: It provides a summary view of all transactions for a vendor in the financial accounts, and it prevents manual updates to the G/L, which reduces errors.

For example, when a vendor’s invoice is posted, the **vendor sub-ledger account** is updated, and the **reconciliation account** in the G/L is also updated automatically.

---

 **5. Different Levels of Vendor Master**

There are **three main levels** in the vendor master record:

- **Client Level**: This level holds **general information** about the vendor such as name, address, and communication data. This data is applicable across all company codes and purchasing organizations.
- **Company Code Level**: Information specific to the company code is maintained at this level, including **payment terms**, **bank details**, and **tax information**.
- **Purchasing Organization Level**: Information relevant to procurement activities is maintained at this level, including **partner functions**, **order data**, and **payment terms** specific to purchasing.

---

**6. Is it Possible to Create Both Internal and External Number Ranges for the Same Vendor Account Group?**

Yes, it is possible to configure both **internal and external number ranges** for the **same vendor account group** in SAP. 

- **Internal Number Range**: SAP automatically assigns numbers to vendor accounts when a vendor is created.
- **External Number Range**: The user manually assigns a number to the vendor when creating the vendor master record.

To create both number ranges for the same account group:

1. **Go to T-Code**: `SPRO` → **IMG** → **Financial Accounting (FI)** → **Accounts Payable** → **Vendor Accounts** → **Define Account Group and Number Range**.
2. Configure **number ranges** for each account group, specifying whether they are **internal** or **external**.

This allows flexibility in managing different types of vendors, especially when dealing with **one-time vendors** or **local/foreign vendors**.

---

 **7. How to Block a Vendor in SAP MM**

Vendors can be blocked at the **vendor master** level to prevent any procurement or payment activities. There are two main types of blocks:

1. **Purchasing Block**: Prevents the vendor from being used in procurement transactions.
2. **Payment Block**: Prevents payments from being made to the vendor.

 **Steps to Block a Vendor**:

1. **Go to T-Code**: `XK02` (Change Vendor) or `MK02` (Change Vendor for Purchasing Organization).
2. Enter the **Vendor Number** and **Company Code**.
3. Navigate to the **Payment Transactions** or **Purchasing Data** tab.
4. Under the **Status** section, set the appropriate block (e.g., **Purchasing Block**, **Payment Block**).
5. **Save** the changes to block the vendor.

By blocking a vendor, you ensure that no further transactions are processed for that vendor until the block is removed.

## ⭐ PURCHASE INFO RECORD 


*  Material Master and Vendor Master Record are used to store material specific information and vendor specific details, respectively.

* Whereas purchasing info record contains information about a specific material and a vendor supplying the
material.
* It can be maintained at purchasing organization level or plant specific, as per the business requirements.
*  The “Purchasing Info record” is used to store the combination a Material and Vendor with the pricing details for
the specific period of time, planned delivery time
* It serves as a source of information for Purchasing.

![demo](./photos/16.png)

**PRE REQUISITE**

* material master 

* vendor master 

---

* price 

* Tax 

* order unit 

* planned delivery time 
* tolerance 
* conference control data

---

* PIR can created from outline agreemnt / quotation , PO

* PIR can be automatically from contract
* PIR can be updated from outline agreement / quotation, PO

**❓ QUESTION**

1. organization level for purchase info record 

* client level

* company code 

* plant 

* purchasing organization 


2. list of ways PIR can be created 

* ME11 - create purchase info record 

* ME51 - mass creation 

* ME1M - automatically 

* via purchase order, contracts


What types of various purchasing information records we maintained in SAP?

* standard 

* consignment 
* subcontracting 
* pipeline 

What are the different organization levels PIR are created?

* client 

* company code 
* plant 
* purchasing organization 

How PIR is useful in procurement?



What are the other options available to create PIR apart from manual PIRcreation?

* automatically from purhcase order or contract 

* ME1M

* mass creation 
* PIR on purchase requisition

## ⭐ SOURCE LIST 

* for some of the materials, there is more than one
source of supply. You can manage these supply sources
using source lists to control how the application-related
supply sources are used.

* Source list specifies the possible sources of supply for a
Material over a given period of time. It shows the time
period in which a material may be ordered from a given
vendor or under a certain long-term purchase
agreement.

* In the source list, you specify which source of supply is
valid for a certain period of time.

* You can specify a preferred source as fixed or MRP-
relevant for a certain period in the source list.

* You can mark an undesired source as blocked.


**Used to Vendor (supplier) are  autohrized to supply the specific material adn within the specific period of time. It helpds manages the relationship between the material and vendors by listing the approved vendors. And validity period for vendor and materials 
In source list contains list of material in a particualra plant for particular period 
We have fix or block the source of material and vendor**

ME01 - creation of source list 

ME05 - automatic source list 

* Source list is a list of approved vendor for a specific material. It tells which vendor to buy from and which time they will supply the material 

* Ensure you to buy material from trusted vendors 
Automatically picks vendor while creating a purchase order or purchase requisition

* contains sources of material and plant for particular time period 

* fixed a source, blocking a source

**FUNCTIONS**

* supplier restriction and vendor selection

* Automatic Source Determination in Purchase Requisitions & Orders

* Mandatory Source List Requirement

* Scheduling Agreements & Contracts Linking

* Vendor Evaluation & Priority Handling

**CREATION**

* **manually**

* **creation from within outline agreement**


**advantages of source list**

1. Streamlined Vendor Selection

2. Automatic Vendor Assignment
3. Prevention of Expired Vendor Contracts
4. Integration with MRP (Material Requirements Planning)
5. Fixed Vendor Assignment
6. Cost Control & Transparency


-------

1. What is use of source list?


The Source List in SAP MM is used to manage and control the vendors authorized to supply a material for a specific plant. It ensures compliance by allowing procurement only from approved sources, automates vendor selection during Purchase Requisition (PR) and Purchase Order (PO) creation, and integrates with Material Requirements Planning (MRP) to select vendors automatically. Additionally, it helps assign Fixed Vendors, restrict unauthorized purchasing, and prevent expired vendor contracts from being used.

2. Is it possible to maintain multiple sources for a plant within same validity period?

Yes, it is possible to maintain multiple vendors for a material at the same plant within the same validity period. SAP allows multiple vendors with defined priority rankings, and one vendor can be marked as Fixed, meaning all procurement should be directed to them. If no vendor is fixed, SAP will consider all eligible vendors during procurement.



3. What are different ways of creation of source list?

The source list can be created in different ways. Manually, it can be created using T-Code ME01 by entering vendor and material details. Automatically, it can be generated using T-Code ME05, which derives data from existing Purchasing Info Records (PIRs) and contracts. Additionally, source lists can be created via PIR integration or during an MRP run, where SAP selects vendors based on pre-defined procurement rules.

## ⭐ QUOTA ARANGEMENT 


Quota Arrangement is a mechanism in SAP MM that helps distribute procurement requirements among multiple vendors based on predefined percentages. It ensures that a company sources materials from different suppliers in a structured and controlled manner.

**KEY FEATURES**

**Key Features of Quota Arrangement**  
1. **Vendor Allocation** – Assigns a specific percentage of procurement to each vendor.  
2. **Automatic Vendor Selection** – When creating a Purchase Requisition (PR) or Purchase Order (PO), SAP selects the vendor automatically based on quota percentages.  
3. **Quota Splitting** – If multiple vendors exist, SAP distributes the total procurement requirement based on the quota percentage.  
4. **Quota Arrangement Usage Period** – Defined start and end dates to control the validity of quota allocation.  
5. **Quota Calculation** – Based on past procurement quantities and assigned quota percentages.  


**quota arrangement is tool for source administrration**

![demo](./photos/17.png)

* quota with the lowest quota rating represents the valid source 

### ⚡ QUOTA RATING 

Quota Rating is a calculated value that helps to determine which vendor will be selected first when there are multiple vendors assigned to the same material in the Quota Arrangement. **The vendor with the lowest quota rating will be selected first for fulfilling procurement requirements.**

## ⭐ MATERIAL TYPE 

It defines how materials are managed, procured, and processed within the system. Each material type has specific attributes, controls, and functionalities associated with it, such as procurement method, valuation class, and inventory management.


| **Material Type**    | **Description**                                               | **Example**                        |
|----------------------|---------------------------------------------------------------|------------------------------------|
| **ROH (Raw Materials)**  | Materials procured externally for production.                | Steel, Plastic                    |
| **HALB (Semi-Finished Goods)** | Materials produced in-house or externally, processed further in production. | Assembled parts, intermediate products |
| **FERT (Finished Goods)**  | Final products produced in-house, ready for sale.            | Cars, Mobile Phones               |
| **VERP (Packaging)**  | Materials used for packaging products.                       | Boxes, Plastic wraps              |
| **HIBE (Hazardous)**  | Materials with hazardous properties.                         | Chemicals, Gases                  |
| **ERSA (Spare Parts)**  | Materials for maintenance and repair of machinery.           | Machine parts, Tools              |
| **SERN (Serialized)**  | Materials requiring serial number tracking.                  | Electronics, Machines             |
| **DIEN (Services)**    | Non-material items representing services.                    | Consulting, Maintenance           |
| **CONS (Consumables)** | Materials used up during operations, not tracked individually. | Office supplies, Lubricants       |
| **NES (Non-Stock)**   | Materials not managed in inventory, used immediately.        | Small tools, One-time materials   |
| **UNBW (Non-Valuated)** | Materials without valuation or stock management.             | Consumables expensed immediately  |
| **BES (Services w/ PO)** | Services provided via Purchase Order.                       | Subcontracting services           |
| **ZMAT (Custom Materials)** | Custom-defined materials for specific needs.               | Tailored materials                |
| **MB01 (Material Stock)**  | Materials in stock, can be issued for consumption.          |                                    |
| **MISC (Miscellaneous)**  | General category for materials not falling under other types. | Miscellaneous items               |
| **MRO (Maintenance, Repair, Overhaul)** | Materials used for maintenance, repair, and overhaul processes. | Maintenance parts                 |
| **EMP (Employee-Related)** | Materials related to employee consumption.                  | Uniforms, Work shoes              |


## ⭐ PURCHASE REQUISITION 

A Purchase Requisition (PR) in SAP MM is an internal document used to request the procurement of materials or services. It acts as the first step in the procurement cycle and is used to inform the purchasing department about the need for materials or services.

**METHODS**

* direct 

* indirect 

automatically from 

In MRP

With maintenance orders


With production orders

With networks

![demo](./photos/18.png)

Standard

Subcontracting

Consignment

Stock Transfer

External Service


## ⭐ RFQ

An RFQ is a document sent to vendors asking them to provide a quote for supplying specific goods or services. The RFQ includes details like:

1. Material or service requirements.

2. Quantities.
3. Delivery dates.
4. Any specific terms and conditions.

Vendors respond with their quotations, which the purchasing team evaluates to select the best supplier.


Collective number is unique number to link several RFQ’s 
Length → 10 

Different RFQ can be linked with → collective number 

## ⭐ PURCHASE ORDER 

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

![demo](./photos/19.png)
![demo](./photos/20.png)

Standard Item categories
* Standard

* Subcontracting
* Third Party
* Consignment
* Stock Transport Order

### ⚡ Document Type in Purchase Order (PO) in SAP MM

In SAP MM, a Document Type in a Purchase Order (PO) defines the purpose, control parameters, and number range for different types of purchase orders. It helps in classifying and managing procurement documents effectively.

**Key Functions of PO Document Types:**

* Controls Number Range: 

* Determines Field Selection: 

* Manages Workflow & Approvals:

## ⭐ ACCOUNT ASSIGNMENT 

 **What is Account Assignment in SAP MM?**  
**Account Assignment** in SAP MM is the process of linking a **Purchase Order (PO), Purchase Requisition (PR), or Goods Receipt (GR)** to a **specific cost object** such as a cost center, project, asset, or sales order. It determines how the cost of the purchased material or service is allocated in financial accounting.  

---

 **Why is Account Assignment Required?**  
- It is required when purchasing **non-stock materials or services**, which are not stored in inventory but consumed directly.  
- It ensures proper tracking of expenses and cost allocation in **FI (Financial Accounting) and CO (Controlling) modules**.  

---

**Types of Account Assignment Categories in SAP MM:**  

| **Account Assignment Category** | **Description** | **Example Usage** |
|--------------------------------|----------------|------------------|
| **K (Cost Center)** | Costs are charged to a **Cost Center**. | Office supplies, stationary, utilities. |
| **F (Order)** | Costs are assigned to an **Internal Order**. | Temporary projects, events. |
| **P (Project/WBS Element)** | Costs are assigned to a **Project (WBS Element)**. | Construction, IT projects. |
| **A (Asset)** | Costs are booked to an **Asset** in Asset Accounting. | Machinery, vehicles. |
| **C (Sales Order)** | Costs are linked to a **Sales Order** in SD. | Customer-specific purchases. |
| **M (Material)** | Costs are charged to **Material** stock. | Inventory procurement. |
| **Q (Project Stock)** | Costs are booked to **Project Stock**. | Raw materials for specific projects. |
| **U (Unknown)** | Used when account assignment is **not yet determined**. | Temporary usage. |

---

 **Where is Account Assignment Used?**  
- **Purchase Requisition (PR)**
- **Purchase Order (PO)**
- **Service Entry Sheets (SES)**
- **Goods Receipts (GR)**
- **Invoice Verification (MIRO)**  





* **When GR is done for the PO item, stock will not increase in the system, but it will be directly consumed against the cost object.**

![demo](./photos/21.png)

## ⭐ CONDITIONS 

![demo](./photos/22.png)

Conditions used to represents pricing elements like price, discounts, subcharges, taxes, delivery costs

Conditions can be maintained while creating quotations, info record, outline agreement, po

* PB00, PBXX - gross price 

* RA01 - discount 
* FRA1 - freight 


* Gross price → price without any discounts, surcharges in account 

* Net price → price taking after discounts and surcharges

* Effective price → net price after deduction of cash discount 


**1. Time-Independent Conditions**

These conditions don’t change based on time. The price or discount is fixed, no matter when you make the purchase.

**2. Time-Dependent Conditions**

These conditions change depending on the time, such as special offers or discounts available only for certain periods.

## ⭐ OUTLINE AGREEMENT 

Outline agreement 
Outline agreement is a long term agreement with the vendor regarding the procurement of material or services 
Types 

Contract agreement 

Scheduling agreement 

Long term agreement between the purchase organization and vendor for procurement of material or service 

In **SAP MM (Materials Management)**, an **Outline Agreement** is a long-term purchasing arrangement between a company and a vendor. It is used to streamline procurement by pre-defining terms and conditions for future transactions. There are two main types of outline agreements in SAP MM:

 **1. Contract (T-Code: ME31K)**
   - A **contract** is a formal agreement with a vendor that specifies the terms of procurement but does not contain detailed delivery schedules.
   - It defines **quantity-based** or **value-based** agreements.
   - The actual procurement is done using **release orders (Purchase Orders, T-Code: ME21N)** referencing the contract.
   - **Types of Contracts:**
     - **Quantity Contract (MK)** → The total quantity of materials is fixed, and release orders are created until the quantity is fulfilled.
     - **Value Contract (WK)** → The total contract value is fixed, and release orders can be created until the value is exhausted.

 **2. Scheduling Agreement (T-Code: ME31L)**
   - A **scheduling agreement** is a long-term agreement with a vendor that includes **specific delivery schedules**.
   - Unlike contracts, the delivery dates and quantities are predefined in the system.
   - Scheduling agreements **automatically generate** delivery schedules based on requirements.
   - **Types of Scheduling Agreements:**
     - **Without Release Documentation** → The system directly sends the scheduling lines to the vendor.
     - **With Release Documentation** → A formal release (forecast or JIT) is required before the vendor proceeds with delivery.


![demo](./photos/23.png)

* manually

* with reference to other documents 

   * purchase requisition 

   * RFQ's / quotation 

   * other contracts


## ⭐ SOURCE DETERMINATION 

Source determination is a process of finding the right supplier for the materila or service when creating purchasing requisition or purchase order. 

When the company buys something sap helps finding the best supplier through 

* Purchase info record 

* Source list 
* Quota arrangement 
* Outlien agreement 

Auotmaticaly picks vendor instead of manual selections 

* Use only approved vendors 

* Reduce time 

Adopted using bp using quota arrangement 

* MRP run

* Purchase requisition
* Planned order 
* Production order 

## ⭐ BACKGROUND JOB 

In SAP MM, a background job is a task or process that runs automatically in the background without user interaction. It’s typically used to perform regular or time-consuming tasks, like report generation, data updates, or stock checks, during off-peak hours.

* It will run parallel without any disturbance

* It can be run as per user choice 
* Reduce manual effort and automate tasks  

* Time saving
* Repetitive task

Common example background job

* MRP run

* Stock reports 

* Price update 
* Document archiving 

How to set background job

* Access the job scheduler 

* Define job name 
* Specify program/task

* Set schedule 
* Save and activate 


Priority 
* Class A (high priority)

* Class  B medium priority
* Class C low priority

Status of background job 

* Scheduled 

   * Job is planned but not started

* Released 
   * Job is ready to execute and is waiting for its turn in the system 
* Ready 
   * The job is queued and will start shortly
* Active 
   * The job is currently running in background
* Finished 
   * The job completed successfully 
* Cancelled 
   * The job was stopped before compilation due to errors, system issues, manual intervention 


## ⭐ SPEICAL PROCUREMENT PROCESS 

SPECIAL PROCUREMENT PROCESS 
Special stock is a stock that do not belong to the company as they are not stored in your company or any other particular location

* Consignment 

* Subcontracing 
* Stock transfer 
* Third party procurement 
* Returnable transport packaging 
* Pipeline handling 
* Sales order stock 
* Project stock 

**CONSIGNMENT STOCK**

Consignment stock is a type of stock where vendor(supplier) keeps all the goods in our location like organization in which we only have to pay for the amount used them.

**STOCK TRANSFER ORDER**

Stock transfer order is used to move materials from one plant to another plant within the same company code



**SUBCONTRACTING STOCK**

In this we have to send the raw materials to the vendor, then vendor used to manufacturing the finished product and send the product to the company 


**STOCK IN TRANSIT**

In SAP Materials Management (SAP MM), Stock in Transit refers to inventory that is being transferred from one location to another within the company, but which has not yet been received at the destination location. It typically arises during inter-plant stock transfers, or when goods are being transferred from a supplier or warehouse to a plant.

**PIPELINE STOCK**

Pipeline Stock refers to the stock that is not physically stored in a company's warehouse but is available for use directly from a vendor or supplier's pipeline, such as gas, water, or electricity.

**PROJECT STOCK**

Project Stock is a special type of stock in SAP used exclusively for a specific project. It ensures that materials are reserved and only used for that particular project, preventing their use in other operations or sales orders.

It is managed as valuated or on valuated project stock 



**RETURNABLE TRANSPORT PACKAGING**

Returnable Transport Packaging (RTP) is a special procurement process where reusable packaging materials, such as pallets, containers, crates, or barrels, are sent along with goods. These packaging materials do not belong to the buyer and must be returned to the vendor after use.

**THIRD PARTY PROCESSING**

Materials are delivered directly to the customer by your vendor, skipping your warehouse. The sales order not processed by the company but by the vendor 

**SALES ORDER STOCK**

Sales Order Stock is a special stock type in SAP that is reserved for a specific sales order. It ensures that the materials procured or produced for a particular customer’s order are exclusively used to fulfill that order, preventing their use for other purposes.



| **Special Procurement Type** | **Description** |
|-----------------------------|---------------|
| **Consignment (K)** | The material is stored at the company's location but remains the vendor’s property until used. Payment is made only when consumed. |
| **Subcontracting (L)** | Raw materials are sent to a subcontractor, who processes them and delivers the finished product back. |
| **Stock Transfer (U)** | Transfer of material between plants within the same company code or different company codes. |
| **Third-Party Processing (X)** | Material is delivered directly from the vendor to the customer without passing through the company. Used in **drop shipping** scenarios. |
| **Returnable Transport Packaging (RTP) (M)** | The supplier delivers materials in returnable packaging, which is sent back after use. |
| **Pipeline (P)** | Materials such as gas, water, or electricity are supplied through pipelines or cables, with consumption-based invoicing. |
| **By-Product (O)** | A secondary product obtained during the manufacturing of another material. |
| **External Processing (E)** | Part of the manufacturing process is outsourced to an external vendor. |
| **Vendor Managed Inventory (VMI)** | The vendor monitors stock levels and replenishes materials automatically. |


![de](./photos/24.png)

## ⭐ SERVICE MASTER 

The Service Master in SAP MM is a central repository that stores details about external services procured by a company, such as consulting, maintenance, repairs, or transportation. Unlike material master, which deals with physical goods, service master records are used to manage non-stock services efficiently.

**Purpose**: The service master record counts as part of the master data within External Services
Management and serves as a source of data for you to draw upon when creating service specifications.
Structure: A service master record contains the following principal information for the unique description
of a service:

* Service number

* Service category

* Descriptive texts (short and long text)

* Base unit of measurement

* Material/service group

* Valuation class

## ⭐ PRICING PROCEDURE 

calculation of cost and price mentioned in purchase order based on condition which are mentioned by the suppliers

* Standard type of condition types 

* Gross price 
* Discount 
* Freight / delivery cost
* Surcharges 
* Taxes 
* Insurance 

**Gross price**: price excluding the discounts and subcharges 

**Net price**: price taking discounts, surcharges, taxes

**Effective price**: net price plus delivery cost, cash discounts


A vendor’s price of a material is made up of different components:

* Gross Price

* Surcharge
* Freight Cost
* Taxes

**PRICE DETERMINATION PROCESS**

* Condition table is created to group together fields for which we want to maintain condition record

* Assign the condition tables to access sequence

* Define condition type and assign access sequence to condition type

* Define pricing procedure in calculation schema

* Define vendor and purchasing Org. schema

* Assign Calculation schema to vendor and purchasing organization schema combination

* Maintain condition records in the condition table


### ⚡ CONDITION TABLE


## ⭐ MESSAGE DETERMINATION 