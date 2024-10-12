>Open Source Software Tool für automatisierte Konfiguration und Orchestrierung

- arbeitet nach einem Client Server Prinzip, wobei der Client in Ruby und der Server in Ruby und Erlang geschrieben ist
- Konfig Anweisungen werden als „Rezepte“ beschrieben und in einem „Kochbuch“ zusammengefasst
- des weiteren enthält ein Kochbuch noch Template und Attribute Files
- um Kochbücher auszuführen werden weitere Tools benötigt
	- Berkshelf - Abhängigkeitsmanager für öffentliche Cookbooks
	- Knife - Verwaltung und Ausführung von Cookbooks
	- 