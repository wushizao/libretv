services:
  libretv:
    image: bestzwei/libretv:latest
    container_name: libretv
    ports:
      - "8899:8080" # 将内部 8080 端口映射到主机的 8899 端口
    environment:
      - PASSWORD=${PASSWORD:-your_password} # 可将 9598 修改为你想要的密码，默认为 your_password
      - ADMINPASSWORD=${PASSWORD:-your_adminpassword} # 可将 9598 修改为你想要的密码，默认为 your_adminpassword
    restart: unless-stopped
