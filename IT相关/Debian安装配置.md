# Debian 安装配置
+ 下载镜像：在国内安装Debian时会因为网络导致安装太慢或安装失败的情况，因此下载镜像不要选择网络安装镜像。下载镜像建议去国内开源的镜像站下载。
+ 用户权限：完成安装后，将当前用户（any-user）添加到sudo用户组。`usermod -aG sudo any-user`。配置生效需要注销后重新登陆。
+ 换软件源：将/etc/apt/source.list进行备份，将其中内容替换成国内开源镜像。
  - 直接使用https可能无法解析，需先使用http的镜像安装解析https的软件`apt install apt-transport-https ca-certificates`
  - 安装完上述两个软件，建议将镜像切换回https镜像。
+ 更新软件：`apt update`，`apt upgrade`
