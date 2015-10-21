#A.20.IR29.ds.specification

**Purpose**: For every conformity statement, one citation of the product specification or user requirement against which data is being evaluated must be given.

**Prerequisites**
* [A.01.validate](A.01.validate.md) must be passed

**Test method**

The test first checks if there is at least one [specification](#specification). In case there is none, a warning is thrown.
It then performs the following checks
*	The specification must contain an element of type gmd:CI_Citation/gmd:title which should not be an [empty characterstring](./README.md#emptychar)
*	The specification must contain an element of type gmd:CI_Citation/gmd:date[./*/gmd:dateType/*/text()='{type}']/*/gmd:date, where {type} is one of creation, revision and publication.

**Reference(s)**

* [TG MD](./README.md#ref_TG_MD), 2.8.2, Req 29
* [IR MD](README.md#ref_IR_MD) Part B. 7.2

**Test type:** Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="specification"></a> specification    | ./gmd:dataQualityInfo/*/gmd:report/*/gmd:result/*/specification