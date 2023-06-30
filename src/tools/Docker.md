# Docker

Docker is software to run software in a container. Because it's in contained and easy to download an image, it's very easy to use software that's hard to set up or has been written (for Linux). If the software is run by a server, it's easy to use locally without having to know about setting up a server in language whatnot.

- Download [Docker desktop](https://www.docker.com/products/docker-desktop/)
- Use `WSL2` option during install.
  ![WSL2_Option](02%20docker%20options.png)
  ![Restart](03%20docker%20restart.png)
- Follow instructions when the Computer and Docker have restarted. 
  ![Install_WSL2](04%20docker%20installation%20wsl2.png)
- Open Windows Poweshell and use wsl 2 as standard
  ```
  wsl --set-default-version 2
  ```
  ![Use_WSL2_option](06%20powershell%20set%20wsl%20version%20succeeded.png)
- Pull (Download) the PlantUML server container by starting it with:
  ```
  docker run -d -p 8080:8080 plantuml/plantuml-server:jetty
  ```
  ![Plantuml_container_pull](plantuml_container.gif)
- Allow Windows firewall to use port 8080
  ![Windows_firewall_port_8080](10%20allow%20firewall%20to%20expose%20port%208080.png)
- In Docker Desktop you can now see the container running. As per the startup arguments it has connected port 8080 of the container to port 8080 of our computer.
  ![Running_PlantUML_server](11%20see%20container%20running.png)
- Browse to the adress [http://localhost:8080](http://localhost:8080) to use PlantUML server. This way you do not need to have access to the Internet in case you are working in a factory where access to the Internet is limited or unavailable.

If you have trouble accessing the container due to possibly other servers using the localhost 8080 port, please connect the container port `8080` to another local port like `8181` like so:
- When starting from the command line use the following startup command:
  ```
  docker run -d -p 8181:8080 plantuml/plantuml-server:jetty
  ```
- Or start the container from Docker desktop by choosing `Images -> plantuml/plantuml-server`, press the `run` button and change the port like so:
  ![Start_from_Docker_desktop](12%20docker%20start%20plantuml.png)

  ![Change_port](13%20docker%20change%20port.png)
- Browse to the adress [http://localhost:8181](http://localhost:8181) to use PlantUML server.
