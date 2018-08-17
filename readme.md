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

 or to start a tunnel + socks5 proxy on port 23000

> start-socksproxy -sshhost ssh.myhost.com -username USER -password PASS -RemotePort 23000 -LocalPort 10000


when youre done

> Stop-PortForwardJobs

