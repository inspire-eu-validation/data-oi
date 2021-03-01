# Orthoimagery - Constraints

**Purpose**: Verify that the features provided in the dataset adhere to the constraints specified in the INSPIRE application schema.

* The acquisition time of the orthoimage coverage shall be provided through the phenomenonTime attribute or the mosaicElement association (acquisitionTimeRequired).
* The dimension of the grid used shall always be 2 (domainDimensionIs2).
* The domainExtent attribute shall be at least populated with a subtype of EX_GeographicExtent (domainExtentContainsGeographicElement).
* The coordinate reference system used to reference the grid shall be provided (domainRequiresCRS).
* All the OrthoimageCoverage instances, to which an aggregated OrthoimageCoverage instance refers, shall share the same orientation of grid axes and the same grid spacing in each direction (identicalOffsetVectorsWithinOrthoimageAggregation).
* The origin of the grid shall be described in two dimensions (originDimensionIs2).
* The values in the range set shall be described by the Integer type (rangeSetValuesAreOfTypeInteger).


**Prerequisites**

**Test method**

The following checks are performed for every feature in the dataset:

* Check that the acquisition time of the orthoimage coverage is provided through the [phenomenonTime](#phenomenonTime) attribute or the [mosaicElement](#mosaicElement) association (OCL: "inv: phenomenonTime->notEmpty() or mosaicElement->notEmpty()").

* Check that the grid [dimension](#dimension) is 2 for an OrthoimageryCoverage (OCL: "inv:domainSet.dimension=2").

* Check that the [domainExtent](#domainExtent) is at least populated with a subtype of EX_GeographicExtent (OCL: "inv: domainExtent.geographicElement->size()>=1").
	
* Check that the [coordinate reference system](#originCRS) used to reference the grid is provided (OCL: "inv: domainSet.origin.coordinateReferenceSystem->notEmpty").

* Check that the [origin](#origin) of the grid is described in two dimensions (OCL: "inv: domainSet.origin.dimension=2").


The following checks shall be manually performed for every feature in the dataset:

* Check that all the OrthoimageCoverage instances, to which an aggregated OrthoimageCoverage instance refers, share the same orientation of grid axes and the same grid spacing in each direction (OCL: "Inv: contributingOrthoimageCoverage->forAll(v | v.domainSet.offsetVectors = self.domainSet.offsetVectors)").

* Check that the values in the range set are described by the Integer type (OCL: "inv: rangeSet->forAll(v | v.oclIsKindOf(Integer))").


**Reference(s)**: 

* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 4 (2)
* [TG DS-OI](./README.md#ref_TG_DS_OI) 5.3.2.1.3.
* [IR-ISDSS](./README.md#ref_IR-ISDSS) Annex III, Section 3.2.1.

**Test type**: Automatic + Manual

**Notes** 


## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
constraintViolation <a name="constraintViolation"/>  |  XML document '$filename', $featureType '$gmlid': The constraint '$constraint' is violated.

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

Abbreviation                                               |  XPath expression                     |Multiplicity       |Voidable
---------------------------------------------------------- | ------------------------------------- | ------------------|----------
phenomenonTime <a name="phenomenonTime"></a> | //schema-element(oi:OrthoimageCoverage)/oi:phenomenonTime/@xlink:href | 0..1 | Yes
mosaicElement <a name="mosaicElement"></a> | //schema-element(oi:OrthoimageCoverage)/oi:mosaicElement/@xlink:href | 0..\* | Yes
dimension <a name="dimension"></a> | //schema-element(oi:OrthoimageCoverage)/gml:domainSet/gml:RectifiedGrid/@dimension | 1 | Not applicable
domainExtent <a name="domainExtent"></a> | //schema-element(oi:OrthoimageCoverage)/oi:domainExtent/gmd:EX_Extent/gmd:geographicElement | 1..\* | No
origin CRS <a name="originCRS"></a> | //schema-element(oi:OrthoimageCoverage)/gml:domainSet/gml:RectifiedGrid/gml:origin/gml:Point/@srsName | 0..1 | Not applicable
origin dimension <a name="origin"></a> | //schema-element(oi:OrthoimageCoverage)/gml:domainSet/gml:RectifiedGrid/gml:origin/gml:Point/@srsDimension | 0..1 | Not applicable