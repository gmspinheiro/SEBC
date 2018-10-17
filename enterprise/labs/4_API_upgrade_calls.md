# CM Upgrade
Backups of the Cloudera Managment Services and support databases were performed on host `sebct1` and are located in the `/root/cm_upgrade_2018-10-17-CM` directory.

The image below showcases the previous installed version of Cloudera Manager.

![](../png/4_cm_old_version.png)

## API Calls
#### API Version
`curl -u gmspinheiro:cloudera http://localhost:7180/api/version`

![](../png/4_api_version.png)

#### CM Version
`curl -u gmspinheiro:cloudera http://localhost:7180/api/v19/cm/version`

![](../png/4_cm_version.png)

#### CM Users
`curl -u gmspinheiro:cloudera http://localhost:7180/api/v19/users`

![](../png/4_users.png)

#### CM Database
`curl -u gmspinheiro:cloudera http://localhost:7180/api/v19/cm/scmDbInfo`

![](../png/4_cm_database.png)
