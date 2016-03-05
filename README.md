# WEBLOGIC--PROTOCOL-VIOLATION-ISSUE

This is quite different where the heap memory did not reach the peak utilization but the Managed servers reach 75% often and get back to normal. Heap reaching 75% is not an issue in usual JVM behaviour, but in our application we have configured in such a way that the node is put on STANDBY when the hap utilization increases to 75%. 
The heap dump will help you to identify the issue only when the memory increases to peak utilization. We had touch time in nailing down the issue.
Initially we analysed the thread dumps taken during the issue reported time period. We could find requests were getting struck during the Weblogic servers trying to connect to database. 
The issue can occur when there is change in JDBC driver, Database Upgrade and other firewall or network related changes in the environment.

