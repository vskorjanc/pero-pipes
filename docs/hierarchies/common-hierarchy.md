# Common data hierarchy
An overview of container relations. Showing container `type`.  

``` mermaid
flowchart TD
root --> batch_group --> batch;
batch --> EQE & evap_logs & UV-VIS & JV & MPP & PL;
UV-VIS --> transmission & reflection
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