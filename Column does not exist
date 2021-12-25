-- Second query

-- Add the new column to the select statement
SELECT PlayerName, 
       Team, 
       Position, 
       AvgRebounds -- Add the new column
FROM
     -- Sub-query starts here                             
	(SELECT 
      PlayerName, 
      Team, 
      Position,
      -- Calculate average total rebounds
     (ORebound+DRebound)/CAST(GamesPlayed AS numeric) AS AvgRebounds
	 FROM PlayerStats) tr
WHERE AvgRebounds >= 12; -- Filter rows
