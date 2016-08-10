# Frequently Asked Questions

- Runtime Exception: Access is denied.
-

####<a name="accden"></a>I receive a Runtime Exception: Access is denied.
Windows Event Log requires a registered event source to fire events. Log4JNA attempts to create one automatically in 
`HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\services\eventlog\`, but doesn’t have enough registry permissions to do so. 

In order to create registry entries the program using  Log4JNA must be run as Administrator or a the keys must be added manually to the 
registry. See the usage page for Registry configuration instructions.

