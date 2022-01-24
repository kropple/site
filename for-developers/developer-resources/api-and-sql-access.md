---
description: >-
  AnyBlock Analytics (eth.events) offers access to GC through ElasticSearch and
  the ability to query a SQL Database.
---

# API & SQL Access with AnyBlock Analytics

1\) Go to [https://account.anyblock.tools/auth/login/](https://account.anyblock.tools/auth/login/) and sign up for a free account.

![Login to create an account](../../.gitbook/assets/aa\_free\_acct.png)

2\) You will receive an API key and SQL username/password.

## ElasticSearch

* Your API key is used to replace `$mytoken` in standard queries.&#x20;
* Queries to the GC use the xdai eth.events endpoint:   [https://api.eth.events/ethereum/xdai/mainnet/es/](https://api.eth.events/ethereum/xdai/mainnet/es/block/search/)
* Example Queries are located here: [https://www.anyblockanalytics.com/docs/elastic/example-queries/](https://www.anyblockanalytics.com/docs/elastic/example-queries/)
* Documentation regarding ElasticSearch API calls is available here: [https://www.anyblockanalytics.com/docs/elastic](https://www.anyblockanalytics.com/docs/elastic/)

For example, this curl query will show us data about the last 2 blocks.

```
curl -X POST \
https://api.eth.events/ethereum/xdai/mainnet/es/block/search/ \
-H 'Authorization: Bearer $mytoken' \
-H 'Content-Type: application/json' \
-d '{
  "sort": {
    "number.num": "desc"
  },
  "size": 2
}'
```

## SQL Access

1\) Download a SQL client Anyblock Analytics favors [PGAdmin4](https://www.pgadmin.org/download/)

2\) Click on Server -> Create -> Server

![](../../.gitbook/assets/servers.png)

3\) In the **General** Tab, choose a **Name** for your server instance

![](../../.gitbook/assets/xdai\_server.png)

4\) Go to the **Connection** Tab, and fill in the information from your AnyBlock Analytics Account and click **Save**:

|                      |                                                           |
| -------------------- | --------------------------------------------------------- |
| Host name.address    | sql.anyblock.tools                                        |
| Port                 | 45432                                                     |
| Maintenance database | ethereum\_ethereum\_mainnet (or another db from the list) |
| Username             | _\<your\_username>_                                       |
| Password             | _\<your\_password>_                                       |

5\) You will see a list of all databases.

1. Click on **ethereum\_poa\_xdai** to interact with xDai data.&#x20;
2. To Query the DB, go to Tools -> Query Tool

![Access the Query Tool](../../.gitbook/assets/query\_tool.png)

6\) **Try a Query!**

1. Check you are in the GC xDai database
2. Enter your Query (this query shows info about the most recent block)
3. Click the lighting icon to execute
4. Output from query

![Run query with the lightning icon](../../.gitbook/assets/query.png)

7\) Explore different queries and information in the SQL documentation and tutorials available here: [https://www.anyblockanalytics.com/blog/basic-sql-usage-examples/](https://www.anyblockanalytics.com/blog/basic-sql-usage-examples/)

**Example Query to find transactions for the EternalStorageProxy token contract**

```
SELECT * FROM tx
WHERE tx.to = '0x7301CFA0e1756B71869E93d4e4Dca5c7d0eb0AA6'
LIMIT 50
```
