# CSV To Excel #

This little piece of code takes a list of CSV files with a name and inserts them all into a new excel file, you'll get one sheet per CSV. It also improves the display by bolding the first line (assuming these are column titles) and adjusts the width of each column depending on the size of the strings within the column. 

You can use it like this:
	
```
#!python

ew = ExcelWriter()
ew.convert( {
    # Specify the csv files, whether it has column titles (default: yes) and the names
    "sheets" : [
        {
            "filelocation" : "test/work.csv",
            "sheetname" : "Works"
        },
        {
            "filelocation" : "test/person.csv",
            "sheetname" : "People",
            "has_titles" : False
        }
    ],
    # Specify the output name
    "outputname" : "test/test_outout_file.xlsx"

```