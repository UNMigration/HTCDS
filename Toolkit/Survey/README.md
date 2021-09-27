# HDCDS CORE 1.0 Survey
Please download a copy of the XLSForm and XForm files from this folder.

XLSForm and XForm are open standard formats designed to express a survey data model. Many common desktop and cloud-based survey tools support this standard. Platforms such as KoBoToolbox are popular with humanitarian organisations, for example.

Survey tools can help organisation capture case data. In general, surveys capture a record once, and are not usually used to update or manage existing records. (Case management software is usually used to manage and update existing case data). There are many commercial and open-source tools available, and many of them support open data standards that can describe surveys.

The HTCDS toolkit includes an XForm and XLSForm implementation of the HTCDS Core standard, except for outgoing referral fields. XForm is an XML file supporting the W3C XForm standard, and XLSForm is a spreadsheet format which also describes surveys. Either of these solutions can be used to configure a suitable survey tool. The XForm and XLSForm HTCDS files contain the standard HTCDS field names and field labels, which should more easily enable combined data analysis.

Examples of survey tools include ODK, KoBoToolbox, and Survey123. To begin using the HTCDS survey, select a survey tool and import either the XForm or XLSForm file from this repository. An easy example is to follow the KoBoToolbox instructions here, using the following XLSForm URL: https://github.com/UNMigration/HTCDS/raw/master/Toolkit/Survey/htcds_xlsform.xlsx
