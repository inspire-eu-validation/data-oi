# Conformance class: Application schema, Orthoimagery

Conformance class for the requirements associated with the application schema. 

To be able to test this conformance class, the encoding of the data set must be known, i.e. this is a parameterized conformance class. The XPath expressions used in this test suite assume that the GML encoding is used. If used with the GML encoding this conformance class has an indirect dependency to the conformance class "GML application schemas, Orthoimagery".

This conformance class is part of the [INSPIRE Data Specification on Orthoimagery](../README.md).

## Standardization target type

INSPIRE spatial data set

## Dependencies

### Direct dependencies

none

### Indirect dependencies

An indirect dependency is another conformance class whose requirements must be met by a related resource.

| Specification | Conformance class | Related resource | Parameters |
| ------------- | ----------------- | ---------------- | ---------- |
| [TG DS-OI](./README.md#ref_TG_DS_OI) | [GML application schemas, Orthoimagery](../oi-gml/README.md) | INSPIRE spatial data set encoded in GML, Orthoimagery | n/a |
 
## Feature types <a name="feature-types"></a>

The instantiable feature types are:

* OrthoimageCoverage
* SingleMosaicElement
* AggregatedMosaicElement


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
| [Code list values](./code-list-values.md)  | ready for review  | A.1.3 |
| [Constraints](./constraints.md)  | ready for review   | A.1.6  |
| [External Object Identifiers](./ext-object-id.md)  | ready for review  | A.1.6  |
| [Specific requirements](./specific-req.md)  | ready for review   | A.2.3; A.3.5; A.3.6  |


## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         | Namespace
-------------- | -------------------------------------------------
oi	 	 	   | http://inspire.ec.europa.eu/schemas/oi/4.0
base           | http://inspire.ec.europa.eu/schemas/base/3.3
gml            | http://www.opengis.net/gml/3.2
wfs            | http://www.opengis.net/wfs/2.0
xsi            | http://www.w3.org/2001/XMLSchema-instance
xlink          | http://www.w3.org/1999/xlink
xml            | http://www.w3.org/XML/1998/namespace
