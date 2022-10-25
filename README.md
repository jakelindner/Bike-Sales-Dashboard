# Bike Sales Dashboard
 Excel project created by [Alex Freberg](https://www.youtube.com/watch?v=opJgMj1IUrc)



## Data Cleaning
Deduping the Data
- Deduped the data based on ID
- Manually checked the duplicates using conditional formatting to verify no other field is needed
- Deduped on ID Column
- 26 duplicates were removed; 1,000 unique values remain

Applied user friendly names:
- Married...M -> Married | S -> Single
- Gender... M -> Male | F -> Female

Added Age Bracket to group the ages for better visualization
- =IF([@Age]>54,"Old",IF([@Age]>=31,"Middle Age", IF([@Age]<31,"Adolescent","Invalid")))

Added Count fields to potentially use in Calculated Fields
- Total Count: =IF([@ID]>=0,1,0)
- Purchased Count: =IF([@[Purchased Bike]]="Yes",1,0)
- Home Owner Count: =IF([@[Home Owner]]="Yes",1,0)

## Pivot Table Creation
Created multiple pivot tables:
- number of bikes purchased by Education
- % of bikes purchased by Occupation
- % of bikes purchased by Age Bracket
- number of bikes purchased by Commute Distance
- number of bikes purchased by Income Level
- number of bikes purchased by Number of Children
- % of bikes purchased by Home Owners

## Dashboard Creation
By using the pivot tables, I created dynamic graphs that will change based on the filters provided.

Chart Formatting:
- I chose a consistant blue for all the graphs (Blue is good for color blind audiences)
- I removed gridlines, vertical axis labels, and the legend
- I added informative chart title and data labels

Slicer/Filter Creation:
- I created slicers that connected to all the pivot tables/charts
- One based on Region
- One based on Home Owner
- One based on Education
