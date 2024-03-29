# Openness & DevOps Readiness of OT Systems

## PLC/DCS Systems

draft version (table not correct) - for initial feedback  
sort: score, alphabetical

| System                | Plain Text [a]   | Open Download [b] | Extensible IDE [c]          | Linux [d]        | Testing Framework [e] | CLI [f]             | Transparent Licensing [g] | Open Docs [h]    | Hardware Independent [i] | Score |
| --------------------- | ---------------- | ----------------- | --------------------------- |------------------| --------------------- | ------------------- | ------------------------- | ---------------- | ------------------------ | ----- |
| Codesys V3.5          |:x:               |:heavy_check_mark: |:heavy_check_mark: :moneybag:|:x: [2]           |:heavy_check_mark:     |:heavy_check_mark:   |:heavy_check_mark:         |:heavy_check_mark:|:heavy_check_mark:        | 7     |
| Codesys Go            |:heavy_check_mark:|:grey_question:    |:heavy_check_mark: :moneybag:|:heavy_check_mark:|:heavy_check_mark:     |:heavy_check_mark:   |:grey_question:            |:grey_question:   |:heavy_check_mark:        | 6     |
| Beckhoff TwinCAT 3    |:x: [3]           |:heavy_check_mark: |:heavy_check_mark:           |:grey_question:   |:heavy_check_mark:     |:x:[1]               |:grey_question:            |:heavy_check_mark:|:heavy_check_mark:        | 5     |
| Bosch Rexroth CtrlX   |:grey_question:   |:heavy_check_mark: |:heavy_check_mark:           |:grey_question:   |:heavy_check_mark:     |:x:                  |:grey_question:            |:heavy_check_mark:|:heavy_check_mark:        | 5     |
| B&R Automation Studio |:heavy_check_mark:|:heavy_check_mark: |:grey_question:              |:grey_question:   |:heavy_check_mark:     |:grey_question:      |:grey_question:            |:heavy_check_mark:|:grey_question:           | 4     |
| Siemens AX            |:heavy_check_mark:|:x:                |:grey_question:              |:grey_question:   |:heavy_check_mark:     |:heavy_check_mark:   |:x:                        |:x:               |:x:                       | 3     |
| Siemens TIA           |:x:               |:grey_question:    |:heavy_check_mark:           |:grey_question:   |:heavy_check_mark:     |:x:[1]               | :x:                       |:x:               |:x:                       | 2     |
| Schneider EAE         |:grey_question:   | :grey_question:   |:grey_question:              |:grey_question:   |:grey_question:        |:grey_question:      |:grey_question:            |:grey_question:   |:heavy_check_mark:        | 1     |
| B&R Aprol             | :grey_question:  | :x:               |:grey_question:              |:grey_question:   |:grey_question:        |:grey_question:      |:grey_question:            |:grey_question:   |:x:                       | 0     |
| Siemens PCS7          |:x:               | :x:               |:x:                          |:x:               |:x:                    |:x:                  |:x:                        |:x:               |:x:                       | 0     |
| Siemens PCS7 NEO      |:x:               | :x:               |:x:                          |:x:               |:x:                    |:grey_question:      |:x:                        |:x:               |:x:                       | 0     |
| Siemens S7            |:x:               | :x:               |:x:                          |:x:               |:x:                    |:x:                  |:x:                        |:x:               |:x:                       | 0     |
| ...                   |                  |                   |                             |                  |                       |                     |                           |                  |                          | 0     |

[1] Partially supported, by means of an API (application programming interface). See specific vendor notes below for more information.
[2] Only runtime on Linux
[3] TwinCAT stores files in XML format, which technically counts as plain text, but the source code is still cluttered by unnecessary tags and ids. This makes it diffcult to interact with non-proprietary tooling (source code editors, diff tools, ...) 

## HMI/SCADA Systems

...

## Explanation


### Store code files as plain text [a]

Most software IDE's store code as plain text files. This allows full access and control over the code by external tools and solutions.

One of the most important of those is proper version version control with for example git. If the automation IDE doesn't store the code as text files then it is not possible to use git. (Except maybe with a complex procedure that first exports the code.) Some automation IDE's store the code in XML format. This is still not ideal because on the one hand it is difficult to read the code. Additionally the IDE might add different id's to the XML tags while the code is essentially the same, rendering the standards diff checks useless.

Also for code generation solutions direct access to plain text files is important. As well for external package/library management.

### Open download of IDE and simulation runtime [b]

It is important that engineers have easy access to the IDE as well as runtime simulation environments. Not only for evaluation and training, but also to allow system independent tools to be able to develop and test properly with each system.

### Extensible IDE [c]

The IDE is extensible

### Linux support for runtime and build tools [d]

Linux is extensively used in server environments and is a popular choice for running Continuous Integration and Continuous Deployment pipelines. Build tools that run on Linux can seamlessly integrate into these pipelines, automating the build, test, and deployment processes. Linux applications are also typically 100% configurable through configuration files and/or cli commands, allowing to fully automate the setup and deployment of the application.

### Testing framework [e]

Without testing frameworks all code needs to be tested manually. The available testing frameworks should be able to test the IEC 61131 / IEC 61499 code.

### CLI Tooling [f]

CLI tooling or the IDE allow all compilation, build and deployment workflows to be automated

### Transparent licensing [g]

Understanding the licensing of the needed components at a granular and transparent level allows consumers to accurately compare offerings. Transparent licensing also allows to have confidence that the cost can scale alongside with the deployments.

### Open Documentation [h]

Open accessible documentation not locked away behind a login helps to better understand these systems. And recently it also allows LLMs to train on these documents, which is important since LLMs are becoming more important in helping to design and manage DevOps configurations and workflows.

### Hardware Independent Runtimes [i]

...


## System Details

in alphabetical order

### ABB B&R
...

### Beckhoff Automation TwinCAT 3

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
...

### Codesys Go
...

### Omron Sysmac Studio
...

### Siemens Simatic S7
...

### Siemens Simatic AX
...

### Siemens TIA Portal

#### DevOps Integration Notes

Siemens TIA Portal supports some DevOps workflows via the [Openness API](https://support.industry.siemens.com/cs/document/109792902/tia-portal-openness-automation-of-engineering-workflows?dti=0&lc=en-WW).

### Siemens PCS7 NEO
...

### Schneider EAE
...

### Siemens AX
...

### Siemens PCS7 NEO
...

### Siemens S7
...

### Siemens TIA
...

### Bosch Rexroth CtrlX
Bosch Rexroth is a long competitor of all previous mentioned vendors and they launched their new control platform about five years ago. This platform runs on Linux and the RealTime is enabled with Preempt-RT. It is a very powerful platform because of its open strategy on integrating different apps via snap package manager. Everyone can create snaps and integrate those as apps even for modular machine designs but also via an open app-store-like ctrlX-World platform. It is also possible to add Matlab snaps, HMI snaps, Node-Red, Codesys V3.5, CtrlX Plc and many more. Those snaps can interact via a powerful DataLayer which is similar to ADS from the TwinCAT world but more modern and with a RealTime capable fast lane. Bosch Rexroth also offers drives where the ctrlX Core can be directly integrated, which enables a machine manufacturer to build machines with a very small footprint.
Their operating system CtrlX-OS is available for many different platforms. 
- [Documentation](https://docs.automation.boschrexroth.com/welcome/) & [HowTos](https://developer.community.boschrexroth.com/t5/Store-and-How-to/bg-p/dcdev_community-dev-blog/label-name/rex_c_How-to)
- [Store](https://developer.community.boschrexroth.com/t5/Store-and-How-to/bg-p/dcdev_community-dev-blog/label-name/rex_c_Store)
- [Github](https://github.com/boschrexroth)
more will be added soon...











