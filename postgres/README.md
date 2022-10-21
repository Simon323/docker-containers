## Info
  - pg_container -> postgres container name
  - root -> POSTGRES_USER
  - local_db -> DB name
  - local_db_10-02-2022... -> backup name, can change

## Run
  - docker-compose up

## Exit from docker bash
  - CTRL + C
  - CTRL + D

## Backup restore
  - docker exec -it pg_container bash
  - psql -U root your_project_db < /tmp/your_project_db_stage_yyyy_MM_dd.backup

## Get backup
  - docker exec -it pg_container bash
  - pg_dump -U root your_project_db > /tmp/your_project_db_`date +%d-%m-%Y"_"%H_%M_%S`.backup
  - pg_dumpall -c -U root > /tmp/your_project_db_`date +%d-%m-%Y"_"%H_%M_%S`.sql

## Connection between pg & admin:
  - run cmd
  - execute ipconfig /all
  - copy local ip address 192.168.x.x
  - use local ip as "Host name/address" in connection process

## Connect to external db:
  - host.docker.internal