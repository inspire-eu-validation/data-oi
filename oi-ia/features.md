# Feature references

**Purpose**: Verify that referenced features can be retrieved.

**Prerequisites**

**Test method**

* Verify that any feature reference in an association role is publicly accessible via HTTP, i.e. inspect all relevant properties. If a reference (@xlink:href) has a value that starts with "#", verify that an element with a `gml:id` attribute with the referenced identifier exists in the same document. If the reference starts with "http", verify that a HTTP GET request to the URI retrieves an XML document. Otherwise report [brokenLink](#brokenLink).

This data theme currently has the following association role:

* [OrthoimageCoverage.contributingOrthoimageCoverage](#contributingOrthoimageCoverage): OrthoimageCoverage
* [OrthoimageCoverage.mosaicElement](#mosaicElement): MosaicElement 


**Reference(s)**: 

* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 4 (2)

**Test type**: Automated

**Notes**

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
brokenLink <a name="brokenLink"/>  |  XML document '$filename', $featureType '$gmlid': The property '$propertyName' has a value '$value' that cannot be retrieved using HTTP. Every code list value must be made available in an online registry. 

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

Abbreviation                         |  XPath expression    | Multiplicity    | Voidable
------------------------------------ | ---------------------|-----------------|------------
OrthoimageCoverage.contributingOrthoimageCoverage <a name ="contributingOrthoimageCoverage"></a>	| //schema-element(oi:OrthoimageCoverage)/oi:contributingOrthoimageCoverage/oi:OrthoimageAggregation/oi:contributingOrthoimageCoverage/@xlink:href | 0..\* | No
OrthoimageCoverage.mosaicElement <a name ="mosaicElement"></a>	| //schema-element(oi:OrthoimageCoverage)/oi:mosaicElement/@xlink:href | 0..\* | Yes