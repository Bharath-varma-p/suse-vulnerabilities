# Fixing World-Writable Directories Without Sticky Bits Set (Vulnerability 105146)

## Introduction
This documentation provides a step-by-step guide to resolve the vulnerability 105146, where world-writable directories are found without their sticky bits set on a SUSE Linux Enterprise Server 15 SP4 host. Setting the sticky bit on world-writable directories is considered a best practice to enhance security.

## Affected System
- IP Address: ***#########***
- Hostname: viparlink-dev.cech.uc.edu
- Operating System: SUSE Linux Enterprise Server 15 SP4

## Vulnerability Details
- Vulnerability ID: 105146
- Description: World-Writable Directories Should Have Their Sticky Bits Set
- Status: Active
- Vulnerability Count: 1
- CVSS Score: 0.0 (AV:N/AC:L/Au:N/C:N/I:N/A:N)
- Temporal Score: 0.0 (E:U/RL:W/RC:UC)

## Affected Directory
`/tmp/SPLUNK_UPDATER_MONITORED_DIR#`

## Resolution Steps
1. Log in to the affected system (viparlink-dev.cech.uc.edu) using an account with sudo or root privileges.

2. Open a terminal and navigate to the affected directory:
   ```bash
   cd /tmp/SPLUNK_UPDATER_MONITORED_DIR#
3. Verify the current permissions and sticky bit status of the directory using the following command:

```bash
        ls -ld /tmp/SPLUNK_UPDATER_MONITORED_DIR#
```


4. To set the sticky bit on the directory, use the following command:
```bash 
    sudo chmod +t /tmp/SPLUNK_UPDATER_MONITORED_DIR#
```

5. Verify that the sticky bit has been successfully set by running the command from step 3 again:

```bash
    ls -ld /tmp/SPLUNK_UPDATER_MONITORED_DIR#    
```


