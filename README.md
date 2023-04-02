# Redis homework:

# Eviction policies:
- ### Noeviction - redis retunr an error when memory limit is reached
- ### volatile-lru - inserts without ttl are returning errors, through inserts with ttl are ok, hence least recently used keys are evicted
![image](https://user-images.githubusercontent.com/44341837/229371338-41897c1f-ba23-4dee-b9e4-30feecf286e4.png)
- ### allkeys-lru all insets are successful, as keys which are least recently used are expired
![image](https://user-images.githubusercontent.com/44341837/229371755-f3266ecb-3ff5-43cd-a55a-9cbd4aa95e09.png)
- ### volatile-lfu - inserts without ttl are returning errors, through inserts with ttl are ok, hence least frequently used keys are evicted


# Caching:

## To launch run: 
- `cp sentinel-template/* sentinel`
- `docker-compose up --build`
- Oridnary cache: `siege -b -t10m -c300 'http://127.0.0.1:9000/cache'`
- Probabilistic eviction cache: `siege -b -t10m -c300 'http://127.0.0.1:9000/cache'`



## Results Table
### Ordinary cache
![image](https://user-images.githubusercontent.com/44341837/229362983-b16876c0-21cd-4a9d-942a-51d5e23ae6e5.png)


### Cache with probabilistic eviction
![image](https://user-images.githubusercontent.com/44341837/229362136-70139742-2e33-4527-8d39-68d066827c3b.png)
