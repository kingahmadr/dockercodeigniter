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

sql environment, such as password in the .env file

How to use:
- please settings the required environment variable, such as database and user
- navigate to nginx-fpm directory
- run docker-compose up or docker-compose up -d
- check the container provisioning by running docker-compose ps

