## hongsea/ftp:1.0
# FTP
```
sudo docker pull hongsea/ftp
sudo docker run -d -v <Directory>:/home/vsftpd \
-p 20:20 -p 23:21 -p 47400-47470:47400-47470 \
-e FTP_USER=username \
-e FTP_PASS=password \
-e PASV_ADDRESS=<IP ADDRESS> \
--name ftp \
--restart=always hongsea/ftp
```
