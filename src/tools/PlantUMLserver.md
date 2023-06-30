# PlantUML server

Follow these instructions to install the PlantUML docker container. Using a container allows ease of running a local server. This way you do not need to have access to the Internet in case you are working in a factory where access to the Internet is limited or unavailable.

- Pull (Download) the PlantUML server container by starting it with:
  ```
  docker run -d -p 8080:8080 plantuml/plantuml-server:jetty
  ```
  ![Plantuml_container_pull](plantuml_container.gif)
- Allow Windows firewall to use port 8080
  ![Windows_firewall_port_8080](10%20allow%20firewall%20to%20expose%20port%208080.png)
- In Docker Desktop you can now see the container running. As per the startup arguments it has connected port 8080 of the container to port 8080 of our computer.
  ![Running_PlantUML_server](11%20see%20container%20running.png)
- Browse to the adress [http://localhost:8080](http://localhost:8080) to use PlantUML server. 

If you have trouble accessing the container due to possibly other servers using the localhost 8080 port, please connect the container port `8080` to another local port like `8181` like so:
- When starting from the command line use the following startup command:
  ```
  docker run -d -p 8181:8080 plantuml/plantuml-server:jetty
  ```
- Or start the container from Docker desktop by choosing `Images -> plantuml/plantuml-server`, press the `run` button in the top right corner and change the port like so:

  ![Change_port](13%20docker%20change%20port.png)
- Browse to the adress [http://localhost:8181](http://localhost:8181) to use PlantUML server.