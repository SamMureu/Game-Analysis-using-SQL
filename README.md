# Game-Analysis-using-SQL

### Table of contents
- [Project Name](#project-Name)
- [Dataset Description](#Dataset-Description)
- [What to Do](#What-to-do)

###  Project Name: Decode Gaming Behavior

I will be working with a dataset related to a game. The dataset includes
two tables: 
1. `Player Details`
2.  `Level Details`.
   
  ## Below is a brief description of the dataset and the tasks to perform:
### Dataset Description:

## Player Details Table:

- `P_ID`: Player ID
- `PName`: Player Name
- `L1_status`: Level 1 Status
- 'L2_status`: Level 2 Status
- `L1_code`: Systemgenerated Level 1 Code
- `L2_code`: Systemgenerated Level 2 Code

## Level Details Table:

- `P_ID`: Player ID
- `Dev_ID`: Device ID
- `start_time`: Start Time
- `stages_crossed`: Stages Crossed
- `level`: Game Level
- `difficulty`: Difficulty Level
- `kill_count`: Kill Count
- `headshots_count`: Headshots Count
- `score`: Player Score
- `lives_earned`: Extra Lives Earned
### Entity relationship 
![entity relationship](https://github.com/SamMureu/Game-Analysis-using-SQL/assets/84933401/8a04d24d-db2f-4afa-977f-ebfd5e616a2e)

### What to do?
Use the “Game Analysis.sql” file. to answer 15 questions by writing SQL queries.

1. Extract `P_ID`, `Dev_ID`, `PName`, and `Difficulty_level` of all players at Level 0.![1](https://github.com/SamMureu/Game-Analysis-using-SQL/assets/84933401/972cbf7e-fb5b-4351-af76-db4631d6ff1e)

2. Find `Level1_code`wise average `Kill_Count` where `lives_earned` is 2, and at least 3
stages are crossed.![2](https://github.com/SamMureu/Game-Analysis-using-SQL/assets/84933401/8e746c02-f05b-4656-994b-ccf55a201744)

3. Find the total number of stages crossed at each difficulty level for Level 2 with players
using `zm_series` devices. Arrange the result in decreasing order of the total number of
stages crossed.![3](https://github.com/SamMureu/Game-Analysis-using-SQL/assets/84933401/c0c84663-c465-4bfb-bf70-0e2bbaff06ff)

4. Extract `P_ID` and the total number of unique dates for those players who have played
games on multiple days.![4](https://github.com/SamMureu/Game-Analysis-using-SQL/assets/84933401/4c878388-2eb1-4fff-9a7d-6ba97c57841a)

5. Find `P_ID` and levelwise sum of `kill_counts` where `kill_count` is greater than the
average kill count for Medium difficulty.![5](https://github.com/SamMureu/Game-Analysis-using-SQL/assets/84933401/e69809c8-395e-42fd-9f28-aeead331e8fd)

6. Find `Level` and its corresponding `Level_code`wise sum of lives earned, excluding Level
 '0' Arrange in ascending order of level.![6](https://github.com/SamMureu/Game-Analysis-using-SQL/assets/84933401/1f767fc5-41ae-4eaa-b789-f490e0702105)

7. Find the top 3 scores based on each `Dev_ID` and rank them in increasing order using
`Row_Number`. Display the difficulty as well.![7](https://github.com/SamMureu/Game-Analysis-using-SQL/assets/84933401/85d75483-66f2-415a-9280-bf0732200f5f)

8. Find the `first_login` datetime for each device ID.![8](https://github.com/SamMureu/Game-Analysis-using-SQL/assets/84933401/3e4570e7-ab17-4491-a313-fdb8cfd03d0d)

9. Find the top 5 scores based on each difficulty level and rank them in increasing order
using `Rank`. Display `Dev_ID` as well.![9](https://github.com/SamMureu/Game-Analysis-using-SQL/assets/84933401/826b67da-5bf2-4f48-a0f9-ad7db4cf6750)

10. Find the device ID that is first logged in (based on `start_datetime`) for each player
(`P_ID`). Output should contain player ID, device ID, and first login datetime.![10](https://github.com/SamMureu/Game-Analysis-using-SQL/assets/84933401/eeb28e70-12d1-433c-b6b3-cafe11b7b402)

11. For each player and date, determine how many `kill_counts` were played by the player
so far.
a). Using window functions![11a](https://github.com/SamMureu/Game-Analysis-using-SQL/assets/84933401/b122025a-bd47-4c6c-b906-f20dd43907af)

b). Without window functions![11b](https://github.com/SamMureu/Game-Analysis-using-SQL/assets/84933401/fb4e5568-6209-4298-bc0a-57003452917b)

12. Find the cumulative sum of stages crossed over `start_datetime` for each `P_ID`,
excluding the most recent `start_datetime`.![12](https://github.com/SamMureu/Game-Analysis-using-SQL/assets/84933401/518f1acb-11cc-47ba-8c2b-dee43020a526)

13. Extract the top 3 highest sums of scores for each `Dev_ID` and the corresponding `P_ID`.![13](https://github.com/SamMureu/Game-Analysis-using-SQL/assets/84933401/d98152f3-d052-4521-87b3-b9d836dd5796)

14. Find players who scored more than 50% of the average score, scored by the sum of
scores for each `P_ID`.![14](https://github.com/SamMureu/Game-Analysis-using-SQL/assets/84933401/75a48e82-6c92-4076-9ae3-32078850ae0f)

15. Create a stored procedure to find the top `n` `headshots_count` based on each `Dev_ID`
and rank them in increasing order using `Row_Number`. Display the difficulty as well.
![15](https://github.com/SamMureu/Game-Analysis-using-SQL/assets/84933401/c8379766-9932-43a8-8efc-810697e2c7b1)
