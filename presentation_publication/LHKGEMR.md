% Learning a Health Knowledge Graph from Electronic Medical Records
% Ole Berg
% November 19, 2024

# Table of Contents

1. Motivation and earlier work
2. Goal and methods
3. Structure of Schema.org
4. Real-world examples
5. Limitations and criticism of Schema.org
6. Conclusion
7. Sources

---

# 1 Motivation and earlier work

* Demand for decision support systems in clinical settings

* Existing knowledge bases created manually or *"using simple pairwise statistics"* [1, p. 1]

* E. g. 15 person-years needed for *Internist-1/QMR* knowledge base

* Manually developed systems very brittle and difficult to extend

* Automatic compilation speeds up development of KBs

* *WatsonPath* by IBM and *Isabel* use NLP to find relations betweens diseases and symptoms in textbooks and journals

---

# 2 Goal and methods

* Utilize electronic medical record (EMR) to construct a knowledge graph

* Validation against Google health knowledge graph

* Three steps for knowledge graph generation:

  1. Data collection and preparation

  2. Learning of statistical modela

  3. Transformation of models into knowledge graphs

---

# 3 Electronic Medical Record (EMR)

* EMR sometimes used interchangeably with electronic health record (EHR)

* Some authors distinguish between these terms: EHR is comprehensive collection of EMRs

* EMR is information on a patient from one --TODO--

* EMRs useful as data source because they represent diseases and their symptoms in real-world environment

* Difficult data source for four reasons:
  1. Notes from physicians and notes less formal
  2. Comorbidities, confounding factors and nuances present
  3. Associations between diseases and symptoms are statistical
  4. Pre-filtered by physician

---

# 6 Conclusion

Thank you for attending my presentation!

Do you think that Schema.org still has **unused potential**? Or are the extensions all we can expect?

---

# 7 Sources I

* [1] M. Rotmensch, Y. Halpern, A. Tlimat, S. Horng, und D. Sontag, „Learning a Health Knowledge Graph from Electronic Medical Records“, Sci Rep, Bd. 7, Nr. 1, S. 5994, Juli 2017, doi: 10.1038/s41598-017-05778-z.


---

# 7 Sources II

* U. Serles und D. Fensel, "Analysis of Schema.org at Five Levels of KR", in *An Introduction to Knowledge Graphs*, Cham: Springer Nature Switzerland, 2024, S. 259–270. doi: 10.1007/978-3-031-45256-7_15.
* P. Hitzler, "A review of the semantic web field", *Commun. ACM*, Bd. 64, Nr. 2, S. 76–83, Jan. 2021, doi: 10.1145/3397512.
