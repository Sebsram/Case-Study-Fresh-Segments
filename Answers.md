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

**5.Summarise the id values in the fresh_segments.interest_map by its total record count in this table**

![a5](https://github.com/Sebsram/Case-Study-Fresh-Segments/assets/130475600/b6d16851-1768-492c-9a39-a6c845b6ff9a)

| count |
| ----- |
| 1209  |

**6. What sort of table join should we perform for our analysis and why? Check your logic by checking the rows where interest_id = 21246 in your joined output and include all columns from fresh_segments.interest_metrics and all columns from fresh_segments.interest_map except from the id column.**

INNER JOIN is the most appropiate join for this question

![a6](https://github.com/Sebsram/Case-Study-Fresh-Segments/assets/130475600/a1186bb8-f8df-4b72-8ccd-c731a1bfcd80)

**7.Are there any records in your joined table where the month_year value is before the created_at value from the fresh_segments.interest_map table? Do you think these values are valid and why?**

![a7](https://github.com/Sebsram/Case-Study-Fresh-Segments/assets/130475600/033dce79-5316-4f1c-a8a1-3ee04ed2bb83)

| count |
| ----- |
| 188 |

# Interest Analysis
**1.Which interests have been present in all month_year dates in our dataset?**
We start by checking the number of unique months in our dataset

![b1a](https://github.com/Sebsram/Case-Study-Fresh-Segments/assets/130475600/8d7c424c-19ac-422a-b638-b6f88225a82e)

| unique_month_year |
| ----------------- |
| 14                |

![b1b](https://github.com/Sebsram/Case-Study-Fresh-Segments/assets/130475600/27861f89-ebda-4557-b177-44e79cdeb0bd)

| t_months | count |
| -------- | ----- |
| 14       | 480   |
