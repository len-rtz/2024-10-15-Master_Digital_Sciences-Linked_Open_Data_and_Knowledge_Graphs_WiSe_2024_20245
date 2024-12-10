**Author(s): Rafael Barros and Bhagyasha Patil**
**Date: November 5th 2024**


# Welcome

![wikidata](https://diff.wikimedia.org/wp-content/uploads/2024/03/image_acf9c3.png?fit=584%2C600)

---

# Learning Outcomes 

**Context and Meaning, Concepts, Structure,  Applications, Limitations and an example with SPARQL  and  Wikidata**

---

# Context

**Wikidata Environment**
- Before Wikidata, data across Wikimedia projects such as Wikipedia existed in a ***unstructured and decentralized format***;
- **Example:** each wikipedia language version maintained its own datasets for items like birthdates, coodinates and so on;
- **Result**: it leaded to redundancy, inconsistency and bunch of coherence across languages;

**Multi-Language centralized  Data Hub needed**

- The **growing use of linked data in web applications and knowledge graphs** revealed the need for a centralized, ***language-independent***, machine-readable repository;

---

# Purposes

- Wikidata's goal is centralizing data for all Wikimedia projects and freely available for all users for reuse;

- **mission**: make the structured knowledge available for both humans and machines;
- **Core focus:** ***Open Data*** that can be edited by anybody and also reused anywhere;

---

# Concepts
- defining **items** (unit) like people, places and **property** which describes its attibutes and relationships, like 'birth date', 'occupation', 'educated at' etc; 

- **Statements and references**: a combo ( item-property-value ) define a factual information; 

---

# Structure and Model
- same principle as with RDF  based on **triples format** (subject-predicate-object);
- **Example:** 
 ```sparql
 - ASK WHERE {
  dbr:Cologne dbo:country dbr:Germany .
}
```

![order](https://th.bing.com/th/id/R.099b57f2ca635de32f62125d665cc0f8?rik=Y1Du%2fEgBkOw31A&riu=http%3a%2f%2flim.univ-reunion.fr%2fstaff%2ffred%2fEnseignement%2fSW%2fSPARQL-by-example%2fspo-arrow.png&ehk=t%2bd7wD6Wie0rfSDW%2f3TdT93%2fWU4xAro52EYV%2b6mgQtQ%3d&risl=&pid=ImgRaw&r=0)

---

# What is Wikidata?

![Wikidata Concept and LOD](https://www.wikimedia.de/2019/wp-content/uploads/sites/2/2020/06/wikidatat-grafik_jahrebericht_englisch-1440x1002.png)

---

- ***a free, collaborative, multilingual knowledge base.***

- part of the **Wikimedia Foundation** (like Wikipedia - an encyclopedia hosted by Wikimedia  which provides the infrastructure for thousands of global volunteers to create and edit pages).
- Wikidata stores information as structured data in a database.
- the data stored and shared as LOD is discernable by machines and intelligent devices like Alexa, Siri, and others.
- **Link to NLP (see in applications)**: LOD provides structured, semantically rich data, which helps NLP algorithms interpret words and concepts in context;
**Example:** if a virtual assistant like Siri queries a dataset containing LOD, it can retrieve precise information about entities (like people, places, or objects) and their relationships, improving its ability to understand and respond accurately.
 
- **Bullet point:** Central source for structured data that can be used across Wikimedia projects and beyond.

---

# Thinking of Contributing?

 **How to get started?**
- Set up an account
- Basic editing tools

**Types of Contributions**
- Adding new entities
- Editing or updating statements
- Translating labels and descriptions

**Community Guidelines**
- Notability of entities
- Citing reliable sources
- Respecting data accuracy and applications

**Why Contribute?**
- Improve global knowledge

---

# Applications
- **Wikidata** as a training dataset for AI/ML models; 
- **NLP**: Entity Recognition and Machine Translation as linked in the picture shown;

- **chatbots** and **voice assistants** like alexa need entity databases ( well-structured by wikidata );

- **Integration with other platforms** - Knowledge Graph, VIAF and Europeana;

---

# Fields 
- **Healthcare**: medical research databases, linking diseases and treatments;

- **Cultural Heritage**: Museum data, cataloging artifacts;
- **E-Commerce**: Product categorization and recommendation systems;

---

# Others Real-World User Cases

- Digital Libraries and archives
- Cultural and Educational projects
- Academic and scientific research
- Used to populate infoboxes and update articles across languages

---

# Limitations

- **Data quality and vandalism issues due to open editing data**

- **Data management and maintenance in terms of complexity**
- **Multilingual data challenges and need for standardization**

--- 

# Querying Wikidata with SPARQL

![Wikidata  breaking down its content](https://ubc-library-rc.github.io/intro-wiki/content/images/wikidata-data-model.png)

---

The following highlighted SPARQL query retrieves all people who studied at Trinity College:

**?person wdt:P69 wd:Q332342 .**

| wdt| wd|          
|-----------------|-----------------|
| `<property>`        | `<entity>`       | 
|   `<educated at>` | `Trinity College`	|  

---

```sparql
SELECT ?person ?personLabel ?birth_placeLabel ?coodinates
 
WHERE{

  ?person wdt:P69 wd:Q332342 . # all those who studied at Trinity College in Ireland
  
  ?person wdt:P106 wd:Q170790 . # ordered by occupation listed
  ?person wdt:P21 wd:Q6581097 . # male who studied at Trinity College
  ?person wdt:P19 ?birth_place . # place of birth , make sure the name given is at select query on top
  ?birth_place wdt:P625 ?coodinates . # with Label after the name ensure the name of that searched identifier
  
   SERVICE wikibase:label { 
       bd:serviceParam wikibase:language "en" . }
     #service provided by examples on wikidata query service

}
```
--- 

# References
- [Wikidata – Wikimedia Germany](https://www.wikimedia.de/2019/en/themen/wikidata/#:~:text=The%20free%20knowledge%20database%20Wikidata%20is%20the%20largest,data%20sets%20and%20provide%20feedback%20on%20the%20software.)

- [Wikidata Query Service](https://query.wikidata.org/)
- [Much more than a mere technology: A systematic review of Wikidata in libraries - ScienceDirect](https://www.sciencedirect.com/science/article/pii/S0099133321000173)

---

# Conclusion

Thank you for attending our presentation!

---


