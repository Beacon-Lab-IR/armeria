# yamatoSecurityConfigureWinEventLogs.bat

This batch script helps you quickly configure Windows Event Logs for enhanced security monitoring, following best practices from the Yamato Security project.

## 📦 Original Repository

This script is maintained as part of the [Yamato Security Windows Event Log Configuration](https://github.com/Yamato-Security/WindowsEventLogConfig) project.  
For updates, issues, and contributions, visit the [GitHub repository](https://github.com/Yamato-Security/WindowsEventLogConfig).

## 🚀 Usage

1. **Download the Script**  
   Download `yamatoSecurityConfigureWinEventLogs.bat` from the [releases page](https://github.com/Yamato-Security/WindowsEventLogConfig/releases) or clone the repository:
   ```sh
   git clone https://github.com/Yamato-Security/WindowsEventLogConfig.git
   ```
2. Run as Administrator
* Right-click the batch file and select Run as administrator
* Or, open a Command Prompt with administrative privileges and execute:
```sh
cd path\to\script
yamatoSecurityConfigureWinEventLogs.bat
```

3. Follow On-Screen Prompts
The script will apply recommended security settings to your Windows Event Logs.
You may be prompted to confirm actions or restart your system for changes to take effect.

## 📝 Manual & Details
### What does this script do?
Configures key Windows Event Logs (Security, System, Application, etc.) to increase log retention, enable recommended auditing, and set log sizes according to security best practices.

### Supported Systems:
Windows 10, Windows 11, Windows Server 2016/2019/2022.

### Customization:
* Edit the batch file to adjust log sizes or retention policies as needed.
* See the Yamato Security documentation for advanced options.
Reverting Changes:
* To revert, restore your system from a backup or manually reset Event Log settings.

## 📚 References
* [Yamato Security Windows Event Log Config GitHub](https://github.com/Yamato-Security/EnableWindowsLogSettings)
* [Microsoft Docs: Event Logs](https://learn.microsoft.com/en-us/windows/win32/eventlog/event-logging)

## 🛠️ Troubleshooting
* Permission Denied:
Ensure you are running the script as an administrator.
* Script Fails or Errors:
Check the Issues page for known problems or to report a new one.
