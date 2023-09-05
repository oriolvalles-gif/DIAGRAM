# Forking a repository

Try to understand the diagrams below. The first one is a `use case diagram` that shows interactions between actors.

```plantuml
@startuml

skinparam backgroundColor transparent
left to right direction

:you:
:team\nmember:

':you: -> (upstream\nrepository)
:you: -> (forked\nrepository)
:you: -> (clone\nrepository\nlocally)
:team\nmember: -> (clone\nrepository\nlocally)
:you: -> (push\nmodified\nrepository)
:you: -> (commit\nchanges)

(upstream\nrepository) ..> (forked\nrepository)
(forked\nrepository) ..> (clone\nrepository\nlocally)
(clone\nrepository\nlocally) ..> (commit\nchanges)
(commit\nchanges) ..> (push\nmodified\nrepository)
(push\nmodified\nrepository) ..> (forked\nrepository)
@enduml
```
Per action a `sequence diagram` can be written. Below is the sequence diagram of forking a repository to your user account on github. Changing your code is done on your development setup, A PC or Laptop containing your code and programs that you need for working with your hardware.

Changes you do, you commit locally and upload to your own fork when you have internet access.

```plantuml
@startuml
skinparam backgroundColor transparent
actor you
participant local as "laptop/PC containing\n your local copy"

box "the Internet"
participant fork as "your fork"
participant upstream as "project\nrepository"
end box

activate upstream

you ->(20) upstream : fork
note right : this repo contains\nyour teams' project
upstream ->(5) fork : fork to user account
note left : a clone of the\nupstream in\nyour account
activate fork
fork -->(15) you : done

you ->(10) local : "git clone ... " etc
local ->(10) fork : starts cloning
fork ->(10) local : repository is pulled 
activate local
local -->(10) you : done

you ->(10) local : create branch/commits
activate local
local -->(10) you : done with coding
'deactivate local

you ->(10) local : push branch and/or \ncommits to remote
'activate local
local ->(10) fork : push
activate fork
note over fork : your fork now contains\nall the commits and\nbranches you pushed

@enduml
```