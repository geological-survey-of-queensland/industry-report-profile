# Resources Industry Report Profile
Resource authority holders need to submit a range of statutory reports on their activities. Reports include all mineral exploration, geothermal exploration, greenhouse gas exploration, petroleum exploration, petroleum well, seismic survey or airborne geophysical survey, mineral development licence, petroleum lease, and petroleum pipeline licence reports and some other exploration related reporting.

Reporting obligations are defined here:
https://www.business.qld.gov.au/industries/mining-energy-water/resources/minerals-coal/reports-notices and
https://www.business.qld.gov.au/industries/mining-energy-water/resources/petroleum-energy/reports-notices

<img src="model/GSQ%20Industry%20Report%20Profile.svg" style="width:800px;" alt="Resources Industry Report model" />  


## Usage

<img src="model/GSQ%20Industry%20Report%20Usage.svg" style="width:800px;" alt="Resources Industry Report Usage" />  

* When government issues a permit to a holder, the legislation requires a permit holder to submit reports to the Department when certain activities are performed under the conditions of the permit.
* The reports contain knowledge of the geological resource.
* Historically, industry reports have been lodged through [QDEX Reports](https://qdexguest.dnrm.qld.gov.au/portal/site/qdex/).
* GDMP will deliver a new lodgement portal to replace QDEX Reports.
* Most industry reports have a confidentiality period before becoming open file.


## Profile Resources
This profile is presented as a series of files that perform different roles:

1. [model/](model/) - the *model* folder contains this profile's models in both graphical (SVG) and machine-readable, textual, form ( [RDF](https://www.w3.org/RDF/) turtle).
2. [shapes/](shapes/) - folder containing SHACL shapes files used to validate data's conformance to this profile's model.
3. [profile.ttl](profile.ttl) - the profile declaration. A description of all of the items in this profile (the formal model, validating resources, documentation etc.) according to the W3C's [Profiles Ontology](https://www.w3.org/TR/dx-prof/) which describes how all the parts related to one another, the roles they play (to give *guidance* for use, to *validate* data etc.) and how this profile *profiles* the various standards listed above.


## GSQ classes
CLasses used in this profile:
1. [Queensland Mining Permit](https://github.com/geological-survey-of-queensland/gsq-permit-profile) - used if the report relates to a permit(s)
2. [GSQ Survey Profile](https://github.com/geological-survey-of-queensland/gsq-survey-profile) - used if the report is the result of a survey event


## OWL classes
1. [dcat:Dataset](https://w3c.github.io/dxwg/dcat/#Class:Dataset) - industry report is a special type of dataset
2. [dcat:Theme](https://w3c.github.io/dxwg/dcat/#Property:resource_theme) - used to categorise the resource, the GSQ themes are described as [skos:Concept](http://www.w3.org/2004/02/skos/core#Concept)s in the vocabulary [GSQ Data Themes](https://vocabs.gsq.digital/vocabulary/gsq-dataset-theme)
3. [dcat:Distribution](https://w3c.github.io/dxwg/dcat/#Class:Distribution)
4. [dct:Location](https://w3c.github.io/dxwg/dcat/#Class:Location) - spatial coverage of the report expressed as lat/long, centroid, bounding box or simple polygon
5. [dct:creator](https://w3c.github.io/dxwg/dcat/#Property:resource_creator) - the author of the report
6. [dct:publisher](https://w3c.github.io/dxwg/dcat/#Property:resource_publisher) - GSQ
7. [dct:contactPoint](https://w3c.github.io/dxwg/dcat/#Property:resource_contact_point) - GSQ contact
8. [dct:title](https://w3c.github.io/dxwg/dcat/#Property:resource_title) - report title
9. [dct:description](https://w3c.github.io/dxwg/dcat/#Property:resource_description)
10. [dct:identifier](https://w3c.github.io/dxwg/dcat/#Property:resource_identifier) - report number
11. [dct:license](https://w3c.github.io/dxwg/dcat/#Property:resource_license) - not shown in diagram for readability
12. [dcat:keyword](https://w3c.github.io/dxwg/dcat/#Property:resource_keyword) - not shown in diagram for readability
13. [foaf:Agent](http://xmlns.com/foaf/spec/#term_Agent)
14. [rdfs:seeAlso](https://www.w3.org/TR/rdf-schema/#ch_seealso) - refers to secondary metadata
15. [FOAF document](http://xmlns.com/foaf/spec/#term_Document) - a document with secondary metadata
16. [ProperInterval](https://www.w3.org/TR/owl-time/#time:ProperInterval) - the temporal coverage of the report
17. [dct:created](https://w3c.github.io/dxwg/dcat/)
18. [dct:issued](https://w3c.github.io/dxwg/dcat/#Property:resource_release_date) - date of formal issuance (e.g., open file publication)
19. [dct:modified](https://w3c.github.io/dxwg/dcat/#Property:resource_update_date) - most recent date on which the item was changed, updated or modified
19. [prov:wasGeneratedBy](https://www.w3.org/TR/prov-o/#wasGeneratedBy) - the survey or other activity that generated the report (the completion of production of a new entity by an activity). Created as a link to that survey.
19. [prov:wasAttributedTo](https://www.w3.org/TR/prov-o/#wasAttributedTo) - the company or individual who submitted the report (attribution is the ascribing of an entity to an agent).


### [Distribution](https://w3c.github.io/dxwg/dcat/#Class:Distribution) properties not shown in the diagram:
1. [Title](https://w3c.github.io/dxwg/dcat/#Property:distribution_title)
2. [Description](https://w3c.github.io/dxwg/dcat/#Property:distribution_description)
3. [Download URL](https://w3c.github.io/dxwg/dcat/#Property:distribution_download_url)
4. [Byte size](https://w3c.github.io/dxwg/dcat/#Property:distribution_size)
5. [Format](https://w3c.github.io/dxwg/dcat/#Property:distribution_format)


## Vocabularies
The vocabularies used in this profile are:
1. [Georesources Report Type](https://vocabs.gsq.digital/vocabulary/georesource-report)
2. [GSQ Dataset Theme](https://vocabs.gsq.digital/vocabulary/gsq-dataset-theme)
3. [Earth Science Data Category](https://vocabs.gsq.digital/vocabulary/earth-science-data-category) - the category(s) of data contained in the report
4. [Geoadmin Feature](https://vocabs.gsq.digital/vocabulary/gsq-features)
5. [Data Access Rights](https://vocabs.gsq.digital/vocabulary/data-access-rights)
6. [Commodity](https://vocabs.gsq.digital/vocabulary/gsq-commodity)


## Alignment to QDEX Reports Metadata
| QDEX Reports Field   | New Metadata Field                                    |
|----------------------|-------------------------------------------------------|
| Report Title         | Title                                                 |
| Report Type          | Resources Industry Report Type vocab                        |
| Author Name          | dct:creator?                                          |
| Lodger               | Recorded as logged-in-user                            |
| Submitter            | Submitter (prov:wasAttributedTo)                      |
| Locality             | dct:Location                                          |
| Map References       | Not required - can be derived using spatial intersect |
| Commodity            | Select from commodity vocabulary                      |
| Keywords             | Use CKAN controlled keywords vocabulary (ideally)     |
| Tenure               | Lookup to Queensland Mining Permit                    |
| Tectonic             | Not required - can be derived using spatial intersect |
| Stratigraphy         | Select from stratigraphy vocabulary?                  |
| Age                  | Not required - can be derived using spatial intersect |
| Date of Report       | time:ProperInterval (hasStartTime + hasEndTime)        |
| Date of Receipt      | System recorded dct:created                           |
| Project Names        | Free text?                                            |
| Mines/Prospect Names | Lookup from sites register                           |
| Well Names           | Lookup from borehole register                        |
| Seismic Survey Names | Lookup to survey register                                               |


## Licence
The content of this repository is licensed for use with the [Creative Commons 4.0 License](https://creativecommons.org/licenses/by/4.0/). See the [license deed](LICENSE) for details.


## Contacts
**Geoscience Information Team**,
Geological Survey of Queensland,
Department of Resources,
Brisbane, QLD, Australia,
<geological_info@resources.qld.gov.au>
