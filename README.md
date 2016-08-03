# Supported tags and respective `Dockerfile` links

- [`latest` , `0.1`  (0.1/Dockerfile)](https://github.com/vla/docker-nginx-loup/blob/master/Live/Dockerfile)

# About this Repo

nginx-1.10.1集成openssl-1.0.2h静态编译，集成LuaJIT-2.0.4、lua-nginx-module-0.10.1、nginx_upstream_check_module、ngx_cache_purge-2.3、ngx_devel_kit-0.3.0。

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

测试URL如下

```
http://localhost
http://localhost/index.html
http://localhost/purge/index.html
```

查看方向代理是否成功，并且清理index.html缓存


```
http://localhost/lua
```

测试LUA脚本是否可运行

```
http://localhost/status1
```

stub状态

```
http://localhost/status2
```

upstream 状态