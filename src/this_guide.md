# This guide...

... will show you how to set up a minimal system with which you can maintain your documentation about a project.

During this guide you will have to create your own local setup. When done successfully additional instructions for other tools, tips and tricks etcetera will appear.

For example:
- How to work together on a project by using Git.
- Learn about branching and merging branches.
- Excersize creating pull requests to your team's repository.
- Creating Sequence diagrams, State machines.
- Tips and tricks when working with Visual Studio Code.

```plantuml
@startdot
digraph NNN{

graph [bgcolor="transparent"] 

rankdir="LR";
node[shape="circle"]

start[shape="doublecircle"]
create_setup[label="create\nsetup"]
work_locally[label="work\nlocally"]
excersize

start -> create_setup
create_setup -> work_locally
create_setup -> create_setup [label="while\nreading"]
work_locally -> excersize
excersize -> excersize  [label="again and\nagain"]
excersize -> use
work_locally -> use
use -> work_locally

}
@enddot
```