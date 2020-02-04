# docker-jiladahe1997
A docker set for my website, including nginx、nodejs、and java


# 简介 
## nginx-main： 

docker-hub地址：https://hub.docker.com/r/jiladahe1997/nginx

此docker用于转发请求到腾讯云cos云存储，提供前端纯静态页面。

## nginx-proxy：

docker-hub地址：https://hub.docker.com/r/jiladahe1997/nginx-proxy

此docker是用于亚马逊服务器转发到阿里云服务器，用于绕过国内域名必须备案的限制。

运行命令（带ssl证书）：docker run -dt -p 80:80 -p 443:443 -v /etc/letsencrypt/archive/jiladahe1997.cn:/usr/src/app/ssl_certificate jiladahe1997/nginx-proxy

# 自动化CI:

通过github action，实现半自动CI，详情见目录下的：.github/workflows。

每次push后，会自动build一个docker image，自动上传到[docker hub](https://hub.docker.com/repository/docker/jiladahe1997/nginx)。然后需要手动去服务器上重新拉一下image。

TODO: 不要手动去服务器拉，通过docker swarm的API实现自动拉拉取