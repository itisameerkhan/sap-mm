## organization structure 

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

## **🟢 EASY LEVEL (1-20)**  
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

## **🟡 MEDIUM LEVEL (21-40)**  

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

## **🔴 HARD LEVEL (41-50)**  

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

