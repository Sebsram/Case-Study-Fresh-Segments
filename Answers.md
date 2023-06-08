# Data Exploration and Cleansing. 
**1. Update the fresh_segments.interest_metrics table by modifying the month_year column to be a date data type with the start of the month**

![a1](https://user-images.githubusercontent.com/130475600/236249721-5c5194dc-4d15-4601-8787-bf849008a47f.PNG)

**2. What is count of records in the fresh_segments.interest_metrics for each month_year value sorted in chronological order 
(earliest to latest) with the null values appearing first?**

![a2](https://user-images.githubusercontent.com/130475600/236250547-e5903da2-e606-4cdc-b65e-bb920de2488b.PNG)

| month_year | count |
| ---------- | ----- |
|            | 1194  |
| 01-2019    | 973   |
| 02-2019    | 1121  |
| 03-2019    | 1136  |
| 04-2019    | 1099  |
| 05-2019    | 857   |
| 06-2019    | 824   |
| 07-2018    | 729   |
| 07-2019    | 864   |
| 08-2018    | 767   |
| 08-2019    | 1149  |
| 09-2018    | 780   |
| 10-2018    | 857   |
| 11-2018    | 928   |
| 12-2018    | 995   |

**3. What do you think we should do with these null values in the fresh_segments.interest_metrics**

Since we don't have any information about the null values, and the reason why they were added that way on the dataset, I would recommend dropping them. 

![a3](https://user-images.githubusercontent.com/130475600/236251210-914eeb22-d896-46d6-8467-03fdc0eb6ace.PNG)

**4. How many interest_id values exist in the fresh_segments.interest_metrics table but not in the fresh_segments.interest_map table? What about the other way around?**

![a4](https://github.com/Sebsram/Case-Study-Fresh-Segments/assets/130475600/1326c5bc-66d0-4eb7-94f7-35e663313f13)

|map_id_count | metrics_id_count  |not_in_metric | not_in_map |
| ---------- | ----- | ---------- | ----- |
|   1209         | 1202  |      null      | 7  |
