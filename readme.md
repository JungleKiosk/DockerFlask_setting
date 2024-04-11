# First Docker Python Flask app


# Run Flask Dokerized app
1) docker-compose build web
2) docker-compose up web

problem:

C:\Users\Desktop\jk\Docker_Py_PgSQL_setting\back_end> docker-compose up web
[+] Running 1/1
 ✔ Container docker_py_pgsql_setting-web-1  Recreated                                                                                                            0.1s 
Attaching to web-1
Gracefully stopping... (press Ctrl+C again to force)
Error response from daemon: driver failed programming external connectivity on endpoint docker_py_pgsql_setting-db-1 (35bbd0e619d14826e576b2b4cd92b2de661e9f19b296fcf182a5f5cbbfff1879): Bind for 0.0.0.0:5433 failed: port is already allocated

* There was another Docker container in running on port :5433 this created conflict

**Resolution 1**: Stop the conflicting Docker container, keeping port :5433 in the repo's conteiner.
**Resolution 2**: change the port in the repo file docker-compose.yml from :5433 to 5434

# ------------------------------ #