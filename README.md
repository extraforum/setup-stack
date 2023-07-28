# Install Stack

**Stacks** that must be installed for this project include


# 1. Docker

![Docker](https://d1.awsstatic.com/acs/characters/Logos/Docker-Logo_Horizontel_279x131.b8a5c41e56b77706656d61080f6a0217a3ba356d.png)

Access this website address to download docker:
```sh
https://www.docker.com/
```
[Go to Docker website](https://www.docker.com/)
## download and install docker desktop
To check if **docker** has been successfully installed on your machine, use the command:
```sh
docker --version
```
# 2. Install stacks with Docker
Clone this [repository](https://github.com/extraforum/setup-stack) to your computer then install the stack using the command:
```sh
docker compose up
```
After docker successfully build the container, go to docker desktop to check the stacks in the container stacks and then proceed to setup for each technology.
## 2.1. PostgreSQL
**Docs**: https://www.postgresql.org/docs/
<img src="https://images.g2crowd.com/uploads/product/image/large_detail/large_detail_251be2af3ae607c45c14e816eaa1cf41/postgresql.png" alt="PostgreSQL" width="200"/>

### Connect:
Access the address to access **PgAdmin4** http://localhost:5050/ 

Username: root@root.com

Password: root

**Step 1:** Click on  **Add New Server** >

**Step 2:** in the **General** tab enter name: **DB** >

**Step 3:** Open your terminal and enter command
```sh
docker interpise stacks-postgresql-1
```
copy the value of **"IPAddress"**, it has the format like ***172.21.0.5***, it may be different on your machine >

**Step 4:** in the **Connection** tab enter **hostname/address**: Paste the copied **IPAddress** value, **password**: root >

**Step 5:** Click **Save** > Done!
## 2.2. Redis
**Docs**: https://redis.io/docs/
<img src="https://topdev.vn/blog/wp-content/uploads/2019/05/Redis-1.png" alt="PostgreSQL" width="300"/>
### Login:
Access the address to access **RedisInsight**  http://localhost:8001/

Agree all **EULA AND PRIVACY SETTINGS** > click **CONFIRM**

**Step 1:** Click on  **I already have a database** >

**Step 2:** Click on  **Connect to a Redis Database** > 

In the tab **ADD REDIS DATABASE** enter the fields:
* Host: redis
* Port: 6379
* Name: redis

**Step 3:** Click on  **ADD REDIS DATABASE** > Done!
## 2.3. RabbitMQ
**Docs**: https://www.rabbitmq.com/documentation.html/

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/71/RabbitMQ_logo.svg/2560px-RabbitMQ_logo.svg.png" width="320"/>

### Login:
Access the address to access **RabbitMQ Management**  http://localhost:15672/

Username: root

Password: root
## 2.4. Jenkins
**Docs**: https://www.jenkins.io/doc/

<img src="https://tel4vn.edu.vn/uploads/2020/07/jenkins_logo.png" width="300"/>

### Get Administrator password:
Open your terminal and run the command line:
```sh
docker logs stack-jenkins-1
```
terminal will display a result like this:
```sh
*************************************************************
*************************************************************
*************************************************************

Jenkins initial setup is required. An admin user has been created and a password generated.
Please use the following password to proceed to installation:

50557c2b66214f229d1fbc5de73e321b

This may also be found at: /var/jenkins_home/secrets/initialAdminPassword

*************************************************************
*************************************************************
*************************************************************
```
***50557c2b66214f229d1fbc5de73e321b*** is your Administrator password, copy it!

### Unlock Jenkins:
Access the address to access **Jenkins**  http://localhost:8080/

**Step 1:** Paste the Administrator password you copied into the Administrator password field > click **Continue** >

**Step 2:** In the **Customize Jenkins** tab select **Install suggested plugins** > 

**Step 3:** Wait for Jenkins to download the plugins > 

**Step 4:** In the Create First Admin User tab, enter the relevant information > click **Save and Continue** >

**Step 5:** Click **Save and Finish** > click **Start using Jenkins** > Done!
