# Common data hierarchy
An overview of container relations. Showing container `type`.  

``` mermaid
flowchart TD
root --> batch_group --> batch;
batch --> EQE & UV-VIS & JV & MPP & PL;
UV-VIS --> transmission & reflection
click root "../../containers/root"
click batch_group "../../containers/batch_group"
click batch "../../containers/batch"
click EQE "../../containers/EQE"
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