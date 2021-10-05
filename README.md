Directory Structure
.
├── README.md
└── nginx-fpm
    ├── dbdata_home
    │   └── tajalapak.sql
    ├── docker-compose.yaml
    ├── mariadb
    │   └── Dockerfile
    ├── nginx-conf
    │   └── tajalapak.com.conf
    ├── php
    │   └── Dockerfile
    └── webdata

dbdata_home: home directory of mariadb container
nginx-conf: nginx web config
webdata: website root directoy

