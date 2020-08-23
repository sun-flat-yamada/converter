# Tech note of converter

Tech note of Converter.

## Excel to JSON

We often use Excel.

And nowadays, we often use JSON when we use data in programs.

JSON is simple and is the data of choice for programs to handle.
So we often come across situations where we want to convert from Excel to JSON.

A simple tool is this.

- [exceltk](https://github.com/fanfeilong/exceltk)

We can download precompiled binary from `exceltk/pub/exceltk.[version].zip`
And we can do it in the following way:

```bat
# Convert excel to json
.\exceltk.exe -t json -xls .\source-list.xlsx

# This tool creates a JSON file with a sheet name concatenated after the file name.
# The first line of the sheet is interpreted as the key.
# Outputs it with the following structure.
type .\source-lisetSheet1.json
{
  'name':'Sheet1',
  'rows':[
    {
      'column1':'row1-1',
      'column2':'row1-2',
      'column3':'row1-3',
         :
    },
    {
      'column1':'row2-1',
      'column2':'row2-2',
      'column3':'row2-3',
         :
    }
  ]
}
```
