# OpennessOfOTSystems

# Openness & DevOps Readiness of OT Systems

## PLC/DCS Systems

draft version (table not correct) - for initial feedback  
sort: score, alphabetical

| system                | plain text [1] | open download [2] | Linux [3] | testing framework [4] | cli [5] | transparent licensing [6] | open docs [7] | HW independent [8] | score |
| --------------------- | -------------- | ----------------- | --------- | --------------------- | ------- | ------------------------- | ------------- | ------------------ | ----- |
| Siemens AX            | YES            |                   |           | YES                   | YES     |                           |               |                    | 3     |
| Beckhoff TwinCAT 3    |                | YES               |           | YES                   |         |                           |               |                    | 2     |
| Codesys Go            | YES            |                   |           |                       |         |                           |               | YES                | 2     |
| Siemens TIA           |                | ?                 |           | YES                   |         |                           |               |                    | 1     |
| Codesys               | ?              |                   |           |                       |         |                           |               | YES                | 1     |
| Schneider EAE         | ?              |                   |           |                       |         |                           |               | YES                | 1     |
| Siemens S7            |                |                   |           |                       |         |                           |               |                    | 0     |
| Siemens PCS7          |                |                   |           |                       |         |                           |               |                    | 0     |
| Siemens PCS7 NEO      |                |                   |           |                       |         |                           |               |                    | 0     |
| B&R Automation Studio |                |                   |           |                       |         |                           |               |                    | 0     |
| B&R Aprol             |                |                   |           |                       |         |                           |               |                    | 0     |
| ...                   |                |                   |           |                       |         |                           |               |                    | 0     |



## HMI/SCADA Systems

...

## Explanation


### store code files as plain text [1]

Most software IDE's store code as plain text files. This allows full access and control over the code by external tools and solutions.

One of the most important of those is proper version version control with for example git. If the automation IDE doesn't store the code as text files then it is not possible to use git. (Except maybe with a complex procedure that first exports the code.) Some automation IDE's store the code in XML format. This is still not ideal because on the one hand it is difficult to read the code. Additionally the IDE might add different id's to the XML tags while the code is essentially the same, rendering the standards diff checks useless.

Also for code generation solutions direct access to plain text files is important. As well for external package/library management.

### open download of IDE and simulation runtime [2]

It is important that engineers have easy access to the IDE as well as runtime simulation environments. Not only for evaluation and training, but also to allow system independent tools to be able to develop and test properly with each system.

### linux support for runtime and build tools [3]

Linux is extensively used in server environments and is a popular choice for running Continuous Integration and Continuous Deployment pipelines. Build tools that run on Linux can seamlessly integrate into these pipelines, automating the build, test, and deployment processes. Linux applications are also typically 100% configurable through configuration files and/or cli commands, allowing to fully automate the setup and deployment of the application.

### testing framework [4]

Without testing frameworks all code needs to be tested manually

### cli tooling [5]

CLI tooling allows all workflows to be automated

### transparent licensing [6]

Understanding the licensing of the needed components at a granular and transparent level allows consumers to accurately compare offerings. Transparant licencing also allows to have confidence that the cost can scale alongside with the deployments.

### open documentation [7]

Open accessible documentation not locked away behind a login helps to better understand these systems. And recently it also allows LLMs to train on these documents, which is important since LLMs are becoming more important in helping to design and manage DevOps configurations and workflows.

### HW independent runtimes [8]

...


## System Details

in alphabetical order

### ABB B&R

### Beckhoff Automation

#### DevOps Integration Notes

Beckhoff supports DevOps workflows via the [TwinCAT 3 Automation Interface](https://infosys.beckhoff.com/english.php?content=../content/1033/tc3_automationinterface/242682763.html&id=). The Automation Interface enables programmatic access to most actions that can be performed via the TwinCAT 3 IDE, however it uses the Visual Studio DTE (Development Tools Environment) which requires a full IDE installation and hampers full headless operation or usage within a containerized environment. 

Other notes:
- Depends on COM
- Requires trial license generation for deployment, which cannot be automated (does not apply if the target system is already licensed)
- Can be easily integrated into PowerShell scripts and .NET applications
- Example code is available at https://github.com/Beckhoff/TC_AI_DOTNET_Samples

For automatic deployment and configuration of target platforms, Beckhoff's Windows based platforms support a variety of command line actions for configuration, some of which are demoed at https://github.com/Beckhoff-USA-Community/AutoDeployPCviaScript-main. In TwinCAT 4026, there will also be a chocolatey based package server. For BSD, Beckhoff provides a [package server](https://infosys.beckhoff.com/english.php?content=../content/1033/twincat_bsd/7669840651.html&id=3358471846380427993).

#### Static Analysis, Unit Testing and Simulation

Beckhoff provides [Static Analysis](https://www.beckhoff.com/en-us/products/automation/twincat/texxxx-twincat-3-engineering/te1200.html) which can perform basic checks for free or more extensive checks of the application for a fee. Static Analysis in TwinCAT 3 is relatively new and user experience may vary. The requirement to have a license on the development system also makes integration into a CI/CD pipeline difficult since it may not be easy or even possible to attach a USB device to a VM and may not be desireable to permanently assign a license to a ephemeral build environment.

Beckhoff does not officially support any Unit Testing methods, however extensive community effort has gone into the free and open source [TcUnit](https://tcunit.org/), developed and maintained by Jakob Sagatowski.

Beckhoff provides a variety of simulation tools, from simple methods including running the PLC locally on the developer's system without hardware to more extensive simulation of EtherCAT devices or via Simulink and other integrations.


### Codesys

### Codesys

### Codesys Go

### Omron Sysmac Studio

### Siemens Simatic S7

### Siemens Simatic AX

### Siemens TIA

### Siemens PCS7 NEO

### Schneider EAE





