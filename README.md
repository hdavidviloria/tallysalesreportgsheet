# Sales Tallier for G Sheets Wizard
### Sales Report Tally System with Google Sheets

Access the system! https://docs.google.com/spreadsheets/d/1zUsfln_8zvVRlsMNUL08lQHyxXND5pm6q1YplBW_nb8/edit?usp=sharing

## Documentation

### How to make a copy of the system

#### 1. First, go to file and click on make a copy.

<img width="606" alt="Screen Shot 2023-02-26 at 10 51 56 PM" src="https://user-images.githubusercontent.com/94162758/221418308-eff49ab4-b03d-43b3-9e06-8a2e131a2272.png">

#### 2. You’ll see this pop-up, then just click on make a copy (this makes a copy of the Google Sheets as well as the code automatically).

<img width="890" alt="Screen Shot 2023-02-26 at 10 51 47 PM" src="https://user-images.githubusercontent.com/94162758/221418319-0d33345b-b4eb-49f8-81fa-9268e0451f41.png">

#### 3. After making a copy, when you click on any of the “add tally” or “subtract tally” buttons, it shows an “Authorization Required” pop-up. Click continue and click on your Google Account.

<img width="1004" alt="Screen Shot 2023-02-26 at 10 52 42 PM" src="https://user-images.githubusercontent.com/94162758/221418331-90889d3e-4397-4fe9-9d9e-fd5ee9125181.png">

#### 4. Now, click on advanced and click on “Go to Untitled project”. 

<img width="714" alt="Screen Shot 2023-02-26 at 10 54 22 PM" src="https://user-images.githubusercontent.com/94162758/221418365-40e0c6c2-d480-4518-a1b1-70d79be6ff3c.png">

<img width="802" alt="Screen Shot 2023-02-27 at 1 43 57 PM" src="https://user-images.githubusercontent.com/94162758/221484061-448b5f4a-8a88-4a24-9cdf-b29378284ecf.png">

<img width="682" alt="Screen Shot 2023-02-26 at 10 56 51 PM" src="https://user-images.githubusercontent.com/94162758/221418391-356d6c44-8103-4e00-82b3-b66a07bef9da.png">

And that’s it!


## How the code works:

You don't need to do anything to make the code work, as when you copy the spreadsheet the code is already copied (if you follow the documentation). However, if you want to understand how this works or edit it, feel free to look at this section :)

Essentially, how this works is that there are functions, that when executed, increase or decrease the value of a number by one (depending if it's add or subtract tally). 

Each button is assigned to a specific function depending on the cell positions of the tallies they are editing. 

For example in the following code blocks below, the function add1 adds the tally at the position of cell C4, while the function of subtract4 subtracts the tally at position of cell C25.

(Credits to Shreyas Kapur on stackoverflow for reference regarding the code to add values (https://stackoverflow.com/a/32816451)

```function add1() {
  SpreadsheetApp.getActiveSheet().getRange('C4').setValue(SpreadsheetApp.getActiveSheet().getRange('C4').getValue() + 1);
}
```
```
function subtract4() {
  SpreadsheetApp.getActiveSheet().getRange('C25').setValue(SpreadsheetApp.getActiveSheet().getRange('C25').getValue() - 1);
}
```




Note: This method is editing specified rows, so let's say if you have many more rows and you want to make it automatic that each button modifies its own rows without adding even more code, you can check out this answer at stackoverflow (https://stackoverflow.com/a/64976479)

If you want to further edit the code to your own liking, you can edit it via the apps script tab in Google Sheets!

<img width="604" alt="Screen Shot 2023-02-26 at 11 00 54 PM" src="https://user-images.githubusercontent.com/94162758/221418694-3f2d9e01-59f2-4782-915a-ae4c32072371.png">
