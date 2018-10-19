# Install CM

CM is installed in node `sebce2.madrid.es`

#### Contents of `/etc/yum.repos.d`
![](../png/2_cm_yum_repos.png)

#### Prepare database
```
/usr/share/cmf/schema/scm_prepare_database.sh mysql --host sebce1.madrid.es scm scm scm
```
**Output**
![](../png/2_scm_prepare_database.png)

#### db.properties
```
cat /etc/cloudera-scm-server/db.properties
```
![](../png/2_scm_db_properties.png)
