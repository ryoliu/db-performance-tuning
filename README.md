# 資料庫效能調校專案成果

透過 SQL 分析、執行計畫判讀與索引調校，改善 SQL Server 與 Oracle 資料庫的資源使用效率。

## SQL Server CPU 效能改善

分析高 CPU 查詢，依不區分大小寫的定序特性移除篩選欄位上不必要的 `LOWER()` 運算，並調整及補建索引，將平均 **CPU 使用率由約 22% 降至 3%**，尖峰 **由約 90% 降至 23%**。

[查看 SQL Server 專案說明與監控比較圖](sql-server-performance-tuning.md)

## Oracle SQL 效能優化

運用 AWR 與 Autotrace 找出高 I/O SQL，分析並建立適當索引，在還原的測試環境將 Full Table Scan 改為 Index Range Scan 搭配回表存取，單次 **Logical I/O（Consistent Gets）由 97,601 降至 368，減少約 99.6%**。

[查看 Oracle 專案分析與調校成果](oracle-sql-performance-tuning.md)
