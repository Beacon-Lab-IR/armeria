# Velociraptor

Velociraptor is an open-source endpoint monitoring, digital forensics, and incident response (DFIR) tool designed for real-time data collection and analysis. It enables security teams to gather detailed information from endpoints across an organization's network, aiding in the detection, investigation, and remediation of security incidents. Velociraptor stands out for its flexibility, scalability, and extensibility, offering a powerful platform for forensic data collection and analysis in both small and large-scale environments. Its modular design allows users to customize and extend its capabilities according to specific investigative needs, making it a valuable tool in the arsenal of cybersecurity professionals.

This folder contains the client executable and the file configuration needed for the client installation process.

### In Windows
For testing connection (as an administator):

```
velociraptor.exe --config client.config.yaml client -v
```

For installation as a service (as an administator): 

* Old Way, no recommended. 

```
velociraptor.exe --config client.config.yaml service install
```

* New way, using MSI: 
Open CMD.exe. Before download MSI binary, pre packed for our clients

```
msiexec /i velociraptor-windows-repacked.msi
```
### For Linux Debian

* Old way, no recommended.

```
sudo ./velociraptor service install --config client.config.yaml -v
```

* New way, using pre packed binary .deb 

```
sudo dpkg -i velociraptor_client_amd64.deb
```

### For MacOS
```
xattr -d com.apple.quarantine velociraptor
chmod +x velociraptor
sudo ./velociraptor service install --config client.config.yaml -v
```
#### Intel CPU 
```
velociraptor-darwin-amd64
```

#### Apple CPU ARM
```
velociraptor-darwin-arm64
```


## Requeriments 
Allow connection in your security devise to the URL: 
https://velociraptor.beaconlab.us/

Verify if the tool got blocked or URL connection or IP assigned. 


This is a valid service managed by us, which host the Velociraptor server.


For more info about the tool go to: [Velociraptor Docs](https://docs.velociraptor.app/)
