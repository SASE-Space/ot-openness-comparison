# Openness & DevOps Readiness of OT Systems

## PLC/DCS Systems

<!---sort: score, alphabetical--->

| System                                              |Score| Plain Text Source Files [a]   | Open Download for IDE and Simulator [b]  | Extensible IDE [c]          | Linux Support [d]        | Testing Framework [e] | CLI [f]             | Transparent Licensing [g] | Open Docs [h]    | Hardware Agnostic [i]    |
| ---------------------                               | --- | ----------------              | -----------------                        | --------------------------- |------------------        | --------------------- | ------------------- | ------------------------- | ---------------- | ------------------------ |
|[Codesys V3.5](#codesys)                             | 7   |:x:                            |:heavy_check_mark:                        |:heavy_check_mark: :moneybag:|:x: [2]                   |:heavy_check_mark:     |:heavy_check_mark:   |:heavy_check_mark:         |:heavy_check_mark:|:heavy_check_mark: [4]    |
|[B&R Automation Studio](#br)                         | 6   |:heavy_check_mark:             |:heavy_check_mark:                        |:heavy_check_mark:           |:x:                       |:heavy_check_mark:     |:heavy_check_mark:   |:x:                        |:heavy_check_mark:|:x:                       |
|Codesys Go                                           | 6   |:heavy_check_mark:             |:grey_question:                           |:heavy_check_mark: :moneybag:|:heavy_check_mark:        |:heavy_check_mark:     |:heavy_check_mark:   |:grey_question:            |:grey_question:   |:heavy_check_mark:        |
|[Beckhoff TwinCAT 3](#beckhoff-automation-twincat-3) | 5   |:x: [3]                        |:heavy_check_mark:                        |:heavy_check_mark:           |:grey_question:           |:heavy_check_mark:     |:x:[1]               |:grey_question:            |:heavy_check_mark:|:heavy_check_mark: [4]    |
|Bosch Rexroth CtrlX                                  | 4   |:grey_question:                |:heavy_check_mark:                        |:heavy_check_mark:           |:grey_question:           |:heavy_check_mark:     |:x:                  |:grey_question:            |:heavy_check_mark:|:heavy_check_mark:        |
|Siemens AX                                           | 2   |:heavy_check_mark:             |:x:                                       |:grey_question:              |:grey_question:           |:heavy_check_mark:     |:heavy_check_mark:   |:x:                        |:x:               |:x:                       |
|Siemens TIA                                          | 1   |:x:                            |:grey_question:                           |:heavy_check_mark:           |:grey_question:           |:heavy_check_mark:     |:x:[1]               | :x:                       |:x:               |:x:                       |
|ABB AC500 [5]                                        | 1   |:x:                            | :heavy_check_mark:                       |:grey_question:              |:x:                       |:grey_question:        |:grey_question:      |:x:                        |:grey_question:   |:x:                       |
|Phoenix Contact PLCNext                              | 1   |:x:                            | :grey_question:                          |:grey_question:              |:grey_question:           |:grey_question:        |:grey_question:      |:grey_question:            |:grey_question:   |:heavy_check_mark: [4]    |
|Schneider EAE                                        | 1   |:grey_question:                | :grey_question:                          |:grey_question:              |:grey_question:           |:grey_question:        |:grey_question:      |:grey_question:            |:grey_question:   |:heavy_check_mark: [4]    |
|ABB 800xA                                            | 0   |:x:                            | :x:                                      |:x:                          |:x:                       |:x:                    |:x:                  |:x:                        |:x:               |:x:                       |
|ABB Freelance                                        | 0   |:x:                            | :x:                                      |:x:                          |:x:                       |:x:                    |:x:                  |:x:                        |:x:               |:x:                       |
|B&R Aprol                                            | 0   | :grey_question:               | :x:                                      |:grey_question:              |:grey_question:           |:grey_question:        |:grey_question:      |:grey_question:            |:grey_question:   |:x:                       |
|Emerson DeltaV                                       | 0   |:x:                            | :x:                                      |:x:                          |:x:                       |:x:                    |:x:                  |:x:                        |:x:               |:x:                       |
|Honeywell ControlEdge                                | 0   |:x:                            | :x:                                      |:x:                          |:x:                       |:x:                    |:x:                  |:x:                        |:x:               |:x:                       |
|Honeywell Experion PKS                               | 0   |:x:                            | :x:                                      |:x:                          |:x:                       |:x:                    |:x:                  |:x:                        |:x:               |:x:                       |
|Rockwell Studio 5000                                 | 0   |:x:                            | :x:                                      |:x:                          |:x:                       |:x:                    |:x:[1]               |:x:                        |:x:               |:x:                       |
|Rockwell PlantPAX                                    | 0   |:x:                            | :x:                                      |:x:                          |:x:                       |:x:                    |:x:[1]               |:x:                        |:x:               |:x:                       |
|Schneider Foxboro                                    | 0   |:grey_question:                | :grey_question:                          |:grey_question:              |:grey_question:           |:grey_question:        |:grey_question:      |:grey_question:            |:grey_question:   |:grey_question:           |
|Schneider ProWORX 32                                 | 0   |:grey_question:                | :grey_question:                          |:grey_question:              |:grey_question:           |:grey_question:        |:grey_question:      |:grey_question:            |:grey_question:   |:grey_question:           |
|Siemens PCS7                                         | 0   |:x:                            | :x:                                      |:x:                          |:x:                       |:x:                    |:x:                  |:x:                        |:x:               |:x:                       |
|Siemens PCS7 NEO                                     | 0   |:x:                            | :x:                                      |:x:                          |:x:                       |:x:                    |:x:                  |:x:                        |:x:               |:x:                       |
|Siemens S7                                           | 0   |:x:                            | :x:                                      |:x:                          |:x:                       |:x:                    |:x:                  |:x:                        |:x:               |:x:                       |
|Yokogawa Centum VP                                   | 0   |:x:                            | :x:                                      |:x:                          |:x:                       |:x:                    |:x:                  |:x:                        |:x:               |:x:                       |  

[1] Partially supported, by means of an API (application programming interface). See specific vendor notes below for more information.  
[2] Only runtime on Linux  
[3] TwinCAT stores files in XML format, which technically counts as plain text, but the source code is still cluttered by unnecessary tags and ids. This makes it diffcult to interact with non-proprietary tooling (source code editors, diff tools, ...)  
[4] Will be able to run on Open Process Automation Compute DCN  
[5] IDE based on Codesys

---

# Criteria

## Plain Text Source Files [a]

Most software IDE's store code as plain text files. This allows full access and control over the code by external tools and solutions.

One of the most important of those is proper version version control with for example git. If the automation IDE doesn't store the code as text files then it is not possible to use git. (Except maybe with a complex procedure that first exports the code.) Some automation IDE's store the code in XML format. This is still not ideal because on the one hand it is difficult to read the code. Additionally the IDE might add different id's to the XML tags while the code is essentially the same, rendering the standards diff checks useless.

Also for code generation solutions direct access to plain text files is important. As well for external package/library management.

## Open Download for IDE and Simulator [b]

It is important that engineers have easy access to the IDE as well as runtime simulation environments. Not only for evaluation and training, but also to allow system independent tools to be able to develop and test properly with each system.

## Extensible IDE [c]

The IDE is extensible

## Linux support for runtime and build tools [d]

Linux is extensively used in server environments and is a popular choice for running Continuous Integration and Continuous Deployment pipelines. Build tools that run on Linux can seamlessly integrate into these pipelines, automating the build, test, and deployment processes. Linux applications are also typically 100% configurable through configuration files and/or cli commands, allowing to fully automate the setup and deployment of the application.

## Testing framework [e]

Without testing frameworks all code needs to be tested manually. The available testing frameworks should be able to test the IEC 61131 / IEC 61499 code.

## CLI Tooling [f]

CLI tooling or the IDE allow all compilation, build and deployment workflows to be automated

## Transparent licensing [g]

Prices must be publicly available without login or requesting a quote.
Understanding the licensing of the needed components at a granular and transparent level allows consumers to accurately compare offerings. Transparent licensing also allows to have confidence that the cost can scale alongside with the deployments.

## Open Documentation [h]

Open accessible documentation not locked away behind a login helps to better understand these systems. And recently it also allows LLMs to train on these documents, which is important since LLMs are becoming more important in helping to design and manage DevOps configurations and workflows.

## Hardware Agnostic Runtime [i]

---

# Systems

<!---in alphabetical order--->

## ABB

## B&R

[www.br-automation.com](https://www.br-automation.com/en-us/)

### Plain Text  

* Works well with standard version control and diff tools **without** additional dependencies or addons.

### IDE Download  

* [AS V4.12](https://www.br-automation.com/en-us/downloads/?tx_brcdn_downloadlist%5Baction%5D=download&tx_brcdn_downloadlist%5Bcontroller%5D=Download&tx_brcdn_downloadlist%5Bid%5D=DWL%40DWL10000726943%4000&tx_brcdn_downloadlist%5Blang%5D=%2A&cHash=3f689dfa5485c57f2f984b18aef727a9)
* [Other versions](https://www.br-automation.com/en-us/downloads/#categories=Software-1344987434933/Automation+Studio-1344987435049) can be selected from the dropdown menus

### Extensible IDE  

* B&R releases "upgrades" for new features, new standard hardware, module updates, and for customized hardware
* Can be integrated with digital twins and physics tools
* Because of the plain text files and CLI, it is very easy to use an external IDE alongside Automation Studio
* B&R makes it easy to communicate to any common fieldbus via their "IF" modules paired with a "BC" module or directly from a supported interface on a controller. IF modules and fieldbus devices are configured using the FDT DTM container built into Automation Studio
  * Importing an EDS, IODD, etc can allow for the IDE to directly communicate with and configure fieldbus devices within the project
  * This can also leverage online configuration features such as IO-Link's Parameter Server
  * Runtime configuration of fieldbus devices can be achieved programmatically using an appropriate B&R library
* [B&R extension for VS Code](https://marketplace.visualstudio.com/items?itemName=radeonmann.vscode-brautomationtools) that integrates the AS CLI

### Linux Support  

* As of AS V4.12 Linux is not supported. Unsure if this will change with AS V6 in late 2024
* Automation Runtime is a stand-alone RTOS based on VxWorks

### Testing Framework  

* Unit Test library at B&R Help Explorer GUID: 8df9c77d-965d-405b-8662-2056bb6d5bdc
* The unit tests are written in C / C++
* Code tested in this way can be written in IEC, C or C++, however, because the API is used for testing. The API for a dynamic library is defined using \*.VAR, \*.FUN and \*.TYP files
* Unit tests can also be set up and performed for a binary-encrypted library

### Licensing  

* [AS Trial License Request](https://www.br-automation.com/en-us/service/software-registration/)
  * The only limitaiton posed by the trial license (aside not being for commercial use) is that it does not allow automatic downloading of hardware or feature upgrades from within the IDE. In this case, upgrades can be downloaded from the product's web pages and then installed. The basic installation of AS has most everything you need unless you are doing something more advanced
* There are reasonable fees for more advanced features and packages such as mapp View Premium Widgets, mapp Motion, mapp Services, etc
* Licensing does not obstruct development and will not affect machine operation
* For commercial use, licenses are configured in the controller hardware when it leaves the factory
* Licensing levels are well documented: [mapp View Licensing Example](https://www.br-automation.com/en-us/products/software/mapp-technology/mapp-view/mapp-view-licensing/)

### Open Docs  

* Auatomation Studio locally installs B&R Help Explorer
* [Academy and Free Tutorials](https://www.br-automation.com/en-us/academy/)

### CLI Tools  

* AS Help GUID: b83a0224-5992-413e-a3ec-47edf553fe54
* See VS Code extension above

### Hardware Agnostic  

* Automation Runtime only supports B&R hardware
* ARSim virtualizes Automation Runtime on any Windows PC for development and function with digital twins

### Other B&R Tips  

* Automation Studio fully supports feature-rich HMI development (mapp View) utilizing OPC-UA as a data interface and served as a web application
* Supports C, C++, and use of IEC libraries in C/C++ programs
  * C/C++ Objects can only be used in C/C++ programs
* Only IEC variables can be mapped to the IO. You cannot directly map a C++ object member to the IO - use a pointer to an IEC variable
* In IEC 61131-3, supports typical function block features but does not support methods, interfaces, inheritance, and polymorphism navitely
* B&R PCs support a hypervisor for Windows or Linux alongside Automation Runtime
* Navigate AS Help using GUIDs: From the toolbar select "View" -> "Go To Page" and paste the GUID
* [B&R Community forum](https://community.br-automation.com/)

### DevOps  

* B&R does not directly provide a CI/CD solution.
* At a high level, the ArProject library can be used to install a project from a PIP (Project Installation Package) that can be downloaded to the controller via your preferred protocol/method
  * A PIP can be generated when compiling from the IDE or via CLI
  * ArProject GUID: db67ade7-837e-4b89-ad7f-9d9e2f455d50
  * PIP GUID: 9701601d-9a92-4361-8eaa-8f6c19d90615
* CI/CD is fully supported via 3rd party solutions such as Shuv (not FOSS)
* Loupe Package Manager can be used for integration of Loupe's open source libraries

## Beckhoff Automation TwinCAT 3  

### DevOps Integration Notes  

Beckhoff supports DevOps workflows via the [TwinCAT 3 Automation Interface](https://infosys.beckhoff.com/english.php?content=../content/1033/tc3_automationinterface/242682763.html&id=). The Automation Interface enables programmatic access to most actions that can be performed via the TwinCAT 3 IDE, however it uses the Visual Studio DTE (Development Tools Environment) which requires a full IDE installation and hampers full headless operation or usage within a containerized environment.  

Other notes:

- Depends on COM
- Requires trial license generation for deployment, which cannot be automated (does not apply if the target system is already licensed)
- Can be easily integrated into PowerShell scripts and .NET applications
- Example code is available at https://github.com/Beckhoff/TC_AI_DOTNET_Samples

For automatic deployment and configuration of target platforms, Beckhoff's Windows based platforms support a variety of command line actions for configuration, some of which are demoed at https://github.com/Beckhoff-USA-Community/AutoDeployPCviaScript-main. In TwinCAT 4026, there will also be a chocolatey based package server. For BSD, Beckhoff provides a [package server](https://infosys.beckhoff.com/english.php?content=../content/1033/twincat_bsd/7669840651.html&id=3358471846380427993).

There are third party CI/CD tools available as products for the TwinCAT ecosystem, for example CLI-Tools for configure, make and install and also tools for documentation generation and unit testing or enhancing code quality.
- Zeugwerk Operations [build & test](https://github.com/Zeugwerk/zkbuild-action), [documentation generation](https://github.com/Zeugwerk/zkdoc-action)
- [STweep](https://www.stweep.com/)

### Static Analysis, Unit Testing and Simulation

Beckhoff provides [Static Analysis](https://www.beckhoff.com/en-us/products/automation/twincat/texxxx-twincat-3-engineering/te1200.html) which can perform basic checks for free or more extensive checks of the application for a fee. Static Analysis in TwinCAT 3 is relatively new and user experience may vary. The requirement to have a license on the development system also makes integration into a CI/CD pipeline difficult since it may not be easy or even possible to attach a USB device to a VM and may not be desireable to permanently assign a license to a ephemeral build environment.

Beckhoff does not officially support any Unit Testing methods, however extensive community effort has gone into the free and open source [TcUnit](https://tcunit.org/), developed and maintained by Jakob Sagatowski.

Beckhoff provides a variety of simulation tools, from simple methods including running the PLC locally on the developer's system without hardware to more extensive simulation of EtherCAT devices or via Simulink and other integrations.

### Library package manager

There is [Twinpack](https://github.com/Zeugwerk/Twinpack) available as Open-Source library package manager. It provides an integrated User-Interface in TcXaeShell and also a command line tool to be able to use it easily in CI/CD systems like Jenkins.

### Frameworks

With the above tools it is possible to use Frameworks like in IT-space also for Beckhoff TwinCAT on OT side.
- [Zeugwerk-Framework](https://zeugwerk.dev): Full Application framework with a bunch of libraries and an application template

## B&R Aprol

* This is an animal of its own, part IDE, part industrial DevOps, part SCADA, part remote access.
* Not supported in North America.

## Codesys

### **Disclaimer:**

The following information is based on a specific hardware implementation and does not necessarily reflect the more typical Codesys experience. It illustrates that caution should be used regarding the specific hardware selection.

It is important to verify that hardware to be used with Codesys supports the current version and the feature set you desire. An example is IFM's Ecomat controllers. They **only** support Codesys V3.5 SP11 which does not support the Git add-on (Requires V3.5 SP19 or newer) from the Codesys Pro Developer License. Codesys uses a proprietary project file that does not support version control features without the addon. Further, this specific hardware example requires some poorly documented and unorganized setup to get the IDE to support the hardware, and upgrades to the firmware have to be done with IFM's Maintenance app separate from Codesys.

## Codesys Go

## Omron Sysmac Studio

## Rockwell Studio 5000

In 2023, Rockwell Automation has released the Studio 5000 Logix Designer SDK, or Software Development Kit to automate UI functions of Studio 5000 Logix Designer:  
https://www.rockwellautomation.com/en-us/company/news/blogs/logix-designer-sdk-sme.html  
https://www.kb-controls.io/posts/how-to-automate-your-engineering-processes-with-the-studio-5000-logix-designer-sdk  

This can be integrated with their controller emulation software:  
https://www.rockwellautomation.com/en-us/products/software/factorytalk/designsuite/logix-echo.html

## Rockwell PlantPAX

## Siemens Simatic S7

## Siemens Simatic AX

## Siemens TIA Portal

### DevOps Integration Notes

Siemens TIA Portal supports some DevOps workflows via the [Openness API](https://support.industry.siemens.com/cs/document/109792902/tia-portal-openness-automation-of-engineering-workflows?dti=0&lc=en-WW).

## Siemens PCS7 NEO

## Schneider EAE

## Siemens AX

### Siemens S7

### Siemens TIA

## Bosch Rexroth CtrlX
Bosch Rexroth is a long competitor of all previous mentioned vendors and they launched their new control platform about five years ago. This platform runs on Linux and the RealTime is enabled with Preempt-RT. It is a very powerful platform because of its open strategy on integrating different apps via snap package manager. Everyone can create snaps and integrate those as apps even for modular machine designs but also via an open app-store-like ctrlX-World platform. It is also possible to add Matlab snaps, HMI snaps, Node-Red, Codesys V3.5, CtrlX Plc and many more. Those snaps can interact via a powerful DataLayer which is similar to ADS from the TwinCAT world but more modern and with a RealTime capable fast lane. Bosch Rexroth also offers drives where the ctrlX Core can be directly integrated, which enables a machine manufacturer to build machines with a very small footprint.
Their operating system CtrlX-OS is available for many different platforms.

- [Documentation](https://docs.automation.boschrexroth.com/welcome/) & [HowTos](https://developer.community.boschrexroth.com/t5/Store-and-How-to/bg-p/dcdev_community-dev-blog/label-name/rex_c_How-to)
- [First Steps](https://docs.automation.boschrexroth.com/doc/361295008/first-steps/latest/en/)
- [HowTo Video Collection](https://developer.community.boschrexroth.com/t5/Store-and-How-to/Collection-of-how-to-videos-blogs-and-examples-for-ctrlX/ba-p/12343)
- [Community](https://developer.community.boschrexroth.com/t5/ctrlX-AUTOMATION-Community/ct-p/dcdev_community)
- [Store](https://developer.community.boschrexroth.com/t5/Store-and-How-to/bg-p/dcdev_community-dev-blog/label-name/rex_c_Store)
- [Github](https://github.com/boschrexroth)

## HMI/SCADA Systems

...