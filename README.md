# Kofax RPA for Total Agility

Kofax is an **AI-drive, **data-intensive workflow** technology and cloud solution company** and it is Kofax RPA that empowers KTA to be data-intensive. 
Kofax Total Agility is excellent at handling documents and data that is inside internal business systems and databases, but RPA is excellent at getting access to data inside Excel Documents, PDFs, web, cloud applications, desktop applications and green screen systems.  
See [this video and presentation](https://kofax.app.bigtincan.com/lshare/w7GmZ6QAnXbepkDLzdJYEmMTPFwsLEN2j3l4a5oR10VOxvqP9y).
## Managing RPA from KTA
Total Agility is an **orchestration platform** for dealing with complex workflows and case management.  
It is recommend that all Kofax RPA robots be driven from Total Agility, otherwise you have hybrid orchestration, which is not ideal for managing both systems.
Total Agility can then control 
* Robot starting
* retrieving robot results
* handling exceptions in robots and retrying robots and suspending KTA processes.

## Running Robots from KTA
KTA can run robots both synchronously (wait until robot finishes) or asynchronously (do not wait for robot to finish).  
### Synchronous Robots
* KTA handles robots synchronously out-of-the-box.
* robots should be fast and be finished in less than 30 seconds.
### Asynchronous Robots
This is for robots that run "independently" of KTA or robots that take too long to run, that KTA cannot or should not wait for results.
* Kofax RPA supports [robot queuing](https://github.com/KofaxRPA/RPA-11.1/blob/main/RobotQueueing.md#robot-queueing-in-kofax-rpa) via REST. This mechanism returns a token, with which KTA can monitor the process of the robotand retrieve the results of a robot when it has finished.

## Controlling KTA from within RPA
RPA can [control KTA](https://docshield.kofax.com/RPA/en_US/11.3.0_5cdzhlgb3t/help/rpa_help/help_main/designstudio/c_das_ktastep.html) from within the robot, but this is not generally recommended from either Kofax nor from Partners who implement hybrid solutions, due to the superiority of KTA as an orchestration platform.  
![image](https://user-images.githubusercontent.com/47416964/191754515-703bdbb8-c414-4a4e-82c6-e9b768863a36.png)

