# Kroll Artifact Parser and Extractor (KAPE) 
Kape is a versatile and comprehensive digital forensic and incident response tool developed by Eric Zimmerman. It is designed to aid forensic investigators, incident responders, and cybersecurity professionals in efficiently collecting and analyzing digital evidence from various sources. Kape provides a wide range of modules and plugins that can be customized to gather data from different sources like Windows systems, web browsers, chat applications, and more.

Key features of Kape include the ability to automate data collection processes, support for a variety of artifacts and data sources, customizable configurations, and compatibility with popular forensic tools like Autopsy and Magnet AXIOM. Kape simplifies the forensic investigation process by streamlining data collection and analysis, making it a valuable tool for professionals in the digital forensics and incident response fields.

## Getting Started

![image](https://github.com/user-attachments/assets/349e2f2e-b390-4af8-8773-926dfad97d45)
![image](https://github.com/user-attachments/assets/d2d9c4e0-af86-4e61-ae9f-20fde546eed2)


## More advance commands: 

* For targets
```cmd.exe
.\kape.exe --tsource C: --tdest C:\IR-Tools\logs-kape  --target WindowsDefender,AnyDesk,FileZillaClient,FileZillaServer,OpenSSHClient,OpenSSHServer,RemoteUtilities_app,WinSCP,Chrome,!BasicCollection,!SANS_Triage,Antivirus,FileSystem,FTPClients,KapeTriage,RecycleBin,TorrentClients,USBDetective,WSL,ApacheAccessLog,NGINXLogs,DC++,Torrents,$LogFile,ApplicationEvents,EventLogs,EventLogs-RDP,EventTraceLogs,EventTranscriptDB,LogFiles,MemoryFiles,RDPCache,RDPLogs,RecentFileCache,RecycleBin_DataFiles,RecycleBin_InfoFiles,StartupFolders,StartupInfo,USBDevicesLogs,WER,WindowsFirewall --zip target --vss
```

* For targets and modules
```cmd.exe
.\kape.exe --msource C:\ --mdest C:\IR-Tools\logs-kape\module%d%m --zm true --module DumpIt_Memory,BMC-Tools_RDPBitmapCacheParser,Bulk_extractor,Chainsaw,log4j-scanner,Loki_LiveResponse,Loki_Scan,PowerShell_Netscan,reg_hunter_binary,reg_hunter_email,reg_hunter_encoding,reg_hunter_ip,reg_hunter_link,reg_hunter_obfuscation,reg_hunter_script,reg_hunter_shell,reg_hunter_url,WMI-Parser,LogParser_ApacheAccessLogs,LogParser_DetailedNetworkShareAccess,LogParser_LogonLogoffEvents,LogParser_RDPUsageEvents,LogParser_SMBServerAnonymousLogons,NirSoft_BrowsingHistoryView,NirSoft_FullEventLogView_AllEventLogs,NirSoft_FullEventLogView_Application,NirSoft_FullEventLogView_ScheduledTasks,NirSoft_FullEventLogView_Security,SysInternals_Autoruns,Thor_Scan,Thor_Upgrade,!!ToolSync,!EZParser,bstrings,LiveResponse_NetSystemInfo,LiveResponse_NetworkDetails,LiveResponse_ProcessDetails,LogParser,bstrings_Email,EvtxECmd,EvtxECmd_RDP,RBCmd,RecentFileCacheParser,WxTCmd,KapeResearch_EventLogs_XML,Sync_RECmd,Sync_SQLECmd,PowerShell_Defender_Exclusions,PowerShell_Process_Cmdline,PowerShell_ProcessList_CimInstance,PowerShell_ProcessList_WMI,Windows_ARPCache,Windows_DNSCache,Windows_GpResult,Windows_IPConfig,Windows_ManageBDE_BitLockerKeys,Windows_ManageBDE_BitLockerStatus,Windows_MsInfo,Windows_nbtstat_NetBIOSCache,Windows_nbtstat_NetBIOSSessions,Windows_Net_Accounts,Windows_Net_File,Windows_Net_LocalGroup,Windows_Net_Session,Windows_Net_Share,Windows_Net_Start,Windows_Net_Use,Windows_Net_User,Windows_netsh_portproxy,Windows_NetStat,Windows_qwinsta_RDPSessions,Windows_schtasks
```

