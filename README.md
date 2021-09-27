# ArchOnto

At this moment, the development of the ArchOnto ontology is being maintained on GitLab, which can be accessed through https://gitlab.inesctec.pt/episa/archonto

## Project context

Over the years the National Archive of Torre do Tombo has been acquiring a unique collection of historical and contemporary objects. In his possession he has original documents from the 9th century to the present day. This institution has, over the years, been describing all the cultural objects it has in its possession, and this is one of the tasks that has the most human resources allocated.
Torre do Tombo has used the ISAD(G) and ISAAR(CPF) standards for the description of its cultural objects, however these have been showing some limitations that need to be overcome. Taking into account these limitations, the EPISA (Entity and Property Inference for Semantic Archives) project was created, a project that has as partners INESC TEC, DGLAB (General Direction of the Book, Archives and Libraries) and the University of Évora , and a duration of three years, 2019-2021.
This project aims, among other objectives, to develop a prototype for an open source knowledge graph platform, adopting the data model for archival description used by DGLAB. This project is also dedicated to finding ways to ensure the effective migration of content stored according to ICA standards to an ontology-based model, requiring the use of cross-walks and the inference of new relationships with semi-automated methods. (Almeida and Runa 2018)
For the development of the knowledge graph, the model CIDOC-CRM, a model created in the context of museums and which is already stable, has been taken into account.


## ArchOnto (current version)

New ontology created in the domain of the archives as an extension of CIDOC-CRM, in the current version 6.2.7. In common, all properties and classes created for this model have an "AR" prefix, which aims to differentiate the CIDOC-CRM model. Whenever the creation of a class this has the prefix "ARE", while in the properties has the prefix "ARP". The ArchOnto consists of five base ontologies (CIDOC-CRM, N-ary, the ISAD Ontology, DataObject, and an ontology for the connection between CIDOC-CRM and DataObject), explained further below.


### CIDOC-CRM (version 6.2.7)
- Reference ontology aimed at facilitating the integration, mediation and exchange of information within the scope of cultural heritage. Provides the semantic definitions and rules necessary to transform disparate and localized sources of information into a coherent global resource. CRM aims to serve as a reference in terms of concepts and, therefore, semantics to database schemes and document organization structures in different information systems. Use the prefixes "E" for Entities and "P" for Properties.


### N-ary 
- Ontology created to represent tuples of arity greater than two. With this ontology it is possible to represent all instances in which it is necessary to present connections that are not binary, that is, relationships that connect more than two individuals. Ontology created taking into account the suggestion given by CIDOC-CRM to represent non-binary relationships.


### ISAD Ontology
- Ontology created to represent all elements of the ISAD(G) standard. It has Data Properties in its base that allow the incorporation of all ISAD(G) elements. With this ontology, information on existing archival descriptions created over the years by the various archives at national level is maintained. The ontology allows, whenever necessary, the validation of the contents that have been atomized, checking if they are in conformity with the registration that already existed in the ISAD(G) description. With this ontology it will be possible to maintain the interoperability of all data represented in ISAD(G).


### DataObject
- Ontology created in order to validate literal values used in properties of the new data model created. It has in its base classes and Data Properties that are used to validate data of simple types in the ontology, guaranteeing the validation based on the class.


### Ontology to link CIDOC-CRM with the DataObject Ontology
- Ontology created to link the CIDOC-CRM ontology with the DataObject ontology. It imports both ontologies and has an Object Property that allows the connection of the two imported ontologies - hasValue.
