# Distributed Database Caching Service

## Project Overview

This project focuses on optimizing server performance by developing a distributed database caching service. The primary goal is to reduce the load on database queries and enhance response times, using a combination of Flask, NodeJS, and MongoDB as the backend. The caching service is designed to handle large datasets efficiently through region-based distribution and a timestamp-based caching mechanism.

## System Architecture

### Caching Service Design

- **Timestamp-Based Cache:** 
  - Manages cache entries based on timestamps to ensure data freshness.
  - Reduces the frequency of database queries by storing recently accessed data in the cache.

- **Distributed LRU Key-Value Stores:** 
  - Cache is divided by regions, each using a Least Recently Used (LRU) algorithm to manage key-value pairs.
  - Optimizes cache usage by evicting the least recently used entries when the cache is full.

- **Region-Based Distribution:** 
  - Improves scalability by dividing the cache into multiple regions.
  - Each region operates independently, allowing for parallel processing and reducing bottlenecks.

### Server Optimization

- **Load Reduction:** 
  - Caching frequently accessed data significantly reduces the number of queries sent to the database.
  
- **Response Time Improvement:** 
  - The distributed caching mechanism combined with the LRU algorithm minimizes data retrieval times.

- **Performance Analysis:** 
  - Comprehensive performance analysis was conducted, including metrics like response time, cache hit rate, and load reduction.

## Key Features and Implementations

### Timestamp-Based Caching

- **Cache Expiry:** 
  - Entries in the cache are timestamped to control their validity, ensuring only current data is served.
  
- **Efficient Lookup:** 
  - Data retrieval is optimized by checking the cache before querying the database.

### Distributed LRU Key-Value Stores

- **Region Segmentation:** 
  - Cache is divided into distinct regions, each with its own LRU store to improve management and scaling.

- **LRU Algorithm:** 
  - Maintains only the most relevant entries by evicting the least recently used data when the cache reaches capacity.

### Performance Analysis

- **Response Time Measurement:** 
  - Quantified the improvement in response time, showing a 20-30% faster response time compared to the baseline.
  
- **Cache Hit Rate:** 
  - Monitored the cache hit rate to assess the effectiveness of the caching strategy.
  
- **Load Reduction Metrics:** 
  - Evaluated the reduction in database load due to the caching service.

## Conclusion

The development of this distributed database caching service has led to significant improvements in server performance and efficiency. By implementing a timestamp-based cache and distributed LRU key-value stores, the system achieves faster response times and reduced database load. Performance analysis confirms a 20-30% improvement in response time, highlighting the effectiveness of the caching strategies.

## Tools & Concepts Used

- **Flask**
- **NodeJS**
- **MongoDB**
- **Distributed Systems**
- **Caching**
