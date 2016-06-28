#Keywords in vocabulary

**Purpose**: Keyword values originating from a single version of a single controlled vocabulary
shall be grouped in a single instance

**Prerequisites**
* [Schema validation](Schema validation.md) must be passed

**Test method**

1. For each [descriptiveKeywords](#keyword) element, the referenced controlled vocabulary should be unique
2. Each referenced controlled vocabulary must appear in at most one [descriptiveKeywords](#keyword) element


**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD) 2.4.2, Req 19


**Test type:** Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="keyword"></a> Keyword   | gmd:identificationInfo[1]/*/gmd:descriptiveKeywords