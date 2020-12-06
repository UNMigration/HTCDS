# Toolkit Guidance

The HTCDS toolkit is designed to accelerate the development of HTCDS-compliant case management systems by providing tools based upon common platforms that can be customised and extended by organisations as necessary. Of course, it’s possible to build a new system and implement the requirement of HTCDS from the ground up using the specification. However, sometimes it is helpful to begin by using the HTCDS toolkit. HTCDS is intended to support different approaches to case management and thereby enabling companies and organisations of various sizes and operating models to utilise HTCDS.

The current version of the toolkit comprises:

1.	Microsoft Excel
2.	XLSForm and XForm survey template
3.	Salesforce Unmanaged Package

Each option is useful in different ways and is relevant to different organisations and approaches to case management. Below gives some guidance on selecting an approach:

## Microsoft Excel
Microsoft Excel is probably the most popular tool for managing case data. Most organisations who use Excel use the desktop tool although some also use Microsoft Excel Online. Typically, data is organised in a table, with each row representing one case / contact.

**Advantages:**

* Easy and fast to set up.
* Usually, there aren’t any specialised technical skills required.
* Excel files are portable and can be shared with team members easily.
* Microsoft Excel has built-in features which enable graphs and aggregate tables to be generated, which is useful for operational and impact reporting.

**Disadvantages:**

* It can be awkward to manage cases with related records in spreadsheets. For example, managing separate support plan records, or managing details about multiple connected organisations is difficult without a relational database.
* Managing the security of sensitive data can be problematic because spreadsheets can be accidentally emailed or left on unsecured USB sticks.
* It can be difficult for users to concurrently use one spreadsheet. (This can sometimes be mitigated using Microsoft Excel Online).
* Microsoft Excel has a license cost.

The HTCDS spreadsheet template has the following features:

* Validation rules against pick list values specified in HTCDS.
* Row 1 contains the Field Name and is hidden by default in the spreadsheet. This row is relevant when data is being analysed alongside other HTCDS datasets.
* Several picklist fields allow multiple selections to be made, e.g. “Type of Exploitation”. This has been enabled using a short VBA code subroutine and allows multiple semi-colon separated values to be selected in a cell.

The picklist validation rules use hidden cells located in cells BA4-BM253. Each range has been given an Excel Name to reference the range more easily. The reference values are located on the same sheet to enable compatibility with Microsoft Excel 2007.

Customise the spreadsheet in the following ways:

* Add new fields (columns) relevant to your requirements.
* The date fields have been set to Short Date format (DD/MM/YYYY). Adjust this as appropriate.
* Edit the VBA code to refine the multi-select capability by activating the Visual Basic Editor. A list of columns on which the multi-select capability is configured is in the Sheet1 VBA object and can be adjusted as necessary (especially if more columns are inserted).

## XSLForm and XForm

XLSForm and XForm are open standard formats designed to express a survey data model. Many common desktop and cloud-based survey tools support this standard. Platforms such as KoBoToolbox are popular with humanitarian organisations, for example.

Survey tools can help organisation capture case data. In general, surveys capture a record once, and are not usually used to update or manage existing records. (Case management software is usually used to manage and update existing case data). There are many commercial and open-source tools available, and many of them support open data standards that can describe surveys.

The HTCDS toolkit includes an XForm and XLSForm implementation of the HTCDS Core standard, except for outgoing referral fields. XForm is an XML file supporting the W3C XForm standard, and XLSForm is a spreadsheet format which also describes surveys. Either of these solutions can be used to configure a suitable survey tool. The XForm and XLSForm HTCDS files contain the standard HTCDS field names and field labels, which should more easily enable combined data analysis.

Examples of survey tools include ODK, KoBoToolbox, and Survey123. To begin using the HTCDS survey, select a survey tool and import either the XForm or XLSForm file from this repository. An easy example is to follow the KoBoToolbox instructions [here](https://support.kobotoolbox.org/xls_url.html), using the following XLSForm URL:
[https://github.com/UNMigration/HTCDS/raw/master/Toolkit/Survey/htcds_xlsform.xlsx]()

## Salesforce Unmanaged Package

Salesforce is a commercial cloud-based client relational management system which is a popular platform used by larger organisations. Typical uses of Salesforce for case management include:

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
