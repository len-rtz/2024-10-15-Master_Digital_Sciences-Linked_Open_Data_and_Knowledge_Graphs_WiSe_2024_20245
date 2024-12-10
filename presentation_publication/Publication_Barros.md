**Author(s): Rafael Barros**
**Date: November 19th 2024**

# Welcome

## RDF and Property Graphs Interoperability: Status and Issues

#### ***Authors:*** Renzo Angles, Harsh Thakkar, Dominik Tomaszuk

#### ***Affiliations:*** Universidad de Talca, University of Bonn, University of Bialystok

---

# Introduction:

 **RDF and Property Graphs:** ​

-   Both are graph-oriented database models. ​
-   RDF uses triples (subject, predicate, object). ​
-   Property Graphs use nodes and edges with properties.

**Objective:**
- Study interoperability between RDF and Property Graph databases.

---

# Types of Interoperability ​

-   **Syntactic Interoperability:**
    -   Data exchange at the level of serialization formats. ​
    
   -   **Semantic Interoperability:**

       -   Common understanding of data meanings.​
-   **Query Interoperability:**
    -   Transforming queries between different query languages.
    
   ---

# RDF Databases

-   **Data Model:**
    -   RDF triples (subject, predicate, object). ​
    -   Visualized as graphs. ​
-   **Schema:**
    -   RDF Schema, OWL, SHACL, ShEx. ​
-   **Query Language:**
    -   SPARQL.
    
   ---

![RDF Data - tuples format](https://s3.amazonaws.com/dev.assets.neo4j.com/wp-content/uploads/20170617195306/RDF-data-Turtle-syntax-1024x581.png)

---

* You can see that the triples are identified by a URI, which is the **subject**. The **predicate** is the name and the **object** will be _Sketches of Spain_, which together is a sequence of triples.

---

### Let's look at how this information is displayed graphically:

![RDF Graph](https://s3.amazonaws.com/dev.assets.neo4j.com/wp-content/uploads/20170617195358/RDF-graph-example-graphconnect-1024x537.png)

---


# Property Graph Databases

-   **Data Model:**
    -   Directed labeled multi-graph with properties. ​
-   **Schema:**
    -   Node types, edge types, integrity constraints. ​
-   **Query Languages:**
    -   No standard; examples include Cypher, PGQL, G-CORE.

---

![Cypher example](https://s3.amazonaws.com/dev.assets.neo4j.com/wp-content/uploads/20170617195506/LPG-data-cypher-1024x519.png)

---


* The **semantics** are the same. There's no standard serialization format or a way of expressing a labeled property graph, but rather a sequence of `CREATE` statements do the job here.

---

### Let's look at how this information is displayed graphically:

![](https://s3.amazonaws.com/dev.assets.neo4j.com/wp-content/uploads/20170617195625/LPG-Graph-Example-graphconnect-1024x533.png)

---


* **Core Difference:** nodes have this internal structure and values of attributes don't represent vertices in the graph.

---

# Syntactic Interoperability

-   **Challenges:**
    -   No standard data format for Property Graphs. ​
    -   Different serialization formats (e.g., Turtle, RDF/XML for RDF). ​
-   **Approaches:**
    -   Textual mappings, intermediate data formats.
  
  ---

# Semantic Interoperability

-   **Challenges:**
    -   Special RDF features (e.g., blank nodes, reification). ​
    -   Partial schemas in RDF. ​
-   **Approaches:**
    -   Data and schema transformation methods. ​
    -   Use of transformation languages (e.g., XSPARQL, RML).

---

# Query Interoperability ​

-   **Challenges:**
    -   Lack of a standard query language for Property Graphs. ​
    -   Different paradigms (declarative vs. imperative). ​
-   **Approaches:**
    -   Tools like Gremlinator for SPARQL to Gremlin translation. ​
    -   Efforts to standardize Property Graph query languages.

---

# Issues and Challenges

-   **Syntactic Interoperability:**
    -   No standard data format for Property Graphs. ​
    -   Differences in serialization formats. ​
-   **Semantic Interoperability:**
    -   RDF features not easily modeled in Property Graphs. ​
    -   Need for schema discovery and transformation. ​
-   **Query Interoperability:**
    -   No standard query language for Property Graphs. ​
    -   Different query paradigms and semantics.

---

# Conclusions

-   **Importance of Interoperability:** ​
    -   Facilitates data exchange, integration, and reuse. ​
-   **Future Directions:**
    -   Standardization of Property Graph data model and query language. ​
    -   Development of robust transformation methods.

---

# Acknowledgments ​

-   **Funding:**
    -   Millennium Institute for Foundational Research on Data. ​
    -   EU H2020 R&I project BOOST4.0. ​
    -   National Science Center, Poland.

---

# References:

* **About 48 written in the Article**

---


# Thank you 

* **Questions?**



















