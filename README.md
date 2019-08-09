## hongsea/ftp:1.0
FTP
'''
$ sudo docker pull hongsea/ftp:1.0
$ sudo docker run -d -v <directory>:/home/vsftpd \
-p 20:20 -p 23:21 -p 47400-47470:47400-47470 \
-e FTP_USER=admin \
-e FTP_PASS=admin \
-e PASV_ADDRESS=<ip address> \
--name ftp \
--restart=always hongsea/ftp:1.0
'''