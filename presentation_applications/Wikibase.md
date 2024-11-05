% WikiBase (+ Wikibase Cloud)

# What is WikiBase?

### Bullet points

- Wikibase is a free and open-source software suite
- Enables creation and management of open knowledge bases
- Maintained by Wikimedia Deutschland and a global community
- Suitable for institutions and research projects needing structured data

### How big is Wikidata?
More than 114,000,000 items created and managed by community effort

### Who edits Wikidata?
There are currently 24,526 active users

---

# Wikibase Examples

![](areas.png)

![Wikibase Examples](wikibase_examlpes.png){ width=400px }


---

# WikiBase Infrastructure

![Wikibase Structure](wikibase_structure.png){ width=350px }


---

# Data Modeling

- Modeling is a series of choices about how to organize your data, and those choices look different based on data
- Changing models may require significant data restructuring
- In Wikibase, you'll need to think of your data in terms of the concepts Wikibase uses to store data: **items, properties, statements**, and so forth.

![](Data-modeling-jimmy-wales-item-example.png){ width=280px }


---

# Different Modeling Options

More properties, or more items? 

![](Data-modeling-more-properties.png){ width=200px } ![](Data-modeling-more-items.png){ width=200px }


---

# Data Creation

- **Need to import a large amount of data**
  - **OpenRefine** is for transforming and reconciling data for import
  - **WikibaseIntegrator** is a good choice if you know Python and want to automate data import

- **Need to keep external data in sync with Wikibase**
  - **OpenRefine** connects to various data stores, allowing for ongoing reconciliation with Wikibase

- **Want to input data manually with structured fields**
  - **Cradle** Ensures all required fields are filled when entering data manually

- **Need to import data from a flat text file**
  - **QuickStatements** accepts batch data in command formats (v1, CSV)

---

# Tool Overviews

- **OpenRefine** - a data-wrangling tool that connects to Wikibase and other databases. It allows transformation and mapping for import and ongoing reconciliation

- **WikibaseIntegrator** is a python library for automated data import. It is useful for creating bots to handle large imports with minimal intervention

- **Cradle** is useful for Wikibase administrators who wish to allow creation of lots of items manually, all of which need to conform to a particular schema.


---

# Tool Overviews

- **QuickStatements** supports v1 command format and CSV format.  Accessible via QuickStatements interface in Wikibase

![](example_csv.png){ width=300px }

![](Quickstatements-v1-command.png){ width=280px }

# Wikibase Cloud

Wikibase.cloud is a cloud-based platform developed by Wikimedia Deutschland that allows users to create and manage their own instances of Wikibase without the need for self-hosting.

It offers a user-friendly environment for building collaborative knowledge bases, leveraging the same software that powers Wikidata.

## Wikibase Documentation and Creating a Wikibase

Within Wikibase.cloud website you can register for creating Wikibases and find the documentation about data modelling, creating and deleting data, importing data, and many other things.

![image.png](attachment:45306efc-1628-483a-bce5-44ef3417c3a2.png)

<br>
<br>
<br>


## **Wikibase.cloud allows up to 6 free Wikibase instances**


<br>
<br>
<br>

![image.png](attachment:4bc2357b-04a7-41e0-ba8d-daab70b1e2e1.png)

<br>
<br>
<br>

## **Choosing the name and the domain** 
![image.png](attachment:f995488d-d675-4c10-8265-2496cd67fbc6.png)


<br>
<br>
<br>

## **Wikibase settings**

![image.png](attachment:e0c1ce14-f425-42b8-aa6b-d81f9e94746d.png)

## Wikibase homepage
![image.png](attachment:c55c171b-bec9-4f8f-8772-e9cdbf03df2c.png)
