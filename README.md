## hongsea/ftp:1.0

### Archlinux

### 1. Install package

```
sudo pacman -S docker
```

### 2. Start docker

```
sudo systemctl enable docker
sudo systemctl start docker
```

### 3. FTP(File Transfer Protocol) on docker container

- Download image from docker hub

    ```
    sudo docker pull hongsea/ftp
    ```

- Run FTP on this command, you need complate `<Directory>` path mount to docker for share, `<username>` and `<password>`

    ```
    sudo docker run -d -v <Directory>:/home/vsftpd \
    -p 20:20 -p 23:21 -p 47400-47470:47400-47470 \
    -e FTP_USER=<username> \
    -e FTP_PASS=<password> \
    -e PASV_ADDRESS=<IP ADDRESS> \
    --name ftp \
    --restart=always hongsea/ftp
    ```
