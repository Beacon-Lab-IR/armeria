# Hayabusa
Hayabusa is a Windows event log fast forensics timeline generator and threat hunting tool

![image](https://github.com/user-attachments/assets/f1240e27-618a-481b-a4d7-b0362f539684)


## Getting Started 
1. Go  haybusa folder, with a `cmd.exe` with admin permissions
1. Update rules in haybusa```hayabusa-2.16.0-win-x64.exe update-rules```
![Screenshot 2024-07-30 at 11 22 30](https://github.com/user-attachments/assets/f2a752b0-df74-4e55-a6f2-61d5f58df1ce)
1. You must first export all the EVTX logs and put under `.\logs` folder.  and execute the following command
``` hayabusa.exe computer-metrics -d .\logs -o computer-metrics.csv```

![image](https://github.com/user-attachments/assets/bb71b4a8-5c7c-4f86-8719-1259699dea45)

1. You should see something like this:

![image](https://github.com/user-attachments/assets/884f8307-51c7-420f-b468-d30e12a16b20)



## Notes

*The zip file is detected and deleted by the Windows Defender Security*


### Official Links: 
* https://github.com/Yamato-Security/hayabusa
