# backend
 
##### To start redis server
```docker run -d --name redis-stack-server -p 6379:6379 redis/redis-stack-server:latest```

##### To start redis server with redis stack
```docker run -d --name redis-stack -p 6379:6379 -p 8001:8001 redis/redis-stack:latest```


## System Design
![Dashboard Page](./System%20Design/Socket.io%20dash%20design.svg)
![Board Page](./System%20Design/Socket.io%20board%20design.svg)


![image](https://github.com/user-attachments/assets/af54e763-319d-4e8c-8136-eb776bb42a70)
![image](https://github.com/user-attachments/assets/997f9882-97f3-464f-9ca2-3477aae3e8c3)

The reason behind using FirebaseToRoomMap is because redis doesn't let you set expiry on hashmap keys
So FirebaseToRoomMap maps the owner's firebase uid to the actually room keyvalue object, on which the expiry is set.
