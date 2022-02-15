# Microsoft Excel
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

There are currently three HTCDS spreadsheet templates. They can be used to more quickly develop a spreadsheet to capture case data.

Each template uses fields in spreadsheet columns and that represent those fields listed as 'core' in the standard. The top row is hidden and displays the field names which can be used to programatically map fields in the future.

The [first template](https://github.com/UNMigration/HTCDS/raw/master/Toolkit/Excel/HTCDS%20Excel%20Spreadsheet%20v2.0.xlsx) is a simple list of fields and each row as a number. This is the simplest template and most compatible with older versions of Microsoft Excel. However, this file does not have any field validation included. Therefore the author of the spreadsheet should adapt the tool to ensure that valid picklist values and date formats are maintained.

The [second template](https://github.com/UNMigration/HTCDS/raw/master/Toolkit/Excel/HTCDS%20Excel%20Spreadsheet%20single%20select%20with%20validation%20v2.0.xlsx) contains the same list of fields as the first, but with the addition of Excel field validation on relevent fields. The field validation values are in the "validation" sheet.

The [third template](https://github.com/UNMigration/HTCDS/raw/master/Toolkit/Excel/HTCDS%20Excel%20Spreadsheet%20multi%20select%20with%20validation%20v2.0.xlsm) contains the same list of fields as the other two templates, but also includes an additional feature to enable multi-select values to be stored in Excel fields. For example, in the "Type of Exploitation" field, multiple values can be selected in one field in one row. The semi-colon is used as the delimeter.

## Customising the Multi-select Options
The multi-select feature in the third template uses VBA code within the spreadsheet to populate the values in the cells. When customising the spreadsheet (particularly when adding or removing columns), the VBA code also needs minor modifications so that the multi-select feature is applied to the correct columns.

To update the VBA code, follow the procedure below:

1. Open the [multi-select template](https://github.com/UNMigration/HTCDS/raw/master/Toolkit/Excel/HTCDS%20Excel%20Spreadsheet%20multi%20select%20with%20validation%20v2.0.xlsm) in Microsoft Excel.
2. On the title of the sheet at the bottom left of the window, right-click and select "View Code" from the context menu. A new window title "Visual Basic for Applications" should load. 
3. About one third of the way down you should see a line of code: `If Target.Column = 8 Or Target.Column = 18 Or Target.Column = 20 Or Target.Column = 21 Or Target.Column = 22 Or Target.Column = 23 Or Target.Column = 25 Then` Each number in this line corresponds to a column number which needs multi-select functionality. For example, Column 8 corresponds to Column H, Column 18 corresponds to Column R, etc.
4. If a new column is inserted or removed then edit these numbers accordingly. For example, if a new column C is inserted, then edit Column 8 to be Column 9, Column 18 to Column 19, etc.
5. Save the updated code by clicking the Save icon, and close the Microsoft Visual Basic for Applications window.
