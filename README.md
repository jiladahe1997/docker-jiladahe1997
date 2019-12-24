# docker-jiladahe1997
A docker set for my website, including nginx、nodejs、and java


# 简介
## nginx-main：

docker-hub地址：https://hub.docker.com/r/jiladahe1997/nginx

此docker用于转发请求到腾讯云cos云存储，提供前端纯静态页面。

## nginx-proxy：

docker-hub地址：https://hub.docker.com/r/jiladahe1997/nginx-proxy

此docker是用于亚马逊服务器转发到阿里云服务器，用于绕过国内域名必须备案的限制。