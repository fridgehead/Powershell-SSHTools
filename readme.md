SSH-Tools.ps1
--


Some ssh tools for powershell using the ssh.net libraries. 

Current functionality:
* Reverse port forwarding
* Includes ssh.net dll in the script, doesnt write to disk when executed and only requires this ps1 file. Can be used with Empire without breaking opsec

Usage
--

> import-module SSH-Tools.ps1
> Start-ReversePortForward -sshhost ssh.myhost.com -username USER1 -password PASS -RemotePort 23000 -Desthost someinternalserver.local -destport 80

when youre done

> Stop-reverseportforward

Currently only one port forward at a time is possible, it uses the PS jobs system so I see no reason more couldnt be started, I just havent got round to it yet :)
