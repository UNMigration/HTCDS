# HTCDS EXPANDED 2.0 Salesforce Unmanaged Package
Use this URL to install the Salesforce unmanaged package into a Production organization:
[https://login.salesforce.com/packaging/installPackage.apexp?p0=04t4K000002Jk1N](https://login.salesforce.com/packaging/installPackage.apexp?p0=04t4K000002ml1d)

Use this URL to install the Salesforce unmanaged package into a Sandbox organization: [https://test.salesforce.com/packaging/installPackage.apexp?p0=04t4K000002Jk1N](https://test.salesforce.com/packaging/installPackage.apexp?p0=04t4K000002ml1d)

Salesforce is a commercial cloud-based client relational management (CRM) system which is a popular platform used by larger organisations. Typical uses of Salesforce for case management include:

* Helpline/hotline case management
* Dedicated case management systems which are developed, operated and used by large organisations.
* Case management software services, which are centralised multi-tenant platforms operated by specialised service organisations and used by smaller front-line organisations.

**Advantages:**

* Salesforce is a very flexible platform offering various data model design, workflow, reporting and user interface options.
* Salesforce offers excellent security features.
* Provides collaboration functionality on records, potentially replacing email in many cases.

**Disadvantages:**

* Salesforce is a more complicated platform to configure compared to spreadsheets or file-based products. Specialised technical expertise and support may be required.
* Salesforce has a license cost (although free or low cost licenses are available to qualifying non-profit organisations).

The Salesforce Unmanaged Package contains the data model for HTCDS and can be used as a starter-package for any of the three uses above. An “unmanaged package” is a collection of components and metadata which can be installed in a Salesforce environment. After installation, the developer can edit and change the individual component within the package as necessary.

It is recommended to install the package in a Sandbox environment first to test and verify the implementation, before installing it into Production.

The package contains custom fields and objects. Normally, an implementation of Salesforce will include configuration of page layouts, record types, reports, business processes, user interface customisations and security features. The package is not intended to represent a complete case management system on Salesforce.

The HTCDS standard contains field definitions but doesn’t strictly enforce a full object model currently. Therefore, this package has made design assumptions which should be relevant to most implementations but should be verified before implementation. The design features and assumptions are:

* Standard Case, Contact and Account objects are assumed to be used to describe client cases, contact details and organisations accordingly.
* A custom junction object called “Connected Person or Organisation” has been created to allow a many-to-many relationship between Cases and Contacts, and Cases and Organisations.
* A custom object called “Support Plan” represents support planning and is related to the case.
* Historical Trafficking Event fields have been added to the Activity standard object (which would be accessible via cases, for example). It is recommended that the developer verify this design choice and whether an alternative solution such as a custom object is more appropriate for the organisation.
