# Docker and PlantUML server container

For installation of Docker and the PlantUML server container follow indstructions of the screenshots `01 .. ` to `11 .. ` in the folder `src/images/docker_install`. Because the PlantUML server container exposes port `8080` as standard, you can access the container by opening a new internet client and go to the adress http://localhost:8080 to use the server.

If you have trouble accessing the container due to possibly other servers using the localhost 8080 port, please follow instructions of images `12 .. ` and `13 .. ` to change the port.

# Setup of PlantUML extension

- in `VS Code` open the settingd by `CRTL` + `,`
- search for `plantuml` in the search box
  
  ![VSCodePlantUmlSetting](../../images/code_plantuml_settings.png "PlantUML settings")

- Choose `PlantUMLServer` for renderer.
- Change the URL of the server to the correct adress of the PlantUML server docker container.

Try [making a very simple diagram ](../../Usage.md#create-a-plantuml-picture)