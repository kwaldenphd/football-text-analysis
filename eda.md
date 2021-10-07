# Lab #2 (Structured Data): Exploratory Data Analysis/Visualization

<a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license"><img style="border-width: 0;" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" alt="Creative Commons License" /></a>
This tutorial is licensed under a <a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license">Creative Commons Attribution-NonCommercial 4.0 International License</a>.

# Section Table of Contents

- [Exploratory Data Visualization](#exploratory-data-visualization)
  * [DataBasic: WTFcsv](#databasic-wtfcsv)
  * [Excel](#excel)
  * [Tableau](#tableau)
  * [Python](#python)
  * [RStudio](#rstudio)
- [Discussion/Reflection Questions](#discussionreflection-questions) 

# Exploratory Data Visualization

From [Wikipedia](https://en.wikipedia.org/wiki/Exploratory_data_analysis): "In statistics, exploratory data analysis is an approach of analyzing data sets to summarize their main characteristics, often using statistical graphics and other data visualization methods...EDA is for seeing what the data can tell us beyond the formal modeling or hypothesis testing task."

To think about this another way, "the purpose of EDA is to use summary statistics and visualizations to better understand data, and find clues about the tendencies of the data, its quality and to formulate assumptions and the hypothesis of our analysis" (Andrew Andrade and Lukasz Golab, ["Exploratory Data Analysis"](https://datascienceguide.github.io/exploratory-data-analysis) *Data Science Guide*)

- [Data](#data)
- [DataBasic: WTFcsv](#databasic-wtfcsv)
- [Excel](#excel)
  * [Getting Data Into Excel](#getting-data-into-excel)
  * [Analyzing Data in Excel](#analyzing-data-in-excel)
  * [Creating a Table](#creating-a-table)
  * [Data Visualization](#data-visualization)
  * [PivotTables and PivotCharts](#pivottables-and-pivotcharts) 
  * [PowerQuery](#powerquery)
- [Tableau](#tableau)
  * [Uploading to Tableau Public](#uploading-to-tableau-public)
  * [Discussion and Reflection Questions](#discussion-and-reflection-questions)
- [Python](#python)
- [RStudio](#rstudio)

## Data

1- We'll be using three sample datasets in the Exploratory Data Analysis section of the lab.

2- `ND_Directory_Cleaned_Geography.csv` represents a data structure based on the 1922-1923 student directory. Fields in the dataset include:
- `Combined_Name_Original` (combined first name, last name, and major field)
- `Combined_Name` (combined first name, last name field)
- `Last_Name` (standarized last name)
- `First_Name` (standardized first name)
- `Major` (standardized major)
- `Combined_Address` (combined street, city, state, and country field)
- `Street` (standardized-ish street)
- `City` (standardized city)
- `State` (standardized state)
- `Country` (standardized country)
- `Standardized_Address` (standardized combined street, city, state, country field)
- `Standardized_City_State` (standardized city, state, country field)
- `Country` (standardized country)
- `Latitude` (latitude)
- `Longitude` (longitude)

3- `combined_nd_rosters.csv` represents a data structure scraped from Sports Reference's Notre Dame college football season roster pages. Fields in the dataset include:
- `Rk` (player rank on team at end of season)
- `Season` (season)
- `Player` (combined player name field)
- `First_Name` (player first name)
- `Last_Name` (player last name)
- `G` (number of games)
- `RushingAtt` (number of rushing yards attempted)
- `RushingYds` (number of actual rushing yards)
- `RushingAvg` (average number of rushing yards per attempt)
- `RushingTD` (number of rushing touchdowns)
- `ReceivingRec` (number of receiving receptions)
-  `ReceivingYds` (number of receiving yards)
-  `ReceivingAvg` (average number of receiving yards per reception)
-  `ReceivingTD` (number of receiving touchdowns)
-  `ScrimmagePlays` (number of plays from scrimmage, rush attempts + receptions)
-  `ScrimmageYds` (number of scrimmage yards, rushing + receiving yards)
-  `ScrimmageAvg` (average number of yards from scrimmage per play)
-  `ScrimmageTD` (number of touchdowns from scrimmage, receiving + rushing touchdowns)

4- `combined_nd_schedules_cleaned.csv` represents a data structure scraped from Sports Reference's Notre Dame college football season results pages. Fields in the dataset include:
- `G` (game number)
- `Season` (season or year)
- `Standarized_Date` (standardized game date, YYYY-MM-DD)
- `Date` (original date field, MM DD, YYYY)
- `Day` (game day of week)
- `Time` (game time of day)
- `School` (Notre Dame, includes ranking)
- `Standardized_School` (standardized Notre Dame school field, does not include ranking)
- `Game_Type` (home, away, neutral site game)
- `Opponent` (opponent, includes ranking)
- `Standarized_Opponent` (standardized opponent school field, does not include ranking)
- `Post_Season` (Y/N field indicating if game is postseason/bowl/playoff game)
- `Conf` (conference)
- `Result` (W/L/T game result)
- `Combined_Location` (combined game location, location/city/state/country)
- `City` (game site city)
- `State` (game site state)
- `Country` (game site country)
- `Pts` (number of ND points in game)
- `Opp` (number of opponent points in game`
- `W` (win number)
- `L` (loss number)
- `T` (tie number)
- `Streak` (W/L/T streak)
- `Notes` (additional notes on game)
- `Latitude` (latitude)
- `Longitude` (longitude)

## DataBasic: WTFcsv

5- According to [its website,](https://databasic.io) “DataBasic is a suite of easy-to-use web tools for beginners that introduce concepts of working with data. These simple tools make it easy to work with data in fun ways, so you can learn how to find great stories to tell.” DataBasic is developed and supported by MIT’s [Center for Civic Media](https://civic.mit.edu/) and Emerson College’s [Engagement Lab.](https://elab.emerson.edu/)

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/DataBasic-tutorial/blob/master/screenshots/Capture_1.jpg?raw=true" alt="Capture" /></p>

6- Navigate to https://databasic.io/ in a web browser (preferably Chrome). 

7- Click on the `WTFcsv` icon to open the WTFcsv tool.

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/football-structured-data/blob/main/figures/Fig_1.png?raw=true" alt="Capture" /></p>

8- As described on the page, "WTFcsv tells you WTF is going on with your .csv file. Data arrives at your doorstep in the form of a spreadsheet but how do you find a story in rows and columns? WTFcsv provides the first step by characterizing each column's data type and contents so that you can ask more questions."

9- `WTFcsv` gives you the option to use a sample file or upload your own file.

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/football-structured-data/blob/main/figures/Fig_2.png?raw=true" alt="Capture" /></p>

10- Click on the `Upload a file` icon and select a sample dataset.

11- The lab procedure is going to used the `combined_nd_schedules_cleaned.csv` file, but you can use any of the sample datasets as we move through this section of the lab.

12- Click `Analyze` to analyze the dataset.

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/football-structured-data/blob/main/figures/Fig_3.png?raw=true" alt="Capture" /></p>

13- The WTFcsv results include summary information about the entire dataset as well as a summary view of each field.

14- For the whole dataset, we can tell the number of rows and columns.

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/football-structured-data/blob/main/figures/Fig_4.png?raw=true" alt="Capture" /></p>

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/football-structured-data/blob/main/figures/Fig_5.png?raw=true" alt="Capture" /></p>

15- For each column, we can see the data type (the icon in the top-left corner of that column's tile), a summary visualization for that column (the default tile view), and additional metadata for that column (available by clicking on the circle `i` icon in the top-right corner of the tile).

<blockquote>What is metadata? In the words of information and infrastructure scholar Janet Evans, metadata is "data about data" (Evans, <a href="https://inventingthemedium.com/glossary/">Inventing the Medium: Principles of Interaction Design as a Cultural Practice</a>, glossary). Within WTFcsv, metadata is described as "[summarizing] basic information about your data."</blockquote>

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/football-structured-data/blob/main/figures/Fig_5.png?raw=true" alt="Capture" /></p>

16- Looking at the column visualization for `Day`, we can see this is a string field (circle icon in the top-left), and WTFcsv has given us a bar chart showing the counts for each unique column value.

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/football-structured-data/blob/main/figures/Fig_6.png?raw=true" alt="Capture" /></p>

17- Looking at metadata for `Day` column tile (click the circle `i` icon in the top-right of the tile), we can see this is a string field (a field that includes text characters), the maximum string length, the number of unique values, and the number of entries for the most frequently occurring values.

18- We can go back to the column visualization by clicking on the chart icon in the top-right of the tile.

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/football-structured-data/blob/main/figures/Fig_4.png?raw=true" alt="Capture" /></p>

19- We can look at the column visualization for `Time` and see it is a time field (clock icon in the top-left), and WTFcsv has given us a line plot showing the number of rows for each time value.

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/football-structured-data/blob/main/figures/Fig_7.png?raw=true" alt="Capture" /></p>

20- We can look at the metadata for the `Time` column (click the circle `i` icon in the top-right of the tile) and see the smallest and largest values in this field, as well as the number of rows with missing data (or `NA` values) and the number of unique values.

21- Continue exploring the results for the sample dataset you uploaded. 
- Or, upload and explore another sample dataset.

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/football-structured-data/blob/main/figures/Fig_8.png?raw=true" alt="Capture" /></p>

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/football-structured-data/blob/main/figures/Fig_9.png?raw=true" alt="Capture" /></p>

22- You can also click on the arrow icon next to the page title to get a temporary link to share your results.

23- This tool does not include an image export option for specific visualizations- screenshots are your best option for capturing these visuals.

### WTFcsv Discussion and Reflection Questions

- What do you notice about the results for this dataset (or these datasets) displayed in WTFcsv?
- How does the tool's results shape your understanding of the data?
- What additional questions do you have about this data (or these datasets)? Where would you go next with exploring this dataset using some of the analysis tools/approaches highlighted in the tool?
- Other comments/questions/observations

## Excel

24- Microsoft Excel is a proprietary spreadsheet program that is part of the Microsoft Office (or Office365) suite of tools/programs.

25- The Microsoft Office suite is available via campus computers and the virtual computer lab.
- [Campus Computer Labs](https://inside.nd.edu/task/all/computerlabs)
- [Virtual Computer Lab](https://inside.nd.edu/task/all/virtual-computer-lab)

26- OIT also provides [free access to the Office suite through Office365](https://inside.nd.edu/task/all/office-365-portal), which includes an option to download and install on your local machine.

27- A few notes:
- This tutorial is written on a Windows computer. Mac users will see slightly different menu options in Excel.
- Images and screenshots included in this tutorial are from a sample dataset and do not reflect what you will see working with different data.
- If you do not have Microsoft Excel, some of the tasks we're exploring in Excel (arithmetic operations on a field, generating visualizations, etc) can be accomplished via Google Sheets.
  * However the Pivot Chart, Power Pivot, and Power Query functionality is not available within Google Sheets.

### Getting Data Into Microsoft Excel

28- The sample datasets provided for this lab are in a `CSV` (comma-separated values) plain-text format.

29- The operations we are going to explore in Excel require using a workbook file format, rather than a single `CSV` table or sheet.

30- The goal is to end up with an Excel workbook (or Google Sheets project) that includes the three sample datasets we're using in this section of the lab.

31- One option is to open a blank Excel workbook, save it with a descriptive file name, and import each CSV.
- HESA, "[Importing `*.csv` formatted data into Excel](https://www.hesa.ac.uk/support/user-guides/import-csv)"

32- We can also download an Excel workbook that already has these CSV files loaded into a single workbook.
- [Download from GitHub](https://github.com/kwaldenphd/football-structured-data/blob/main/data/Football_Lab2_Combined_Workbook.xlsx)
- [Download from Google Drive](https://docs.google.com/spreadsheets/d/12LogN6lkr5yfG3tbs9SAdOO6YvuYqP0CkQVkHqQwONQ/edit?usp=sharing)
  * Click `File` --> `Download` --> `Microsoft Excel (.xlsx)`

33- If you're working in Google Sheets, you can [make a copy of the Google Sheet project](https://docs.google.com/spreadsheets/d/12LogN6lkr5yfG3tbs9SAdOO6YvuYqP0CkQVkHqQwONQ/copy).

34- You can also import each CSV file to a new Google Sheets project.
- `File` --> `Import`
- Upload file from your computer or select CSV file in Google Drive
- Select `Comma` as the delimiter
  * Google Docs Help Center, "[Import data sets & spreadsheets](https://support.google.com/docs/answer/40608?hl=en&co=GENIE.Platform%3DDesktop)* 

### Analyzing Data in Microsoft Excel

35- We can use Excel's `AutoSum` tool to calculate preliminary arithmetic operations on data in our workbook.

<p align="center"><a href="https://github.com/kwaldenphd/excel-pivot-tables-tutorial/blob/HUM295-DataViz/screenshots/Capture_1.png?raw=true"><img class="aligncenter" src="https://github.com/kwaldenphd/excel-pivot-tables-tutorial/blob/HUM295-DataViz/screenshots/Capture_1.png?raw=true" alt="" /></a></p>

<p align="center"><a href="https://github.com/kwaldenphd/excel-pivot-tables-tutorial/blob/HUM295-DataViz/screenshots/Capture_1a.png?raw=true"><img class="aligncenter" src="https://github.com/kwaldenphd/excel-pivot-tables-tutorial/blob/HUM295-DataViz/screenshots/Capture_1a.png?raw=true" alt="" /></a></p>

<p align="center"><a href="https://github.com/kwaldenphd/excel-pivot-tables-tutorial/blob/HUM295-DataViz/screenshots/Capture_1aa.png?raw=true"><img class="aligncenter" src="https://github.com/kwaldenphd/excel-pivot-tables-tutorial/blob/HUM295-DataViz/screenshots/Capture_1aa.png?raw=true" alt="" /></a></p>

36- Identify a numeric column in one of the workbook sheets.

37- Use your cursor to select the values in that column.

38- Click the `AutoSum` icon.

<p align="center"><a href="https://github.com/kwaldenphd/excel-pivot-tables-tutorial/blob/HUM295-DataViz/screenshots/Capture_1b.png?raw=true"><img class="aligncenter" src="https://github.com/kwaldenphd/excel-pivot-tables-tutorial/blob/HUM295-DataViz/screenshots/Capture_1b.png?raw=true" alt="" /></a></p>

39- Excel has calculated the sum of the values in your selected cells. The result is printed below your selected values.

40- The AutoSum function defaults to calculating the sum of selected cells, but it can also perform other mathematical calculations.

41- For folks working in Google Sheets, the `Functions` icon is in the menu bar, next to the filter and language icons. The drop-down list includes many of the same arithmetic operations covered with the AutoSum tool in Excel.

### Creating a Table

42- Let's say we want to be able to interact with our dataset by sorting, filtering, etc.

43- This can be useful for data wrangling/cleaning, or summarizing operations.

44- Within Excel, we can access these operations by creating a `Table` from our data.

45- Before creating a table, remove any AutoSum results or outputs.

46- Select all the cells in your table that include data.
- An easy way to do this is to select the top-left cell, use `Control-Shift-Right Arrow` (PC users) or `Command-Shift-Right Arrow` (Mac users) to select all columns with data and `Control-Shift-Down Arrow` (PC users) or `Command-Shift-Down Arrow` (Mac users) to select all rows with data.

47- Once you have selected the entire table, click the `Insert` menu option (next to `File`, `Home`, etc) and click the `Table` icon.

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/football-structured-data/blob/main/figures/Fig_10.png?raw=true" alt="Capture" /></p>

<p align="center"><a href="https://github.com/kwaldenphd/excel-pivot-tables-tutorial/blob/HUM295-DataViz/screenshots/Capture_3.png?raw=true"><img class="aligncenter" src="https://github.com/kwaldenphd/excel-pivot-tables-tutorial/blob/HUM295-DataViz/screenshots/Capture_3.png?raw=true" alt="" /></a></p>

48- Excel has already determined your selection is the data source for the table.

49- Be sure the `My table has headers` box is selected.

50- Click `OK` to create the table.

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/football-structured-data/blob/main/figures/Fig_20.png?raw=true" alt="Capture" /></p>

51- Once you've created the table, go to the `Table Design` tab and rename the table.

52- We also want to add the table to our data model.

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/football-structured-data/blob/main/figures/Fig_21.png?raw=true" alt="Capture" /></p>

53- Select the `Power Pivot` menu option (next to `Table Design`).

54- Click the `Add to Data Model` icon.

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/football-structured-data/blob/main/figures/Fig_22.png?raw=true" alt="Capture" /></p>

55- In the pop-up Power Pivot window, select `File` --> `Close` to add the table to the data model.

56- Go through this process of creating a table (under `Data`), renaming the table (under `Table Design`), and adding the table to the data model (under `Power Pivot`) for each sheet in the workbook.

57- Renaming tables and adding them to the data model is an important step down the line when we want to start aggregating the data for more fine-tuned analysis and visualization.

58- For folks working in Google Sheets, there is not an equivalent for this step. Google Sheets already treats your spreadsheet as a table.

59- BUT, before you start sorting/filtering/etc, you probably want to freeze the first row in the spreadsheet as a column header.
- `View` -- `Freeze` -- `1 row`

<p align="center"><a href="https://github.com/kwaldenphd/excel-pivot-tables-tutorial/blob/HUM295-DataViz/screenshots/Capture_4.png?raw=true"><img class="aligncenter" src="https://github.com/kwaldenphd/excel-pivot-tables-tutorial/blob/HUM295-DataViz/screenshots/Capture_4.png?raw=true" alt="" /></a></p>

<p align="center"><a href="https://github.com/kwaldenphd/excel-pivot-tables-tutorial/blob/HUM295-DataViz/screenshots/Capture_5a.png?raw=true"><img class="aligncenter" src="https://github.com/kwaldenphd/excel-pivot-tables-tutorial/blob/HUM295-DataViz/screenshots/Capture_5a.png?raw=true" alt="" /></a></p>

60- Formatting your data as a table in Excel allows you to sort values within specific columns, and filter the values that display in your table.

61- You can access these tools by clicking the arrow drop-down icon in the first row for each column (in the cell with the column header).

62- For folks working in Google Sheets, many of these same tools are under the `Data` dropdown menu.

63- Explore some of the searching, sorting, and filtering operations.

#### Discussion and Reflection Questions

- How do the AutoSum calculations impact or inform your understanding of the data?
- What questions do you have about the data or calculations?
- Why would it be helpful to be able to sort/filter/etc within a dataset?
- As you explore the sort/search/filter functionality, what questions emerge about the data?
- Other comments/questions/observations

### Data Visualization with Microsoft Excel

64- Excel includes a range of built-in chart types that you can use to generate visualizations for data in your table.

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/football-structured-data/blob/main/figures/Fig_11.png?raw=true" alt="Capture" /></p>

65- Click on the `Recommended Charts` icon under `Data`.

66- Explore the different options Excel recommends for visualizing your data.

67- Click on `OK` in the `Insert Chart` pop-up window to insert a chart to your workbook sheet.

68- You can also click on a specific chart type in the `Charts` menu area to build your own visualizations.

69- For folks working in Google Sheets:
- Google Docs Help Center, "[Types of charts & graphs in Google Sheets](https://support.google.com/docs/answer/190718?hl=en)"
- Google Docs Help Center, "[Add & edit a chart or graph](https://support.google.com/docs/answer/63824?hl=en&co=GENIE.Platform%3DDesktop)"

#### Discussion and Reflection Questions

What types of visualizations were you able to generate in Excel using PivotChart? How could those visualizations shape or impact your understanding of the data? Did you generate any visualizations that were confusing or misleading? Alternatively, did you generate any visualizations that were unexpected or illuminating?

### PivotTables and PivotCharts

70- From [Wikipedia](https://en.wikipedia.org/wiki/Pivot_table):
- "A pivot table is a table of grouped values that aggregates the individual items of a more extensive table within one or more discrete categories. This summary might include sums, averages, or other statistics, which the pivot table groups together using a chosen aggregation function applied to the grouped values."

71- Within Excel, PivotTables (and PivotCharts) let us generate more fine-tuned and customized visualizations for data in the workbook.

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/football-structured-data/blob/main/figures/Fig_18.png?raw=true" alt="Capture" /></p>

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/football-structured-data/blob/main/figures/Fig_17.png?raw=true" alt="Capture" /></p>

72- To create a PivotTable and PivotChart:
- Click on the `PivotChart` dropdown in the `Charts` menu bar area
- Select the `PivotChart & PivotTable` option
- Check that `Use this workbook's Data Model` and `New Worksheet` are selected.
- Click `OK` to create the PivotTable.

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/football-structured-data/blob/main/figures/Fig_19.png?raw=true" alt="Capture" /></p>

73- Your data is now formatted as a PivotTable, which allows us to aggregate, analyze, and visualize across different sheets in the workbook.

74- The steps we took earlier in the lab to name our tables and add them to the data model means we now have a PivotTable and PivotChart that lets us access all three tables for aggregating and visualizing data.

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/football-structured-data/blob/main/figures/Fig_24.png?raw=true" alt="Capture" /></p>

75- The PivotChart side bar allows you to select specific data fields and arrange or restructure them to generate visualizations.

76- You can click on the drop-down arrow next to each table to see a list of its fields (or columns).

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/football-structured-data/blob/main/figures/Fig_25.png?raw=true" alt="Capture" /></p>

77- To show the number of students by major, drag the `Major` field from the `Directory` table into the `Axis (Categories` box.

78- Then, drag the `Major` field from the `Directory` table into the `Values` box.

79- The default value and bar chart are showing us the number of students in each major.

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/football-structured-data/blob/main/figures/Fig_26.png?raw=true" alt="Capture" /></p>

80- The `Values` box also can calculate other arithmetic values for numeric data fields. You can click on the drop-down arrow next to a field in `Values` and select `Value Field Settings` to see these additional options.

81- You can right click on various parts of the bar chart to customize colors and labels.

#### Discussion and Reflection Questions

Experiment with other PivotChart functions and other data fields to generate different types of visualizations.

What types of visualizations were you able to generate in Excel using PivotChart? How could those visualizations shape or impact your understanding of the data? Did you generate any visualizations that were confusing or misleading? Alternatively, did you generate any visualizations that were unexpected or illuminating?

### PowerQuery

82- But one of the things we might want to be able to do with these datasets is connect across them, or generate visualizations that connect across the different discrete datasets.

83- For example, think about the information that is contained in the directory dataset and the data that is contained in the football roster dataset.

84- Theoretically, individuals who played on the football team were also students who attended class and majored in particular subjects.

85- Let's say we wanted to generate visualizations of the home states or majors for individuals playing on the football team.

86- We would need to connect the roster and directory datasets to be able to access information across both tables.

<blockquote>The larger concept we're talking about here falls under the big umbrella of data models and relational database systems. Those concepts are outside the scope of this class, but for folks who want to learn more about relational databases, entity relationship diagrams, data models, and structured query language (SQL):
 <ul>
  <li>Prof. Walden's <a href="https://github.com/kwaldenphd/data-models">"Introduction to relational database systems and data models" lab</a></li>
  <li>Library Carpentry's <a href="https://librarycarpentry.org/lc-sql/08-database-design/index.html">"Database Design" curriculum</a></li>
  <li>Prof. Walden's <a href="https://github.com/kwaldenphd/sqlite-intro">"SQLite Intro" lab</a></li>
  <li>Prof. Walden's <a href="https://github.com/kwaldenphd/sql-queries-joins">"SQL Queries and Joins" lab</a></li>
  <li>Library Carpentry's <a href="https://librarycarpentry.org/lc-sql/">"SQL" curriculum</a></li>
 </ul>
 </blockquote>

87- We can connect these two tables using the `Combined_Name` field in the `directory` table and the `Player` field in the `roster` table.

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/football-structured-data/blob/main/figures/Fig_30.png?raw=true" alt="Capture" /></p>

88- First, we need to establish query relationships with each of the tables in our workbook.
- Click the `From Table/Range` option (under `Get & Transform Data`, top-left) under the `Data` tab
- In the `Power Query Editor` pop-up window, select `Close & Load`

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/football-structured-data/blob/main/figures/Fig_31.png?raw=true" alt="Capture" /></p>

89- You should now see a `Schedules (2)` sheet that also shows up under `Queries & Connections`.

90- Do this for each table in the workbook.

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/football-structured-data/blob/main/figures/Fig_32.png?raw=true" alt="Capture" /></p>

91- Now, we need to create a new table that merges connecting records from the `rosters` and `directory` tables.

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/football-structured-data/blob/main/figures/Fig_29.png?raw=true" alt="Capture" /></p>

92- We can do this by using PowerPivot and PowerQuery to merge connecting records in these fields.
- Click the `Get Data` icon in the `Data` tab
- Hover over `Combine Queries` in the drop-down
- Click `Merge` under `Combine Queries`

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/football-structured-data/blob/main/figures/Fig_33.png?raw=true" alt="Capture" /></p>

93- In the `Merge` pop-up window, select the tables and fields to create this relationship.
- `Player` from `Rosters`
- `Combined_Name` from `Directory`
- `Left Outer` under the `Join Kind` drop-down

94- Click `OK` to create the relationship.

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/football-structured-data/blob/main/figures/Fig_34.png?raw=true" alt="Capture" /></p>

95- Now, we see a new `Merge1` table in the `PowerQuery Editor` window.

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/football-structured-data/blob/main/figures/Fig_35.png?raw=true" alt="Capture" /></p>

96- We can rename this table under `Query Settings`.

97- Now we want to select what columns from the merge will be included in the new table.

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/football-structured-data/blob/main/figures/Fig_36.png?raw=true" alt="Capture" /></p>

98- We can click the arrow icons next to the `Directory` column in the new table to expand the list of merged fields.

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/football-structured-data/blob/main/figures/Fig_37.png?raw=true" alt="Capture" /></p>

99- We want to select fields from the `Directory` table to merge with the `Rosters` table.

100- The name fields are duplicated, so we can focus on columns with major and home geographic information.

101- Click `OK` to merge these columns.

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/football-structured-data/blob/main/figures/Fig_38.png?raw=true" alt="Capture" /></p>

102- We can now see the merged columns in our new table.

103- Click `Close & Load` to save these changes and load the new table to the workbook.

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/football-structured-data/blob/main/figures/Fig_39.png?raw=true" alt="Capture" /></p>

104- We can now see a `Merged_Roster_Directory` sheet in our workbook.

105- We could use this new sheet the connects roster and directory information to aggregate and visualize this data, using the PivotChart tools covered earlier in the lab.

#### Additional Resources

106- We're just scratching the surface of things you can do in Excel using PowerPivot, PowerQuery, and PivotTables.

107- Google Sheets has some of the PivotTable functionality, but does not currently support things like PowerPivot and PowerQuery.

108- For more on PivotTables in Google Sheets:
- Google Docs Help, "[Create & use pivot tables](https://support.google.com/docs/answer/1272900?hl=en&co=GENIE.Platform%3DDesktop)"
- Google Docs Help, "[Create and edit pivot tables](https://support.google.com/a/users/answer/9308944?hl=en)"

109- For more on data models and queries/joins:
- Microsoft Support, "[Relationships between tables in a Data Model](https://support.microsoft.com/en-us/office/relationships-between-tables-in-a-data-model-533dc2b6-9288-4363-9538-8ea6e469112b)"
- Microsoft Support, "[Create a Data Model in Excel](https://support.microsoft.com/en-us/office/create-a-data-model-in-excel-87e7a54c-87dc-488e-9410-5c75dbcb0f7b)"
- Microsoft Support, "[Merge queries and join tables](https://support.microsoft.com/en-us/office/merge-queries-and-join-tables-cbd17828-7a50-4dc6-9aac-20af4ef6d8a6)"

110- For more on PivotTables and PivotCharts:
- Microsoft Support, "[Overview of PivotTables and PivotCharts](https://support.microsoft.com/en-us/office/overview-of-pivottables-and-pivotcharts-527c8fa3-02c0-445a-a2db-7794676bce96)"
- Microsoft Support, "[Create a PivotTable to analyze worksheet data](https://support.microsoft.com/en-us/office/create-a-pivottable-to-analyze-worksheet-data-a9a84538-bfe9-40a9-a8e9-f99134456576)"
- Microsoft Support, "[Create a PivotChart](https://support.microsoft.com/en-us/office/create-a-pivotchart-c1b1e057-6990-4c38-b52b-8255538e7b1c)"

111- For more on PowerPivot and PowerQuery:
- Microsoft Support, "[Get started with Power Pivot in Microsoft Excel](https://support.microsoft.com/en-us/office/create-a-pivotchart-c1b1e057-6990-4c38-b52b-8255538e7b1c)"
- Microsoft Support, "[Power Pivot: Powerful data analysis and data modeling in Excel](https://support.microsoft.com/en-us/office/power-pivot-powerful-data-analysis-and-data-modeling-in-excel-a9c2c6e2-cc49-4976-a7d7-40896795d045)"
- Microsoft Support, "[Learn to use Power Query and Power Pivot in Excel](https://support.microsoft.com/en-us/office/learn-to-use-power-query-and-power-pivot-in-excel-42d895c2-d1d7-41d0-88da-d1ed7ecc102d"
- Microsoft Support, "[Power Pivot- Overview and Learning](https://support.microsoft.com/en-us/office/power-pivot-overview-and-learning-f9001958-7901-4caa-ad80-028a6d2432ed)"
- Microsoft Support, "[Power Query documentation](https://docs.microsoft.com/en-us/power-query/)"

#### Takeaways from all the Excel adventures...

112- You're probably wondering why we spent so much time working in Excel and exploring some of the more advanced functionality, and that's a fair question.

113- Folks with computer science/data science backgrounds and programming chops are probably wondering why we would spend so much time figuring out how to do things in a proprietary software program that can be accomplished programmatically in open-source programs like Python, RStudio, and SQL.

114- A few reasons:
- Google Sheets is a powerful spreadsheet tool, but there's a reason Excel is an industry standard for more organizations/companies that have more advanced data processing workflows and don't necessarily have data scientists/computer scientists/programmers on staff
- Excel integrates with other data processing workflows and visualization tools (specifically PowerBI) to create an incredibly powerful data ecosystem
- So yes, Excel will change, but it's not going anywhere. 
- And to Prof. Walden's knowledge, there's no non-coding spreadsheet program (including Apple Numbers, Google Sheets, open-source Libre Office Calc) that comes in terms of functionality.

115- Additionally, these Excel workflows can help those without a data science/programming/data engineering/etc background understand some of the core concepts and steps involved in data modeling and database systems.
- This helps immensely when you're in a work setting where you need to be able to talk to or interact with folks working in and around database engineering. Even if you're not the one building or maintaining the workflows, you are much better equipped to have intelligent conversations about what those individuals are doing and what you need these systems to do.

#### Reflection Questions

What types of visualizations were you able to generate in Excel using PivotChart? How could those visualizations shape or impact your understanding of the data? Did you generate any visualizations that were confusing or misleading? Alternatively, did you generate any visualizations that were unexpected or illuminating?

## Tableau

116- [Tableau](https://www.tableau.com) is a software company founded in Silicon Valley in 2003. Developed by researchers affiliated with Stanford University’s Computer Science Department, Tableau is a commercialized application of academic research. Represented as DATA on the New York Stock Exchange after a 2013 initial public offering, Tableau reported $877 million in revenue in <a href="s1.q4cdn.com/149179428/files/doc_financials/2017/FY2016-Annual-Report.pdf">the 2017 fiscal year</a>. Most often deployed in business environments, Tableau Desktop is a subscription-based data analysis and visualization software. Tableau Server and Tableau Online offer subscription-based web-publishing options for making data and interactive visualizations available on the web. Tableau Public offers limited Tableau Desktop functionality with some options for uploading visualizations through the Tableau Public website.

117- To get started, you'll need to download the free version of Tableau (Tableau Public) on your personal computer.

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/football-structured-data/blob/main/figures/Fig_40.png?raw=true" alt="Capture" /></p>

118- Head to https://public.tableau.com/ in a web browser and enter your email to download the program.
- NOTE: Mendoza students in the Business Analytics program have access to Tableau through the [Mendoza virtual computer lab](https://inside.nd.edu/task/all/virtual-computer-lab-mendoza-anaytics).

119- It's a large program, so be prepared for the installation process to take some time.

<p align="center"><a href="https://github.com/kwaldenphd/excel-pivot-tables-tutorial/blob/master/screenshots/Capture_16.PNG?raw=true"><img class="aligncenter" src="https://github.com/kwaldenphd/excel-pivot-tables-tutorial/blob/master/screenshots/Capture_16.PNG?raw=true" alt="" /></a></p>

120- Once the installation has finished, launch the program.

121- Tableau can connect to a number of different data sources and file types.

122- You can load single `CSV` files for the sample datasets we're working with in this section of the lab, or you can upload the entire `Football_Lab2_Combined_Workbook` workbook file.
- [Download from GitHub](https://github.com/kwaldenphd/football-structured-data/blob/main/data/Football_Lab2_Combined_Workbook.xlsx)
- [Download from Google Drive](https://docs.google.com/spreadsheets/d/12LogN6lkr5yfG3tbs9SAdOO6YvuYqP0CkQVkHqQwONQ/edit?usp=sharing)
  * Click `File` --> `Download` --> `Microsoft Excel (.xlsx)`

123- NOTE: Images and screenshots included in this tutorial are from a sample dataset and do not reflect what you will see working with different data.

124- Once you've selected the data you want to load, click `Open` to load the data in Tableau.

<p align="center"><a href="https://github.com/kwaldenphd/excel-pivot-tables-tutorial/blob/HUM295-DataViz/screenshots/Capture_20.png?raw=true"><img class="aligncenter" src="https://github.com/kwaldenphd/excel-pivot-tables-tutorial/blob/HUM295-DataViz/screenshots/Capture_20.png?raw=true" alt="" /></a></p>

125- Tableau's `Data Source` previews the structure of the data we loaded from the Excel file. 

126- Tableau determines what type of data is contained in each field (integer number values, dates, geographic spatial information, strings of letters or characters, etc.).

127- If we wanted to analyze or visualize data from multiple tables, Tableau's Data Source offers some functionality for joining tables and building a database structure.

<p align="center"><a href="https://github.com/kwaldenphd/excel-pivot-tables-tutorial/blob/master/screenshots/Capture_19.PNG?raw=true"><img class="aligncenter" src="https://github.com/kwaldenphd/excel-pivot-tables-tutorial/blob/master/screenshots/Capture_19.PNG?raw=true" alt="" /></a></p>

<p align="center"><a href="https://github.com/kwaldenphd/excel-pivot-tables-tutorial/blob/HUM295-DataViz/screenshots/Capture_20.png?raw=true"><img class="aligncenter" src="https://github.com/kwaldenphd/excel-pivot-tables-tutorial/blob/HUM295-DataViz/screenshots/Capture_20.png?raw=true" alt="" /></a></p>

128- Click on the `Sheet 1` icon next to `Data Source` to move into Tableau's visualization builder interface.

129- Tableau distinguishes between `Dimensions` (data fields that cannot be aggregated) and `Measures` (data fields that can be aggregated--or have mathematical operations performed on them).

<p align="center"><a href="https://github.com/kwaldenphd/excel-pivot-tables-tutorial/blob/HUM295-DataViz/screenshots/Capture_21.png?raw=true"><img class="aligncenter" src="https://github.com/kwaldenphd/excel-pivot-tables-tutorial/blob/HUM295-DataViz/screenshots/Capture_21.png?raw=true" alt="" /></a></p>

130- You can move fields in the dataset to `Columns` and `Rows` to generate aggregate tables.
- This is similar to what we were able to do in Excel using a PivotTable

<p align="center"><a href="https://github.com/kwaldenphd/excel-pivot-tables-tutorial/blob/HUM295-DataViz/screenshots/Capture_23.png?raw=true"><img class="aligncenter" src="https://github.com/kwaldenphd/excel-pivot-tables-tutorial/blob/HUM295-DataViz/screenshots/Capture_23.png?raw=true" alt="" /></a></p>

131- Once you've created an aggregate table for select fields, Tableau may generate a visualization, or the `Show Me` panel on the right-hand side of the window shows other visualization types possible for this data selection.

132- You can move your cursor over the chart to see the interactive data points.

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/football-structured-data/blob/main/figures/Fig_41.png?raw=true" alt="Capture" /></p>

133- Tableau allows chart customization with the `Marks` panel.

134- You can drag specific fields from `Dimensions` or `Measures` onto elements in the `Marks` panel to customize labels, size, shapes, color, etc.

<p align="center"><img class=" size-full wp-image-53 aligncenter" src="https://github.com/kwaldenphd/football-structured-data/blob/main/figures/Fig_42.png?raw=true" alt="Capture" /></p>

135-The `Show Me` panel on the right-hand side of the Tableau window shows other types of visualizations you can build in Tableau using this combination of data fields and calculations.

### Additional Resources

- Tableau Public, ["How-To Videos and Resources"](https://public.tableau.com/en-us/s/resources)
- Miriam Posner, ["Getting started with Tableau Public"](http://miriamposner.com/classes/dh201w19/tutorials-guides/data-visualization/getting-started-with-tableau-public/) tutorial for Winter 2019 "Digital Humanities 201" class

## Uploading to Tableau Public

137- One of Tableau's features is that it allows users to upload interactive data visualizations to the web and embed them in websites and other online spaces.

<p align="center"><a href="https://github.com/kwaldenphd/excel-pivot-tables-tutorial/blob/master/screenshots/Capture_28.PNG?raw=true"><img class="aligncenter" src="https://github.com/kwaldenphd/excel-pivot-tables-tutorial/blob/master/screenshots/Capture_28.PNG?raw=true" alt="" /></a></p>

138- If you have additional time, <a href="https://public.tableau.com/en-us/s/">create a free profile</a> on Tableau Public's website.

139- Click `File` --> `Save to Tableau Public`, and use your login credentials to save your Tableau workbook to Tableau Public's website.

<p align="center"><a href="https://github.com/kwaldenphd/excel-pivot-tables-tutorial/blob/master/screenshots/Capture_29.PNG?raw=true"><img class="aligncenter" src="https://github.com/kwaldenphd/excel-pivot-tables-tutorial/blob/master/screenshots/Capture_29.PNG?raw=true" alt="" /></a></p>

<p align="center"><a href="https://github.com/kwaldenphd/excel-pivot-tables-tutorial/blob/master/screenshots/Capture_30.PNG?raw=true"><img class="aligncenter" src="https://github.com/kwaldenphd/excel-pivot-tables-tutorial/blob/master/screenshots/Capture_30.PNG?raw=true" alt="" /></a></p>

<p align="center"><a href="https://github.com/kwaldenphd/excel-pivot-tables-tutorial/blob/master/screenshots/Capture_31.PNG?raw=true"><img class="aligncenter" src="https://github.com/kwaldenphd/excel-pivot-tables-tutorial/blob/master/screenshots/Capture_31.PNG?raw=true" alt="" /></a></p>

140- Your Tableau Public online profile can host your interactive visualizations, and also gives you the option to share, download, and embed the interactive content.

## Python

141- We can also use a programming language like Python to generate and customize many of the types of visualizations we created using Excel and Tableau.

142- Prof. Walden has built out a Jupyter notebook that goes into more detail about using Python for exploratory data analysis for the sample datasets presented in this lab.

143- Since we're dealing with single data files, running things on your personal computer should not cause any problems.

144- But you can also make copies of the CoLab notebooks and connect to data files within Google Drive.

145- To mount Google Drive files within CoLab:
- [Google Colab, "External Data: Local Files, Drive, Sheets, and Cloud Storage"](https://colab.research.google.com/notebooks/io.ipynb#scrollTo=XDg9OBaYqRMd)
- Mdkaish Ansari, "[How to Connect Google Colab with Google Drive](https://www.marktechpost.com/2019/06/07/how-to-connect-google-colab-with-google-drive/)" *Markettechpost* (7 June 2019)

146- The Jupyter notebook uses the following programs and Python libraries:
- `matplotlib`
- `pandas`
- `geopandas`
- `plotly`

147- The Jupyter notebook includes sample code for the following steps/tasks, using the roster, directory, and schedule datasets:
- Load data as Pandas `DataFrame`
- Merging directory and roster datasets
- Static visualization with `Pandas` and `Matplotlib`
- Static geospatial data visualization with `geopandas`, `shapely`, and `matplotib`
- Interactive visualization with `plotly`
- Interactive geospatial data visualization with `plotly`

148- Jupyter Notebook:
- [GitHub](https://github.com/kwaldenphd/football-structured-data/blob/main/notebooks/nd-football-eda.ipynb)
- [NBviewer](https://nbviewer.jupyter.org/github/kwaldenphd/football-structured-data/blob/main/notebooks/nd-football-eda.ipynb)
- [Google CoLab](https://drive.google.com/file/d/1MybxGo9ngdm20rzV1xAqAGYZwNsLINTM/view?usp=sharing)

## RStudio

149- We can also use a scripting language like R/RStudio to generate and customize many of the types of visualizations we created using Excel and Tableau.

150- Prof. Walden has built out an RMarkdown file that goes into more detail about using R for exploratory data analysis for the sample datasets presented in this lab.

151- The RMarkdown file uses the following programs and packages:
- `tidyr`
- `dplyr`
- `magrittr`
- `ggplot2`
- `viridis`
- `htmltools`
- `geojsonio`
- `plotly`
- `leaflet`
- `sf`
- `sp`
- `tmap`
- `maps`

152- The RMarkdown notebook includes sample code for the following steps/tasks, using the roster, directory, and schedule datasets:
- Load data as `DataFrame`
- Merging directory and roster datasets using `dplyr` and `tidyr`
- Static visualization with `ggplot2`
- Static geospatial data visualization with `ggplot2`, `sf, `sp`, `tmap`, and `maps`
- Interactive visualization with `plotly`
- Interactive geospatial data visualization with `plotly` and `leaflet`

153- RMarkdown File:
- [`.rmd` file on GitHub](https://github.com/kwaldenphd/football-structured-data/blob/main/notebooks/nd-football-eda.Rmd)
- [`.rmd` file on Google Drive](https://drive.google.com/file/d/1gvhci2x1IVsHOFCEwkeVvm_HSUPU0l2V/view?usp=sharing)
- [RStudio Cloud](https://rstudio.cloud/project/2977118)

154- RStudio Project:
- [GitHub, `.zip`](https://drive.google.com/file/d/1zex8zotq6TpLtzcDukl0NtH8oxaswBqR/view?usp=sharing)
- [RStudio Cloud](https://rstudio.cloud/project/2977118)

## EDA Discussion and Reflection Questions:

Experiment with other data fields and calculations to generate different types of visualizations. You can add new worksheets or duplicate an existing worksheet to build multiple visualizations.

What types of visualizations were you able to generate in Tableau? How were those visualizations similar or different than what you generated in Excel?

How could those visualizations shape or impact your understanding of the data? Did you generate any visualizations that were confusing or misleading? Alternatively, did you generate any visualizations that were unexpected or illuminating?</blockquote>

- How is the data in Tableau presented or organized differently than the same information in Excel? 
- What similarities or differences do you notice between the two user interfaces for building data visualizations?
