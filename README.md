# Load testing homework:

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
