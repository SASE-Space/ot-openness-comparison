# Openness & DevOps Readiness of OT Systems

## PLC/DCS Systems

draft version (table not correct) - for initial feedback  
sort: score, alphabetical

| system                | plain text [a]   | open download [b] | extensible IDE [c]          | Linux [d]     | testing framework [e] | cli [f]          | transparent licensing [g] | open docs [h]    | HW independent [i] | score |
| --------------------- | ---------------- | ----------------- | --------------------------- |-------------- | --------------------- | ---------------- | ------------------------- | ---------------- | ------------------ | ----- |
| B&R Automation Studio |:heavy_check_mark:|:heavy_check_mark: |:grey_question:              |:grey_question:|:grey_question:        |:grey_question:   |:grey_question:            |:heavy_check_mark:|:grey_question:     | 3     |
| Beckhoff TwinCAT 3    |:x:               |:heavy_check_mark: |:grey_question:              |:grey_question:|:heavy_check_mark:     |:grey_question:   |:grey_question:            |:heavy_check_mark:|:grey_question:     | 3     |
| Siemens AX            |:heavy_check_mark:|:x:                |:grey_question:              |:grey_question:|:heavy_check_mark:     |:heavy_check_mark:|:grey_question:            |:x:               |:x:                 | 3     |
| Codesys               |:grey_question:   |:heavy_check_mark: |:heavy_check_mark: :moneybag:|:grey_question:|:grey_question:        |:grey_question:   |:grey_question:            |:grey_question:   |:heavy_check_mark:  | 2     |
| Codesys Go            |:heavy_check_mark:|:grey_question:    |:grey_question:              |:grey_question:|:grey_question:        |:grey_question:   |:grey_question:            |:grey_question:   |:heavy_check_mark:  | 2     |
| Siemens TIA           |:x:               |:grey_question:    |:heavy_check_mark:           |:grey_question:|:heavy_check_mark:     |:x:               | :x:                       |:x:               |:x:                 | 2     |
| Schneider EAE         |:grey_question:   | :grey_question:   |:grey_question:              |:grey_question:|:grey_question:        |:grey_question:   |:grey_question:            |:grey_question:   |:heavy_check_mark:  | 1     |
| B&R Aprol             | :grey_question:  | :x:               |:grey_question:              |:grey_question:|:grey_question:        |:grey_question:   |:grey_question:            |:grey_question:   |:x:                 | 0     |
| Siemens PCS7          |:x:               | :x:               |:x:                          |:x:            |:x:                    |:x:               |:x:                        |:x:               |:x:                 | 0     |
| Siemens PCS7 NEO      |:x:               | :x:               |:x:                          |:x:            |:x:                    |:grey_question:   |:x:                        |:x:               |:x:                 | 0     |
| Siemens S7            |:x:               | :x:               |:x:                          |:x:            |:x:                    |:x:               |:x:                        |:x:               |:x:                 | 0     |
| ...                   |                  |                   |                             |               |                       |                  |                           |                  |                    | 0     |



## HMI/SCADA Systems

...

## Explanation


### store code files as plain text [a]

Most software IDE's store code as plain text files. This allows full access and control over the code by external tools and solutions.

One of the most important of those is proper version version control with for example git. If the automation IDE doesn't store the code as text files then it is not possible to use git. (Except maybe with a complex procedure that first exports the code.) Some automation IDE's store the code in XML format. This is still not ideal because on the one hand it is difficult to read the code. Additionally the IDE might add different id's to the XML tags while the code is essentially the same, rendering the standards diff checks useless.

Also for code generation solutions direct access to plain text files is important. As well for external package/library management.

### open download of IDE and simulation runtime [b]

It is important that engineers have easy access to the IDE as well as runtime simulation environments. Not only for evaluation and training, but also to allow system independent tools to be able to develop and test properly with each system.

### extensible IDE [c]

The IDE is extensible

### linux support for runtime and build tools [d]

Linux is extensively used in server environments and is a popular choice for running Continuous Integration and Continuous Deployment pipelines. Build tools that run on Linux can seamlessly integrate into these pipelines, automating the build, test, and deployment processes. Linux applications are also typically 100% configurable through configuration files and/or cli commands, allowing to fully automate the setup and deployment of the application.

### testing framework [e]

Without testing frameworks all code needs to be tested manually. The available testing frameworks should be able to test the IEC 61131 / IEC 61499 code.

### cli tooling [f]

CLI tooling allows all workflows to be automated

### transparent licensing [g]

Understanding the licensing of the needed components at a granular and transparent level allows consumers to accurately compare offerings. Transparant licencing also allows to have confidence that the cost can scale alongside with the deployments.

### open documentation [h]

Open accessible documentation not locked away behind a login helps to better understand these systems. And recently it also allows LLMs to train on these documents, which is important since LLMs are becoming more important in helping to design and manage DevOps configurations and workflows.

### HW independent runtimes [i]

...


## System Details

in alphabetical order

### Codesys
...

### Codesys Go

### Schneider EAE

### Siemens AX

### Siemens PCS7 NEO

### Siemens S7

### Siemens TIA













