 Project_1 : Excel Dashboard of Bike Buyers data

## Source/Reference:

- Datasource:  
https://github.com/AlexTheAnalyst/Excel-Tutorial/blob/main/Excel%20Project%20Dataset.xlsx

- Reference: 
NA

## Aim

1. Data cleaning of given raw data in Excel
2. Dashboard creation in Excel

## Complete Process

- Created four sheets in the excel file : bike_buyers, Working Sheet, Pivot Table, Dashboard.
- `bike_buyers` contains raw data as it is.
- In `Working Sheet`, we copied data from `bike_buyers` and data cleaning process is done in it.
- **Note:** `CTRL+A` for selecting complete sheet.

### Data Understanding

- apply filter on entire data.
- This is classification data where `Purchased Bike` is a outcome field.
- There are total 1026 rows and 13 columns/fields.
- Data contains following fields:

    1. `ID`:
        - Unique ID assigned for each customer
        - numeric
        - unique values ie 1026 values
    2. `Marital Status`: 
        - Is customer married or not?
        - categorical
        - two values: M (married)/ S (single)
    3. `Gender`:
        - Gender of the customer
        - categorical
        - two values: M (male)/ F (female)
    4. `Income`:
        - Income of customer
        - categorical
        - 16 values: 10k, 20k, 30k, 40k, 50k, 60k, 70k, 80k, 90k, 100k, 110k, 120k, 130k, 150k, 160k, 170k
    5. `Children`:
        - Number of children customer has
        - discrete numerical, categorical
        - 6 values: 0, 1, 2, 3, 4, 5, 6
    6. `Education`:
        - Highest education of customer
        - categorical
        - 5 values: Partial High School, High School, Partial College, Bachelors, Graduate Degree
    7. `Occupation`:
        - Current occupation of customer
        - categorical
        - 5 values: Clerical, Management, Manual, Professional, Skilled Manual
    8. `Home Owner`:
        - Does customer owns a house?
        - categorical
        - two values: Yes/ No
    9. `Cars`:
        - How many cars are owned by customer?
        - discrete numeric categorical
        - 5 values: 0, 1, 2, 3, 4
    10. `Commute Distance`:
        - How much distance customer needs to commit daily?
        - categorical
        - 5 values: 0-1 miles, 1-2 miles, 2-5 miles, 5-10 miles, 10+ miles
    11. `Region`:
        - Region in which customer resides
        - categorical
        - 3 values: Europe, North America, Pacific
    12. `Age`: 
        - Age of the customer
        - discrete numerical, can be converted into continuous categorical
        - many values
    13. `Purchased Bike`: 
        - did customer purchase bike?
        - categorical, result column
        - 2 values: Yes/ No


### Data Cleaning Process

- Data cleaning process is started now

    1. **Removing Duplicates**:
        - In `Data > remove duplicates` tab, we can remove duplicates directly
        - There were 26 duplicates in our data. After removing them we have 1000 unique rows.
    2. **Change categorical values for user convenience in Dashboard**:
        - In `Marital Status` field, change `M` -> `Married`, `S` -> `Single`
        - **Note**: `CTRL+H` for find and replace tab
        - In `Gender` field, change `M` -> `Male`, `F` -> `Female`
        - In `Income`, value format changed to `Currency`
        - IN `Commute Distance` field, change `10+ miles` -> `More Than 10 Miles`
        - Create new column `Age Bracket`, and convert age data from column `Age` into ranges instead of discrete values for sake of simplicity while visualizing. Values inside `Age Bracket` field:
            - 0-30 : Adolescent
            - 31-58 : Middle Age
            - 58+ : Old

### Pivoting data

- Now Pivot tables and visualizations are created on `Pivot Table` sheet
- Following Pivots are formed:
    
    1. Average Income based on Bike purchased or not
        - to check if income affects customer's decision to purchase bike or not
    2. Count of Bike purchased per commuting distance
        - to check effect of commuting distance on customer's decision to purchase bike
    3. Count of Bike purchased per Age Bracket
        - to check effect of Age on customer's decision to purchase bike

- Now Copied the visualizations created to `Dashboard` and arranged them Properly
- Insert slicers

## Results and Conclusions

