## Build docker container
```
docker build --tag "uvoo/ntlm-proxy:latest" .
```

## Generate self signed cert for https
```
openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout selfsigned.key -out selfsigned.crt -subj "/CN=app.example.com"
```

## Run
```
docker-compose up
```


### Edit etc/hosts as admin
```
notepad C:\Windows\System32\drivers\etc\hosts
```

```
sudo vim /etc/hosts
```

add line
```
127.0.0.1 app.example.com
```

# # Go to browser

http://localhost:8000/
https://localhost:8443/

