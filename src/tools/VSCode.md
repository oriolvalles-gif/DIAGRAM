# Visual Studio Code

For writing the documentation we'll use Microsoft's Visual Studio Code. This is an IDE with various plug-ins that will help with the writing process.
Because we're not hindered by word processor software like Microsoft Word we can focus on the content and because we write in plain text, we can use Git for revisions, merging work by multiple authors, and have it displayed (rendered) in various tools.

- Download and install [Microsoft Visual Studio Code](https://code.visualstudio.com/).
- Open Microsoft Visual Studio Code (from now on abbreviated as `VS Code`).
- Open the `Extensions` tab on the left and search for packages that will help with the workflow.
 
  ![Extensions](code_extensions.png "Visual Code Extensions")
- Install `PlantUML`
  
  ![PlantUML](code_plantuml.png "PlantUML")

- Install `GitLens`

  ![GitLens](code_gitlens.png "GitLens")

- Install `Markdown All in One`
  
  ![MarkdownAllinOne](code_markdownallinone.png "Markdown All in One")

# Setup of PlantUML extension

- in `VS Code` open the settingd by `CRTL` + `,`
- search for `plantuml` in the search box
  
  ![VSCodePlantUmlSetting](code_plantuml_settings.png "PlantUML settings")

- Choose `PlantUMLServer` for renderer.
- Change the URL of the server to the correct adress of the PlantUML server docker container.

Try [making a very simple diagram ](../usage/PlantUML.md)
