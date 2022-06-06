# Conformance class: GML application schemas, Orthoimagery

Conformance class for the GML encoding of spatial objects specified in the INSPIRE GML application schema 'Orthoimagery'. This conformance class examines the data set against requirements associated with the GML application schema.

This conformance class is part of the [INSPIRE Data Specification on Orthoimagery](../README.md).

## Standardization target type

INSPIRE spatial data set encoded in GML, Orthoimagery features

## Dependencies

### Direct dependencies

A direct dependency is another conformance class whose requirements must be met by the GML documents, too.

| Specification | Conformance class | Parameters | 
| ------------- | ----------------- | ---------- |
| [TG DS Template](#ref_TG_DS_tmpl) | [INSPIRE GML application schemas](http://inspire.ec.europa.eu/id/ats/data/3.0rc3/schemas) | n/a |

### Indirect dependencies

n/a
 
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
| [Basic test](./basic.md)  | ready for review  | A.1.1, (A.6.1)  |
| [Validation against INSPIRE official schema](./official-schema-validation.md)  | ready for review  | A.1.1, (A.6.1)  |

## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         | Namespace
-------------- | -------------------------------------------------
oi             | http://inspire.ec.europa.eu/schemas/oi/4.0
