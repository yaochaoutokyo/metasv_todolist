# metasv_todolist
1. metanet的查询接口有个小问题， 同一个块内的metanet交易无法确定版本先后， 因为没有blockIndex字段，且插入是并发的， 所以查询顺序并非ttor，需要加入blockIndex字段确保版本是ttor
