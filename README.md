# Islands

Your mission, should you accept:

1) Download install.sql and execute it an a database of your choosing. It creates the `dbo.OrderProduct` table and inserts a "few" rows.
2) The company has been running different marketing campaigns and now they want to know which one was the most successfull. For that the need to know the longest stretch of consecutive orders (by product).
3) Write a query that finds the product that has the longest stretch of consecutive orders and return the product_id, the number of days that were part of the stretch and the start and end date of the same.
4) To confirm that you found the right result, execute `SELECT CHECKSUM(ppp,lll);` replacing ppp with the product_id and lll with the length in days. It should result in 8160.
5) Measure the total number of logical reads your query used to find the two suppliers. Report that number to me as soon as you have it.
6) Bonus: Also return - within the same query - the product that had the longest order gap together with the length in days of that gap. (the same checksum calculation should result in 1271 for the gap.


The team with the lowest number of logical reads wins. In case of a tie, the team that solve the bonus wins. Still a tie? The first submission wins. 

**Make sure you send me your number of reads and query (privately!), as soon as you have the correct result.**

For reference, I came up with several solutions using 1784 reads (1874 with paralelism enabled). The slowest executed in about 1 second, the fastest finished after about 330 ms. (That's in a VM with access to 3 CPU cores on my laptop.)

Good Luck!
