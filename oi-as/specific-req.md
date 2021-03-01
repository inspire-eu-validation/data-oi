# Orthoimagery - theme-specific requirement

**Purpose**: Verify that the following specic requirements are meet.

* Requirements for Orthoimage Coverages:

(1) By way of derogation from the requirement in Section 2.2 of Annex II ([IR-ISDSS](./README.md#ref_IR-ISDSS)), any grid compatible with one of the following coordinate reference systems may be used for making gridded Orthoimagery data available:
	— two-dimensional geodetic coordinates (latitude and longitude) based on a datum specified in Section 1.2 of Annex II and using the parameters of the GRS80 ellipsoid;
	— plane coordinates using the ETRS89 Lambert Conformal Conic coordinate reference system;
	— plane coordinates using the ETRS89 Transverse Mercator coordinate reference system.
	The grid specified in Section 2.2.1 of Annex II shall not be used.
(2) The footprint of an OrthoimageCoverage instance shall be spatially included in its geographic extent that is described through the domainExtent property.
(3) The value type of the metadata property carried by the spatial object type OrthoimageCoverage shall be set to OM_Observation when using the Observation and Measurement metadata model defined in ISO 19156:2011.
(4) All the OrthoimageCoverage instances, to which an aggregated OrthoimageCoverage instance refers, shall be consistent. This means that they shall share the same range type, Coordinate Reference System and resolution. They shall also support grid alignment, i.e. the grid points in one OrthoimageCoverage instance line up with grid points of the other OrthoimageCoverage instances, so that grid cells do not partially overlap.
(5) The contributing footprint of an OrthoimageCoverage instance referred by an aggregated OrthoimageCoverage instance shall be spatially included in its own footprint.
(6) The contributing footprints of any two OrthoimageCoverage instances referred to by the same aggregated OrthoimageCoverage instance shall be either adjacent or disjoint.
(7) The union of the contributing footprints of the OrthoimageCoverage instances referred to by the same aggregated OrthoimageCoverage instance shall determine the footprint of the aggregated OrthoimageCoverage instance.

* Requirements for mosaic elements:

(1) All the mosaic elements related to an OrthoimageCoverage instance shall be of the same type, i.e. either SingleMosaicElement or AggregatedMosaicElement.
(2) The geometries delineating any two MosaicElement instances related to the same OrthoimageCoverage instance shall be either adjacent or disjoint.
(3) The union of the geometries delineating all MosaicElement instances related to the same OrthoimageCoverage instance shall include its footprint and be contained in its geographic domain extent.



**Prerequisites**

**Test method**

Check manually that the specic requirements are meet.

**Reference(s)**: 

* [TG DS-OI](./README.md#ref_TG_DS_OI) 5.3.1.4.1.; 5.3.1.4.4.; 5.3.1.4.5.; 5.3.1.4.6.; 6.2.2.2.
* [IR-ISDSS](./README.md#ref_IR-ISDSS) Annex III, Section 3.5.2.; 3.5.3.

**Test type**: Manual

**Notes** 


## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

Abbreviation                   |  XPath expression                 |Multiplicity       |Voidable
------------------------------ | --------------------------------- | ------------------|----------
