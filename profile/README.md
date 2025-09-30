## Welcome to the Kubernetes Storm Center 👋 Let's take the fear out of threats (by understanding them)

We want to enable (truly) free and open source threat intelligence for the cloud native ecosystem.


Keeping it simple, such that many non-experts can instrument their existing cluster-templates, stream and collect the information of how attackers traverse their "honeycluster", and publish their threat intelligence.
What started with honeyclusters, became a project to instrument kubernetes for live adaptive detection, meaning to construct an algorithm of detection mechanisms to auto-tune the finding of interesting activity on a large and distributed system.


It should be noted, that a large usecase is to "simulate" the attack by using synthetic attacks (attack yourself) to test if a team can a) detect and b) defend and c) incident respond (as required by e.g. NIS-2). This is how the project became more of a SOC, then a honeytrapping system. The stack
can be used for both, and you are solely responsible for taking adequate care - however you choose to instrument your infrastructure. Usage of this software can be destructive or have side-effects.

Contributions, ideas and discussions from the cloud-native community are very welcome. We encourage users to report any issues. Sample livelabs may be found on the iximiuz-labs platform.

There is a SLACK for the community [https://join.slack.com/t/k8sstorm/signup]
Community Office Hrs: Every second Friday at 11am CET at [ZOOM](https://tuwien.zoom.us/j/66245245063?pwd=VVJFY1Azci9aVVZuWWdib0RxZVlBQT09)  

Community Discord Server: https://discord.gg/wTYDWYTS 

This is a not-for-profit community project (with absolutely no liability). Due to reasons, the licence was changed back to the original GPLv2 recently. Please take note

![MVPTreeLogo](https://github.com/user-attachments/assets/78f93955-1f90-4ef0-a050-a652e2adf9fe)
Make the attack trees visible !



## Glossary
| Term | Definition | Example |   
|------|------------|---------|
|  Threat Model    |     Entire superset of threats to your org       |         |   
|  Threat Model -Branch   |   One threat to your org         | Initial Access:    Application Exploit leads to Priv Esc , Abuse of Service Account leads to Lateral Movement, Persistence is established on worker Node    |   
|  Attack Model    |   Concrete implementation of Threat Model Branch Exploit       |    Wordpress Version 1.1.1 CVE 1234 allows RCE , POD SA creates PV/C , C2 software planted in PVC       |   
|  Bait    |  Purpuseful initial access to Threat Model Branch         |    Commit creds to github     |  
|  Events    |    Individual occurences in the IT system        |   Application logs, Network logs, TracingPolicy logs  , Audit logs    |  
|  TracingPolicy    |   eBPF instruction to hook into kernel         |   Kprobe on filedescriptor "write" access in /tmp      |  
|  Stix Observables   |   Relevant events that have occured         |    File '/tmp/wanky' has been written     |  
|  Stix Indicators   |     Attack Model nodes necessary for Attack        |  'access to /etc/shadow'       |  
|  Pattern   |    Match between Observable (event) and Indicator        |    '/usr/bin/mycat /etc/shadow'   <-> access to sensitive file  |  
