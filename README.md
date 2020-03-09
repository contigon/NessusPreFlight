# Nessus PreFlight 

**Use at your own risk, this project is in Alpha**
If there are any suggestions or bugs(please submit a pull request and try to fix them, 'cause that's how collaborative coding works!)

## Description
Nessus Preflight(NPF) Check for local and remote systems, Yes it is very hacky code but it works ok :). This script essentially will do local checks on a windows system or on a remote system, sets the reg keys required for nessus to do its magic!

## Quick-Start
Import the module:
`. .\NPF.ps1`

	Carries out a series of checks on the local or a remote system to ensure nessus will work for credentialed patch scans, current setup is for localonly

- `Invoke-NPF -localonly`
	Only check for the registry keys and set them if not already.

- `Invoke-NPF -cleanup`
    Revert the keys back to standard once complete

- `Invoke-NPF -checklocalreg`
    Run just the checks don't change anything, if not set the function will recommend running -localonly
.
- `Invoke-NPF -remote -target '10.1.1.1'`
    Run the script against a remote system, note this will prompt for your credentials, please enter then DOMAIN\Username
    
