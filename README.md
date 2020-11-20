# belb-retrievor
[![Actions Status](https://github.com/belbet/retrievor/workflows/Go/badge.svg)](https://github.com/belbet/retrievor/actions)

# Examples

## Matches

You can parse results of all match from 2020-01 with

```
startDate := c.String("start-date")
endDate := c.String("end-date")
r := retrievor.MatchesResult{}

r.ParseAllWithStringRange(startDate, endDate)
r.ExportAsCSV()
```

## Clubs

You can parse and export all clubs with

```
var c = ClubParse{}
var countries = []string{"A", "B", "C", "D", "E", "F", "G", "H", "I", "J", "K", "L", "M", "N", "O", "P", "Q", "R", "S", "T", "U", "V", "W", "X", "Y", "Z", "1"}
// Iterate trough all pages
for _, e := range countries {
    c.CurrentPage = e
    c.ParseAll()

}
c.ExportAsCSV()
```