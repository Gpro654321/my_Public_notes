| Short cut key        | what it does                                                                                 | Example    | Does it work in google sheets |
| -------------------- | -------------------------------------------------------------------------------------------- | ---------- | ----------------------------- |
| F4                   | Fixes a formula                                                                              | C4 -> $C$4 | Y                             |
| Ctrl+Shift+Downarrow | Selects cells along a column until it reaches a blank cell                                   |            | Y                             |
| Ctrl + H             | Find & Replace                                                                               |            | Y                             |
| Ctrl+Shift+V         | Paste special -> Values only                                                                 |            | Y                             |
| Ctrl + D             | copies the formula of the first cell of the selected range to the rest of the selected cells |            | Y                             |


# Advantages of Using a table over a name range
1. In a table column wise addressing is possible. Eg. If there is a table named "myexpenses" lets say that the table ranges from A1 : D14. If column "D" has the expenses, then all the expenses may be addressed as "myexpenses[expenses]"
2. If a formula is applied to a column eg. sum. If a new row is added at the last if the range is a table then the formula will automatically be extended to the last row as well.