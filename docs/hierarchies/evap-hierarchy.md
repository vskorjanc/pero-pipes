# Evaporation database
The database can be reached by typing `\\npet1\evap_database` into file explorer.  

!!! warning
    Thot GUI **will not** be able to directly set `\\npet1\evap_database\data` as the root folder.

!!! tip
    Running `net use z: \\npet1\evap_database` in Command Prompt will render shared folder as the `z:` drive on your computer. This will make it more easily accessible, and will allow you to set `z:\data` as the Thot root.

## Hierarchy
An overview of container relations. Showing container `type`.  

``` mermaid
flowchart TD
root --> batch_group --> batch;
batch --> EQE & evap_logs & UV-VIS & JV & MPP & PL;
UV-VIS --> transmission & reflection
click root "../../containers/root"
click batch_group "../../containers/batch_group"
click batch "../../containers/batch"
click EQE "../../containers/EQE"
click evap_logs "../../containers/evap_logs"
click UV-VIS "../../containers/UV-VIS"
click JV "../../containers/JV"
click MPP "../../containers/MPP"
click PL "../../containers/PL"
click transmission "../../containers/transmission"
click reflection "../../containers/reflection"
```

- [[root]]
	- [[batch_group]]
		- [[batch]]
			- [[EQE]]
			- [[evap_logs]]
			- [[JV]]
			- [[MPP]]
			- [[PL]]
			- [[UV-VIS]]
				- [[transmission]]
				- [[reflection]]
			- EDX
			- SEM
			- TRPL
			- XRD
