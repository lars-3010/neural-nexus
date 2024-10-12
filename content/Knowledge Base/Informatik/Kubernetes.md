>Software, von [[Google]] entwickelt
>beinhaltet Orchestrator zur automatischen Bereitstellung, Skalierung und Verwaltung von Containern

### Komponenten
>zur Verwaltung der Container
- kube-apiserver - REST API zur Verwaltung von Containern
- etcd - Hochverfügbarer Key-Value Speicher für alle Clusterdaten
- kube-scheduler - Überwacht & Koordiniert alle Deployments

- mehrere Container können als Cluster (Pods) gestartet & verwaltet werden
- Zuweisung mehrerer Pods: Service definier
	- besitzt feste IP-Adresse 
	- realisiert Loadbalancing[[]]