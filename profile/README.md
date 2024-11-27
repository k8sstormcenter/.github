## Welcome to the Kubernetes Storm Center 👋 Let's take the fear out of threats (by understanding them)

We want to enable (truly) free and open source threat intelligence for the cloud native ecosystem.


Keeping it simple, such that many non-experts can instrument their existing cluster-templates, stream and collect the information of how attackers traverse their "honeycluster", and publish their threat intelligence.

These "honeyclusters" can be used to pro-actively test also perceived or modelled threats on a continuous improvement mindset.

It should be noted, that a large usecase is to "simulate" the attack by using synthetic attacks (attack yourself) to test if a team can a) detect and b) defend and c) incident respond (as required by e.g. NIS-2).

Contributions, ideas and discussions from the cloud-native community are very welcome. We encourage users to report any issues.

There is a SLACK for the community [https://join.slack.com/t/k8sstorm/signup]

This is a not-for-profit community project (with absolutely no liability). Unless specifically specified otherwise, Apache License applies.

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
