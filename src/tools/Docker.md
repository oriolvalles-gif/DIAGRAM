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

