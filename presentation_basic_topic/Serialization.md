% RDF Serialization
% Kseniia Blokhina
% 29/10/2024

# RDF
## Overview

- RDF (Resource Description Framework) allows us to specify graphs that are:
  - Directed (edges have a source and target)
  - Edge-labelled (each edge has one label)
  - A restricted form of multi-graphs (multiple edges can exist between the same vertices with different labels)

## Graphs
- Graphs can be represented in various concrete ways, including graphical diagrams.
- Machines require an RDF serialization to interpret graphs, which allows storing and transmitting triples in a file.

---

# Serializing Graphs

Numerous syntactic formats are available for RDF serialization:

- **N-Triples** - simple, line-based format

- **Turtle** - adds convenient abbreviations to N-Triples

- **JSON-LD** - encodes RDF graphs in JSON

- **XML** - encodes RDF graphs in XML

- **RDFa** - embeds RDF graphs into HTML

---

# N-Triples Basics

- **N-Triples** represent each RDF triple with:
  - Subject
  - Predicate
  - Object
- **Syntax**: Triple statements are separated by whitespace and terminated by a dot ('.') after each triple.

Example:
![Code Snippet 1](code_snippet1.png)

---

# N-Triples: IRIs and Literals

## IRIs
- In N-Triples, IRIs (Internationalized Resource Identifiers) must be written as absolute IRIs.
- They are enclosed in `< >` and may contain numeric escape sequences.

## RDF Literals
- Literals are used to identify values, such as strings, numbers, and dates.
- Syntax includes:
  - A lexical form (the actual string value).
  - An optional language tag (preceded by @).
  - An optional datatype IRI (preceded by ^^).
  - Blank nodes are expressed with _: followed by a label (e.g., _ :alice).

---

# N-Triples: Example

![Code Snippet 2](code_snippet2.png)

---

# N-Triples: Example

![RDF Graph 1](serialization_rdf_graph.png)

---

# Turtle Serialization

## Features
- Prefix declarations and base namespaces allow shortening IRIs.
- Blank nodes can be encoded with square brackets, allowing in-line predicate-object pairs.
- Easy to parse and straightforward for humans to read.

Unfortunately, it's quite costly to parse compared to N-Triples.

## Syntax
- Numbers can be written directly without using quotes or specifying types, as they are automatically treated as default types like integer, decimal, or double.
- Booleans can also be written as true or false directly

---

# Turtle: Example

- If two triples share both the same subject and predicate, the two objects can be separated by commas

![Code Snippet 3](code_snippet6.png)

---

# Turtle: Example

- If several triples share the same subject, the predicates and objects can be listed, separated by semicolons

![Code Snippet 4](code_snippet5.png)

---

# Turtle: Example

![RDF Graph 2](serialization_rdf_graph_2.png)

---

# XML Serialization
RDF/XML is the oldest RDF serialization format, initially chosen due to widespread XML support.

**Challenges**: Blends XML's tree structure with RDF's graph model, making it verbose and hard to understand.

### Primary Components:
- **Graph nodes**: rdf:Description
  - rdf:about attribute can be added if the node is an IRI
- **Predicate arcs** are nested within nodes: ex:editor

---

# Multiple Property

### Example

![Code Snippet 4](code_snippet3.png)

---

# ... to abbreviation

![Code Snippet 5](code_snippet4.png)

---

# ... to abbreviation

![RDF Graph 3](serialization_figure.png)

---

# More abbreviations

- When a predicate arc in an RDF graph points to an object node which has no further predicate arcs this form can be shortened

- When a property element's content is string literal, it may be possible to use it as an XML attribute on the containing node element.

![Abbreviations](serialization_abbreviations.png)


---

# RDFa

- RDFa (RDF in Attributes) - an HTML embedding of RDF triples; used for HTML document annotations (e.g., with schema.org)
  - By adding attributes to HTML elements, you can give semantic context to the content inside your webpages
- Mostly used by web crawlers (e.g., Google) to enhance search previews.

---

# How RDFa Works

It combines RDF with view data (HTML)

### Example

![Code Snippet 6](code_snippet7.png)

---

# Usage

Use RDFa if you want to add lightweight RDF support to existing HTML rather than full RDF compatibility

  - **But**: It makes HTML documents larger and harder to manage.

For higher data volumes or ease of use, consider JSON-LD or N-Triples

---

# JSON-LD

### What is JSON-LD?
- JSON-LD is an extension of JSON, widely used in web applications.

- It's fully compatible with JSON, allowing easy integration with existing JSON APIs. Ideal for RESTful JSON APIs where RDF parsing performance is not critical.

### How it Works:
- Converts JSON data into RDF by adding an @context object to map keys to RDF Classes and Properties.

---

# Example

![Code Snippet 7](code_snippet8.png)

---

# Bonus Method

## HDT

- HDT is both a compact data structure and a binary serialization format for RDF.
- it's designed to save space and bandwidth.

### Key Features

- Highly Efficient
- Built-in Indexing
- HDT compression is resource-intensive

![Total time](serialization_totaltime.png)

More:
https://www.rdfhdt.org/what-is-hdt/

---

# Thank you for your attention!

### Sources
1. https://iccl.inf.tu-dresden.de/w/images/d/d2/KG2020-Lecture-02-overlay.pdf
2. https://heardlibrary.github.io/digital-scholarship/lod/serialization/
3. https://www.w3.org/TR/turtle/
4. https://ontola.io/blog/rdf-serialization-formats
6. https://www.w3.org/TR/rdf-syntax-grammar/
7. Martínez-Prieto, Miguel A., Mario Arias Gallego, and Javier D. Fernández. "Exchange and consumption of huge RDF data." The Semantic Web: Research and Applications: 9th Extended Semantic Web Conference, ESWC 2012, Heraklion, Crete, Greece, May 27-31, 2012. Proceedings 9. Springer Berlin Heidelberg, 2012.