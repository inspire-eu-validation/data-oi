# Conformance class: Information accessibility, Orthoimagery

Conformance class for the requirements related to the accessibility of referenced information, for example, information stored in registries (code lists, coordinate reference systems).

To be able to test this conformance class, the encoding of the data set must be known, i.e. this is a parameterized conformance class. The XPath expressions used in this test suite assume that the GML encoding is used. If used with the GML encoding this conformance class has an indirect dependency to the conformance class "GML application schemas, Orthoimagery".

This conformance class is part of the [INSPIRE Data Specification on Orthoimagery](../README.md).

## Standardization target type

INSPIRE spatial data set

## Dependencies

### Direct dependencies

A direct dependency is another conformance class whose requirements must be met by the data set, too.

| Specification | Conformance class | Parameters | 
| ------------- | ----------------- | ---------- |
| [TG DS Template](#ref_TG_DS_tmpl) | [Information accessibility](http://inspire.ec.europa.eu/id/ats/data/3.0rc3/information-accessibility) | n/a |

### Indirect dependencies

An indirect dependency is another conformance class whose requirements must be met by a related resource.

| Specification | Conformance class | Related resource | Parameters |
| ------------- | ----------------- | ---------------- | ---------- |
| [TG DS-OI](#ref_TG_DS_OI) | [GML application schemas, Orthoimagery](../oi-gml/README.md) | INSPIRE spatial data set encoded in GML, Orthoimagery features | n/a |
 
## Feature types <a name="feature-types"></a>

The instantiable feature types are:

* OrthoimageCoverage
* SingleMosaicElement
* AggregatedMosaicElement


*Note*: When "features" or "spatial objects" are mentioned in the test cases, this refers only to instances of feature types of this application schema, not to any types specified in any other application schema.

## External document references

The following abbreviations are used in the test text for referring to external documents:

Abbreviation                     | Document name
-------------------------------- | --------------------------------------------------
TG DS-OI <a name="ref_TG_DS_OI"></a>   | [INSPIRE Data Specification on Orthoimagery – Technical Guidelines version 3.0](http://inspire.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_OI_v3.0.pdf)
TG DS-OI-corr <a name="ref_TG_DS_OI_corr"></a>   | [Corrigenda to the INSPIRE Data Specification on Orthoimagery – Technical Guidelines version 3.0](https://inspire.ec.europa.eu/file/1622/download?token=Rx6gOtrI) ([Annex Corrigenda](https://inspire.ec.europa.eu/file/1623/download?token=gB8mo2zX))
IR-ISDSS <a name="ref_IR-ISDSS"></a>   | [Commission Regulation (EU) No 1089/2010 of 23 November 2010 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards interoperability of spatial data sets and services](https://eur-lex.europa.eu/eli/reg/2010/1089/2014-12-31)
TG DS Template <a name="ref_TG_DS_tmpl"></a>   | [INSPIRE Data Specification Template version 3.0rc3](http://inspire.jrc.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_Template_v3.0rc3.pdf)

## Test Cases

| Identifier                                                        | Status   | Test case in [TG DS-OI](#ref_TG_DS_OI)  |
| ----------------------------------------------------------------- | -------- | ------------ |
| [Feature references](./features.md)  | ready for review  | A.1.4 |

## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         | Namespace
-------------- | -------------------------------------------------
gml            | http://www.opengis.net/gml/3.2
oi   	       | http://inspire.ec.europa.eu/schemas/oi/4.0

The following variables are used to refer to the corresponding Xpath expressions in all test descriptions:

Variable       | Value
-------------- | -------------------------------------------------
$features      |  //schema-element(oi:OrthoimageCoverage)