## Summary
Bring specific columns using a common column

**Instructions**

1. Have a main sheet
2. Make sure your first column is the same for all the sheets
3. Create a new column with the name of the data you want to bring into the main sheet
4. Click onto empty cell below the new name and type

```excel
=VLOOKUP(
```

5. Click on A2
6. Go to other sheet and highlight all the columns
7. Type the number of the column you want to bring over to the main sheet
8. Type in FALSE then close the bracket

**Example VLOOKUP formulas**

```excel
=VLOOKUP(A2,BillingAccount74265926!A:H,3, FALSE)

=VLOOKUP(A2,BillingAccount74265926!A:H,4, FALSE)

=VLOOKUP(A2,BillingAccount74265926!A:H,5, FALSE)

=VLOOKUP(A2,BillingAccount74265926!A:H,6, FALSE)

=VLOOKUP(A2,BillingAccount74265926!A:H,7, FALSE)

=VLOOKUP(A2,BillingAccount74265926!A:H,8, FALSE) 



=VLOOKUP(A2,BillingAccount74265926!A:H,3, FALSE)

=VLOOKUP(A2,Misc!C:C,3,FALSE)

=VLOOKUP('Misc (2)'!A:I,9,FALSE)
```


**———————————————————————————**

**Summary**

Excel commands that will help with productivity

**How to append extra text (ie. @google.ca)**
=Concatenate(A1, "@example.com")



**How to clear extra characters in a cell**

=TRIM(A1)



**How to Compare 2 Columns**

[https://www.techjunkie.com/compare-2-columns-excel/](https://www.techjunkie.com/compare-2-columns-excel/)





**How to bring specific columns using a common column**

**Step 1**

make sure column one is the same across other spreadsheets

**Step 2**


```excel
=VLOOKUP(A2,subscriptionCount!A:C,3, FALSE)

=VLOOKUP(A2,subscriptionCount!A:C,4, FALSE)

=VLOOKUP(A2,subscriptionCount!A:C,5, FALSE)

=VLOOKUP(A2,subscriptionCount!A:C,6, FALSE)
```