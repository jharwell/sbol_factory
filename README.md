# opil
The Open Protocol Interface Language (OPIL) is intended as a standard language for protocol interfaces. This repository represents an initial OPIL implementation. 

## OPIL is implemented in OWL
A Turtle serialzation of he OPIL ontology can  be found in the 'rdf' directory. OPIL is built on SBOL version 3, but the version 3 of the SBOL ontology is not yet available.  The 'rdf' directory contains a fragment of the anticipated SBOL v3 ontology, based on the SBOL v3 specification.

Our initial example uses OPIL to model the Time Series protocol as described in the 2019 Q4 - 2020 Q1 Strateos Capabilities Overview document and the  YeastSTATES 1.0 Time Series Round 1 experimental request. The models include classes from the SBO and NCI Thesaurus ontologies, but the NCI ontology is not imported because its large file size causes problems for ontology editors. 

## Generating JSON from OPIL
The sample program in this repo shows how the  JSON for the YeastSTATES 1.0 Time Series Round 1 request can be generated from its OPIL representation. The program requires that instances of a class are also inferred to be instances of their superclass. This inferencing is provided by the `custom_eval` module, which is copied without modification from the `rdflib` [examples](https://rdflib.readthedocs.io/en/stable/apidocs/examples.html#module-examples.custom_eval) package. 

The  `opil_demo` package and its dependencies can be installed with
 ```
 python setup.py install
```

