## Welcome to the Kubernetes Storm Center 👋

We want to enable (truly) free and open source threat intelligence for the cloud native ecosystem.

Keeping it simple, such that many non-experts can instrument their existing cluster-templates, stream and collect the information of how attackers traverse their "honeycluster", and publish their threat intelligence.

Contributions, ideas and discussions from the cloud-native community are very welcome.

There is a SLACK for the community [https://join.slack.com/t/k8sstorm/shared_invite/zt-2hulzsqh1-mnZL6fGFZiVLrOcqeTObIA](https://join.slack.com/t/k8sstorm/shared_invite/zt-2ma41wrv4-DWQlLAb6nhfZ2afHdE59Ww) 

This is a not-for-profit community project (with absolutely no liability). Unless specifically specified otherwise, Apache License applies.


![Main_Poster](https://github.com/k8sstormcenter/.github/assets/70207455/2257d1d1-22e7-4280-99c5-c8efcf10c744)

The Four Fold Path (to Threat Intelligence):
<img width="1201" alt="FourFoldPathToThreatIntelligence" src="https://github.com/k8sstormcenter/.github/assets/70207455/1bfa4606-d6e5-4ddf-91a0-8993160a64e7">


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
