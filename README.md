# metasv_todolist
1. metanet的查询接口有个小问题， 同一个块内的metanet交易无法确定版本先后， 因为没有blockIndex字段，且插入是并发的， 所以查询顺序并非ttor， 需要加入blockIndex字段确保版本是ttor

2. 部分outputIndex为0， 而gorm默认不存储默认值， 导致数据库内值为null， 需要使用指针来存储domain变量。

3. 一些涉及到翻页逻辑的索引需要倒序
