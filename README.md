# Session 2

**Testing:**
1) Clone the assignment repo and run docker-compose as below:

````sh
$ git clone https://github.com/mostafaismail/session_2.git
$ cd session_2
$ docker-compose up -d
````

2) Make sure that all 3 contianers are up and running:

```sh
$ docker container ls
CONTAINER ID        IMAGE                               COMMAND                  CREATED             STATUS                      PORTS                    NAMES
647f7c1b8fa1        mostafaismail/session_2_prj_nginx   "nginx -g 'daemon of…"   25 minutes ago      Up 25 minutes               0.0.0.0:80->80/tcp       nginxserver
9a9453c2ea26        session_2_prj_app2                  "catalina.sh run"        25 minutes ago      Up 25 minutes (unhealthy)   0.0.0.0:6062->8080/tcp   cont-app2
035195a3967e        mostafaismail/session_2_prj_app1    "catalina.sh run"        35 minutes ago      Up 25 minutes (unhealthy)   0.0.0.0:6061->8080/tcp   cont-app1
````

3) Verity the deployment by navigating to the below URL's using your preferred browser:

- http://localhost/
> It should preview Nginx home page

- http://localhost/app1
- http://localhost/app2
> It should preview application page "DevOpsArea Java Sample Project 1" or "DevOpsArea Java Sample Project 2" respectively.
