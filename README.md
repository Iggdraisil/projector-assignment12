# Load testing homework:

## To launch run: 
- `docker-compose up --build`
- Oridnary cache: `siege -b -t10m -c300 'http://127.0.0.1:9000/cache'`
- Probabilistic eviction cache: `siege -b -t10m -c300 'http://127.0.0.1:9000/cache'`



## Results Table
### 17:20-17:30 - ordinary cache;
### 16:35-16:45 - cache with probabilistic eviction;
![image](https://user-images.githubusercontent.com/44341837/228574713-0cd44b1d-6aa1-4a29-9882-cbf6b3ab26e0.png)

### *Probabilistic cache*:
```
Transactions:                5154153 hits
Availability:                 100.00 %
Elapsed time:                 600.71 secs
Data transferred:            2369.33 MB
Response time:                  0.01 secs
Transaction rate:            8580.10 trans/sec
Throughput:                     3.94 MB/sec
Concurrency:                   98.95
Successful transactions:     5154408
Failed transactions:               0
Longest transaction:            3.26
Shortest transaction:           0.00
```

### *Ordinary cache*
```
Transactions:                2474214 hits
Availability:                 100.00 %
Elapsed time:                 600.16 secs
Data transferred:            1137.32 MB
Response time:                  0.04 secs
Transaction rate:            4122.59 trans/sec
Throughput:                     1.90 MB/sec
Concurrency:                  181.03
Successful transactions:     2474214
Failed transactions:               0
Longest transaction:          304.96
Shortest transaction:           0.00

```
