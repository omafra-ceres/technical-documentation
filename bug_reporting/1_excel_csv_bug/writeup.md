# Excel CSV Formatting Writeup

> When users click the `Download` button when viewing a dataset a `.csv` file is downloaded to their computers. Users expected to be able to open this file directly in Excel but the dataset appears in a single cell when that is attempted. Instead users must create an Excel file and import the `.csv` data to that file.

## Steps to reproduce

1. View a dataset in the Ceres app
1. Click the `Download` button
1. Open the downloaded file in Excel

## Diagnosis

This is likely a limitation of the `data > .csv` conversion happening in the app.

```
const downloadContent = () => {
  const headers = tableHeaders
    .map(header => header.title)
    .reduce((acc, cur) => (acc ? acc + "," : "") + JSON.stringify(cur), "")
    + "\n"
  const rows = tableItems
    .map(row => row
      .map(item => item == null ? "" : item)
      .reduce((acc, cur) => (acc ? acc + "," : "") + JSON.stringify(cur), "")
    ).join("\n")
  const csv = headers + rows
  const blob = new Blob([csv], { type: 'text/csv;charset=utf-8;' })
  saveAs(blob, details.name.toLowerCase().replace(" ", "_"))
}
```

## Suggested Resolution

As per [this StackExchenage question](https://superuser.com/questions/238944/how-to-force-excel-to-open-csv-files-with-data-arranged-in-columns) there are a few possible resolutions.

1. Replace the comma delimiter with a tab character
1. Change file extension to `.xls` (NOT RECOMMENDED — this does not account for the interoperability of the `.csv` format)
1. As per [this answer](https://superuser.com/a/1222081) use the `SEP=;` option in the `.csv` formatting