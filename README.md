# xdb-guard

> 事务保护器, 保证事务在规定时间内结束

> spring 事务注解中有超时设置，但依赖于最后一个sql执行，如果在事务结束之前，有非sql的阻塞或者等待，如业务计算，死循环是无法保证事务在规定时间内结束

> 这里设计思想，监控事务方法，如果超时规定时间，kill mysql_thread_id

> 因为一些原因，代码暂时还不能放出

## 使用方法
- 通过注解@timeable即可
