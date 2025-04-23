# Day-8---SQL-learning-journal-

## Task 3: Ken Griffey Jr. Home Run History

**Objective:**  
Retrieve and display the number of home runs Ken Griffey Jr. hit each year, sorted by the most recent year first.

### **SQL Query Explanation:**
```sql
SELECT performances.year, performances.HR
FROM performances
JOIN players ON performances.player_id = players.id
WHERE players.first_name = 'Ken'
  AND players.last_name = 'Griffey'
  AND players.birth_year = 1969
ORDER BY performances.year DESC;
Step-by-Step Breakdown:
SELECT performances.year, performances.HR
We select the columns year and HR (home runs) from the performances table.

FROM performances
The query starts by looking at the performances table, which tracks stats like home runs, hits, and more for each player per year.

JOIN players ON performances.player_id = players.id
This part connects the performances table to the players table using the player_id column (from performances) and the id column (from players).

WHERE players.first_name = 'Ken' AND players.last_name = 'Griffey' AND players.birth_year = 1969
Filters the results to include only the player with the first name "Ken", last name "Griffey", and born in 1969 (to distinguish between Ken Griffey Jr. and Sr.).

ORDER BY performances.year DESC
Sorts the results by the year in descending order (most recent year first).

Key Takeaways:
JOIN: Merges two tables based on a common column (player_id and id).

Filtering: Use WHERE to narrow down results to the specific player.

Sorting: Use ORDER BY to control the order of the results.

