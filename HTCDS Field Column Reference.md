# HTCDS Field Column Reference

### Status
Status indicates the release status of the field. Possible values are "Draft" to indicate the field is being considered for "Release" status. "Retired" indicates the field used to be a part of the standard but is now removed.
### Core
Core indicates whether the field shoud be considered a core component of the standard. Non-core fields may be optional.
### Category
There are two categories. "Data" indicates the primary purpose of the field is to store relevant data or information about the trafficking case. "Process" indicates the field's primary purpose is to facilitate a related process such as the case lifecycle.
### Field Name Prefix
This is the three letter prefix of the Field Name. It indicates the relevant table in the field definition.
### Field Name
The name of the field is the system identifier. Typically it should not have spaces and each word is capitalised. It's primary purpose is to enable future computer systems to consistently address the field.
### Field Label
The label is the human readable label of the field that might appear in the user interface of the case management system. This would typically be adjusted based upon context such as language, region, etc.
### Field Type
Field types are the category of the field. Examples include picklist and text. Case management systems typically require a format or type category during design and configuration.
### Salesforce Standard or Custom
Indicates whether the field could be mapped to an existing standard Salesforce field.
### Value Names
These are the system identifiers of the possible values in a picklist.
### Value Labels
These are the human readable labels of possible picklist values.
### Description
This is a description of the field used when there might be ambiguity as to the purpose of usage of the field.
### Notes
Notes include references to other standards or other usage guidance for the field.

