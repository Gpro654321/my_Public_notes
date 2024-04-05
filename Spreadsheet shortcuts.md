| Short cut key | what it does    | Example    |
| ------------- | --------------- | ---------- |
| F4            | Fixes a formula | C4 -> $C$4 |


# Advantages of Using a table over a name range
1. In a table column wise addressing is possible. Eg. If there is a table named "myexpenses" lets say that the table ranges from A1 : D14. If column "D" has the expenses, then all the expenses may be addressed as "myexpenses[expenses]"
2. If a formula is applied to a column eg. sum. If a new row is added at the last if the range is a table then the formula will automatically be extended to the last row as well.