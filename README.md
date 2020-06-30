# Semantic Modeling API

A service to build semantic models of your datasets. Currently deployed at: http://mira.isi.edu:41728

* [Demo](./demo.ipynb)
* [API Documentation](./docs/api.md)
* [Example datasets](./examples)

A semantic model of a dataset is a graph where nodes are ontology classes and attributes (columns), and edges are ontology properties. The concepts and relationships in the dataset are represented by the semantic model, hence the model precisely describes the intended meaning of the data source. Moreover, it can be used to automatically generate R2RML rules or T2WML specifications (for publishing dataset to DataMart or other knowledge graphs).