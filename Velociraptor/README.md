# Velociraptor

Velociraptor is an open-source endpoint monitoring, digital forensics, and incident response (DFIR) tool designed for real-time data collection and analysis. It enables security teams to gather detailed information from endpoints across an organization's network, aiding in the detection, investigation, and remediation of security incidents. Velociraptor stands out for its flexibility, scalability, and extensibility, offering a powerful platform for forensic data collection and analysis in both small and large-scale environments. Its modular design allows users to customize and extend its capabilities according to specific investigative needs, making it a valuable tool in the arsenal of cybersecurity professionals.

This folder contains the client executable and the file configuration needed for the client installation process.

For testing connection 

```
velociraptor.exe --config client.config.yaml client -v
```

For installation as a service: 

```
velociraptor.exe --config client.config.yaml service install
```

Allow connection in your security devise to the URL: 
https://velociraptor.rbnetto.dev/


This is a valid service managed by us, which hosts the Velociraptor server.


For more info about the tool go to: [Velociraptor Docs](https://docs.velociraptor.app/)