```sql
SELECT count(responseTime) as Count, mean(responseTime) as Avg, min(responseTime) as Min, median(responseTime) as Median, percentile(responseTime, 90) as "90%",percentile(responseTime, 95) as "95%",percentile(responseTime, 99) as "99%", max(responseTime) as Max, (sum(errorCount)/count(responseTime)) as "Error Rate" FROM "requestsRaw"  WHERE $timeFilter GROUP BY requestName
```