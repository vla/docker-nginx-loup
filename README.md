# About this Repo

with openssl , lastest integrated ngx_devel_kit, luajit, ngx_cache_purge, 
nginx_upstream_check_module

# Usage

```
$docker run -p 80:80 --name nx -d johnwu/nginx-loup 

```

## Configuration
```
$ docker run --name nx -v /some/nginx.conf:/etc/nginx/nginx.conf:ro -d johnwu/nginx-loup 

```

# Sample

```
$docker run -p 80:80 --name nx -d johnwu/nginx-loup nginx -g "daemon off;" -c /etc/nginx/test.conf 

```

Try to access the URL address below

```
http://localhost
http://localhost/index.html
http://localhost/purge/index.html
```

Response to the agent

```
http://localhost/lua
```

Demonstrate the Lua script

```
http://localhost/status1
```

stub status

```
http://localhost/status2
```

upstream status


