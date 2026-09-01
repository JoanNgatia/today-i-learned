For databases like DynamoDB, to manage the read/write capacicty, and to have efficient queries, users can setup indexes for the specific keys that are retrieved most often. 

Learn more about:
- [ ] Indexes
- [ ] Throughput and setting up systems for future loads
- [ ] difference between partition/sort keys


### Indexes
#### 1. Global Secondary Index
Some applications might need to perform many kinds of queries, using a variety of different attributes as query criteria.To support these requirements, you can create one or more global secondary indexes and issue query requests against these indexes.
A global secondary index can have a different partition and sort key than the base table.
When new data is added to the table, the index updates itself. 
**** Precomputes sort of every 6 hours??


#### 2. Vector Index
Used to perform similarity search on DynamoDB tables. Can be used to store and search vector embeddings alongside existing data. 
Vector indexes support distance functions such as Euclidean, cosine, and dot product.
