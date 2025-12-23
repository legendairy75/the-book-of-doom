- to start a container run:
- ```
  podman run -d \
    -p 8080:8080 \
    -v ~/my-conf.yml:/app/user-data/conf.yml \
    --name my-dashboard \
    --restart=always \
    lissy93/dashy:latest
  ```
	- Or run script in server
- this will open port 8080 on the device to dashy