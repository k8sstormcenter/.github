## Welcome to the Kubernetes Storm Center: Sovereign Detection/Response 


What started with honeyclusters, became a project to instrument kubernetes for live adaptive detection, meaning to archtect (eBPF) detection mechanisms to reconstruct paths of interesting activity on a large, distributed system and being able to respond to a given verdict.



It should be noted, that a large usecase is to "simulate" the attack by using synthetic attacks (attack yourself) to test if a team can a) detect and b) defend and c) incident respond (as required by e.g. NIS-2). You will find the majority of the functionality in:
- bob : how to tune your runtime-behavior config 
- kubescape node-agent : Detection and Signatures
- pixie: Sovereign Multi-cluster dataplane for protocol-reconstruction and forensic capture
- clickhouse: database for forensic storage

<img width="1103" height="580" alt="Screenshot 2026-09-23 at 12 15 49" src="https://github.com/user-attachments/assets/60be0199-04e4-4a07-997e-1fa7d3e163dc" />



Sample livelabs may be found on the iximiuz-labs platform.

There is a SLACK for the community [https://join.slack.com/t/k8sstorm/signup]


This is a not-for-profit community project (with absolutely no liability). 

![MVPTreeLogo](https://github.com/user-attachments/assets/78f93955-1f90-4ef0-a050-a652e2adf9fe)
Make the attack trees visible !



