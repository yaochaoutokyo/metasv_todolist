# metasv_todolist
1. metanet的查询接口有个小问题， 同一个块内的metanet交易无法确定版本先后， 因为没有blockIndex字段，且插入是并发的， 所以查询顺序并非ttor， 需要加入blockIndex字段确保版本是ttor。 [done]

2. 部分outputIndex为0， 而gorm默认不存储默认值， 导致数据库内值为null， 需要使用指针来存储domain变量。 [done]

3. 一些涉及到翻页逻辑的索引需要倒序。 [done]

4. https://api.metasv.com/v1/address/1P3GQYtcWgZHrrJhUa4ctoQ3QoCU2F65nz/utxo UTXO的确认高度更新有bug [done]

5. https://api.metasv.com/v1/address/13E51hwkRV7NzK8N8s6JxccLH4yJQCurtX/utxo 确认的UTXO统计不对 [done]
