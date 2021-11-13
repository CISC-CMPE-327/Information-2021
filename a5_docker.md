## :ship: SHIP the Container!!

Now let's ship it!! Deploying a web application is not easy. By using docker containers, we can bundle all the dependencies into a single image. Follow the steps below:

1. Install and start docker. Think of it as a virtual machine (well on linux it is on the same host but different namespace but you can `treat` it as a virtual machine for now). 
2. Get used to some typical commands:
 - `docker ps` # list running processes and their containers 
 - `docker kill ps_id` # kill a process
 - `docker image list` # list out available images
 - `docker kill $(docker ps -q) ` kill all processes in docker containers
3. check out [here - cli](https://github.com/CISC-CMPE-327/Python-CI-2021/pull/8/files) or [here - web](https://github.com/CISC-CMPE-327/Python-CI-2021/pull/7/files) to see changes we made in the web application source code. Specifically make sure that you understand why:
   - `qbay/__init__.py `: we added `db_string` variable that is read from the environment. This allow us to use a different database such as MySQL than the original single database file. 
   - `qbay/__main__.py `: we added the `host='0.0.0.0'` to the main function so you can access the web application using all IP addresses on the host rather than just `127.0.0.1`. (for example, your laptop/host also has an IP from the router 192.0.0.1 you can use that to visit your app as well)
   - `requirements.txt` : added `pymysql` library to enable us connecting to a MySQL database
   - `wait-for-it.sh ` : (web option only) a bash file that will wait for certain port to be open before running some commands. You don't need to understand what is inside. We use this to wait for the MySQL database server is ready before starting our web application in the deployment. 
   - `Dockerfile ` : define what is installed and included in the container for our web application. Basically the `FROM` statement defines the base image, then we just install dependencies and copy the application over the image. We also copy the `wait-for-it.sh ` file there for later use. The `EXPOSE 8081` statement means that the container will expose its port 8081 to the outside of the container. So we can visit the app with our host.
   - `docker-compose.yml `: define all the services (our web app, SQL server, and the database web UI) and all the resources (data storage volumn & network) to be deployed
   - `db_init.sql` : database initialization file for a proper database such as MySQL. (basically we only created a database using this script)
   - `.gitignore` : stop tracking some data files (as well as the data folder for MySQL to be created later). 
4. Apply the chances above to your own project. Please make sure that files are in the right path (e.g. `Dockerfile` is in the same folder as the `qbay` folder). Or you can change the paths in `Dockerfile`. 
   - For Windows users, make sure wait-for-it.sh file's linebreak is set to LF since the it will be ran on linux.
6. Register your company/group on dockerhub. We will use it to store the image so you can deploy it anywhere! Then on dockerhub, create a **public** repostiroy (usually it is your application name)
7. Compile your image: `docker build --tag=your_docker_hub_name/your_docker_hub_repo_name:version_info .` For example, `docker build --tag=test_company/app:v1 .`
8. Once done, you will find your image by `docker image list`
9. You can run your web application by  
   - web option: `docker run -p 8081:8081 your_docker_hub_name/your_docker_hub_repo_name:version_info python3 -m qbay`. For example: `docker run -p 8081:8081 test/app:v1 python3 -m qbay`.
   - cli option: `docker run -ti your_docker_hub_name/your_docker_hub_repo_name:test_cli python -m qbay`
   - you can build the image with different versions. If you put the same version, it will just overwrite the original one.
   - when running the container, `-p 8081:8081` means we map the port 8081 of the container to 8081 of the host. `python3 -m qbay` is the command to be run in the container (which starts our application)
10. Publishing your web application container
   - use `docker login` command to login
   - use `docker push your_docker_hub_name/your_docker_hub_repo_name:version_info` to push your image to the hub repository. You should be able to see the image on your docker hub page.

9. Now, anywhere (e.g. your friends machine), you can run your web application with docker by follwoing commands, without worrying about the platform, python versions etc. 
 - `docker pull your_docker_hub_name/your_docker_hub_repo_name:version_info` 
 - `docker run -p 8081:8081 your_docker_hub_name/your_docker_hub_repo_name:version_info python3 -m qbay`


## :ship: SHIP the WHOLE SYSTEM

However, we don't stop from a single container deployment. In a lot of situtations, your applicaton (or it is now more like a system) consists of a lot of micro-services and applications. For example, here we have our web application services and we also want a proper database service to serve millions of users. Additionally, we want to add web interface so we can easily manage the database. Now our system consists of these services:
 - `qbay-web`: (web-option) Flask web application (including frontend and backend, in reality people like to further break backend into different independent services)
 - `qbay-cli`: (cli-option) CLI application
 - `qbay-db` : MySQL database
 - `phpmyadmin`  : Web interface for MySQL
These services are all defined in our `docker-compose.yml` file. 
It also defines some resources:
  - `qbay-site` : the network connects everything
  - volumes mounted to the MySQL database instance, including the folder for database data and the database initialization file for MySQL. 
1. The only thing you need to change in the `docker-compose.yml` file is the `image` property of the `qbay-web:`/`qbay-cli` service. It should point to your own image i.e. `your_docker_hub_name/your_docker_hub_repo_name:version_info`. 
2. To run the WHOLE system just issue `docker-compose up`. Then everything should start!! You will see a new folder `mysql_data` created for data store. 
  - web app is running at `0.0.0.0:8081` 
  - for CLI application, you should execute `docker-compose exec qbay-cli python -m qbay` on a seperate terminal
  - database web interface is running at `127.0.0.1:8082`. user name `root`, password `root`, server `qbay-db`. (all of these are defined in the docker compose file). 
  
  NOTE: When running `docker-compose up` you may come accross an error: `ERROR: for qbay-db  Cannot start service qbay-db: Mounts denied: approving PATH/db_init.sql: file does not exist`. If this happens it can be fixed by disabling `Use gRPC FUSE for file sharing` in the Docker Desktop app. Setting can be accessed by `Docker Desktop-> Preferences -> Experimental Features ->Use gRPC FUSE for file sharing`.
