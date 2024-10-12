


https://www.ionos.de/digitalguide/server/sicherheit/was-ist-dns-hijacking/

### **Router Hijack**

- Login-Daten werden nach Installation meist nicht geändert → einfaches Eindringen
- greifen DNS-Server an, tragen ihren eigenen Server ein → Konvertierung von Webadresse zu IP-Adresse
    - jeder Websiteaufruf kann auf krimenelle Seite umgeleitet werden

### **Local Hijack**

Bei dieser Angriffsform ist direkt der Computer des Nutzers betroffen. Über einen Trojaner bekommen Angreifer Zugriff auf die DNS-Einstellungen des Geräts. Windows ermöglicht beispielsweise, den bevorzugten DNS-Server direkt einzutragen. Das machen sich die Angreifer zunutze und geben einfach den eigenen DNS-Server an. Theoretisch können Nutzer das auch sehen – doch wer überprüft regelmäßig die DNS-Einstellungen seines Betriebssystems? Auch bei dieser Technik sendet der Computer also die **Anfragen direkt an den schädlichen Server**. Jeder Websiteaufruf kann so umgeleitet werden.

### **Rouge Hijack**

Während die anderen beiden Angriffsarten im Einflussbereich des Nutzers liegen, sind dessen Geräte beim Rouge Hijack nicht direkt betroffen. Stattdessen wird direkt ein bestehender Nameserver– zum Beispiel beim Internetanbieter – angegriffen und übernommen. Die Geräte der Nutzer greifen also auf einen eigentlich korrekten DNS-Server zu, dieser steht aber nicht mehr – oder zumindest teilweise nicht mehr – unter der Kontrolle des eigentlichen Anbieters. Die Angreifer **ändern meist ausgewählte Einträge**.

Zwar ist eine solche Attacke sehr schwierig durchzuführen, da die meisten Anbieter von Nameservern sehr hohe Sicherheitsstandards haben, doch hat ein Angreifer erstmal Erfolg, kann er über Rouge Hijack eine **enorme Menge an Nutzern erreichen**. Jeder Client, der über diesen DNS-Server die Namensauflösung durchführt, kann das Opfer von DNS Hijacking werden.

### **Man-in-the-Middle-Attacke**

Bei einer [Man-in-the-Middle-Attacke](https://www.ionos.de/digitalguide/server/sicherheit/man-in-the-middle-attack-angriffsmuster-im-ueberblick/) fängt ein Angreifer – der sprichwörtliche Mann in der Mitte – Datenpakete während der Kommunikation zwischen Client und Server ab. Da die DNS-Anfragen vielfach **nicht verschlüsselt** sind, kann der Angreifer einfach mitlesen. Statt der gewünschten Website erhält der Nutzer dann die IP-Adresse zu einer schädlichen Seite im Web. Der eigentliche DNS-Server wird die Anfrage vermutlich niemals erhalten.

# **Gefahren durch DNS Hijacking**

Beim DNS Hijacking werden Nutzer also auf ungewünschte Webseiten weitergeleitet – aber was kann das konkret für Schäden verursachen? Möglich ist es beispielsweise, dass Nutzer auf Websites geleitet werden, auf denen sich ihr verwendetes System **mit schädlicher Software infiziert**. Tatsächlich findet diese Form des Angriffs aber in der Praxis gar nicht oder zumindest kaum statt. Viel häufiger sind hingegen die beiden Techniken [Phishing](https://www.ionos.de/digitalguide/e-mail/e-mail-sicherheit/phishing-mails-erkennen-so-schuetzen-sie-ihre-daten/) und Pharming.

Beim **Phishing** landet der Nutzer auf der Nachbildung einer eigentlich seriösen Website, die aber nur eine Attrappe ist und sensible Daten des Nutzers ermitteln soll. Der Nutzer denkt in einem solchen Fall beispielsweise, dass er sich auf der Homepage seiner Bank befindet, und gibt wie gewohnt seine Anmelde-Informationen inklusive Passwort ein. Der Angreifer kann die Informationen dann speichern und verwenden, um das Onlinebanking-Konto des Nutzers zu kapern.

Phishing funktioniert auch ohne DNS Hijacking, indem Nutzer beispielsweise auf manipulierte Links klicken. Doch durch die Korruption des Domain Name Systems wird die Technik noch perfider: Der Nutzer kann hierbei alles richtiggemacht haben, die korrekte URL in die Adresszeile des Browsers eingetragen haben oder vielleicht sogar auf ein Lesezeichen geklickt haben, und wird dennoch auf die falsche Website geführt. Aufgrund des großen **Vertrauens in das DNS** überprüfen die meisten Nutzer nicht, ob sie sich tatsächlich auf der gewünschten Website befinden oder auf einer Fälschung surfen.

**Pharming** auf der anderen Seite ist meist weniger schädlich für den jeweiligen Nutzer, kann dem Angreifer aber ebenfalls sehr nützlich sein. Bei dieser Methode werden Nutzer auf eine Website geleitet, die komplett mit Werbeanzeigen überfüllt ist. Bei jedem Aufruf dieser Seite, die ansonsten keinerlei Zweck erfüllt, erhält der Betreiber Geld – selbst dann, wenn die Seite sofort wieder geschlossen wird. Der so erzeugte Umsatz fließt dann häufig wieder in andere kriminelle Aktivitäten.

Immer öfter wird DNS Hijacking aber auch von offizieller Seite eingesetzt. Manche Regierungen zensieren das Internet damit. Teilweise, um politische Positionen zu unterdrücken, teilweise aber auch, um beispielsweise Pornografie zu unterbinden. Nutzer, die versuchen, eine betroffene Website aufzurufen, werden auf eine andere Website weitergeleitet. Anders als beispielsweise beim Phishing wird der Nutzer bei dieser **Form der Zensur** aber meist deutlich auf den Vorgang hingewiesen.

Auch **Internetanbieter** selbst setzen teilweise auf DNS Hijacking: Versucht ein Nutzer, eine Webadresse aufzurufen, die nicht im DNS registriert ist, wird eigentlich eine Fehlermeldung (NXDOMAIN) ausgegeben und es wird keine Website geladen. Häufig passiert dies, wenn man sich beispielsweise bei der Eingabe der URL vertippt hat. Bevor eine Fehlermeldung ausgegeben wird, durchläuft die Anfrage jede Ebene des Domain Name Systems. Erst wenn von der obersten Stufe zurückgemeldet wird, dass tatsächlich unter dieser Adresse kein Eintrag vorhanden ist, bekommt der Browser die Rückmeldung.

Genau in diesem Moment findet das **DNS Hijacking durch den Netzanbieter** statt: Die Fehlermeldung wird abgefangen und stattdessen wird die IP-Adresse zu einer anderen Website ausgegeben. Internetanbieter gehen diesen Schritt, um dann entweder ebenfalls auf Websites mit reichlich Werbung umzuleiten und so direkten Umsatz zu erzeugen, oder aber um auf ihre eigenen Angebote hinzuweisen. Dabei entsteht zwar kein Schaden für den Nutzer, doch die Ausspielung von Werbung kann trotzdem störend wirken.

# **Wie kann man sich gegen DNS Hijacking schützen?**

So vielfältig wie die Angriffsmuster beim DNS Hijacking sind auch die Schutzmöglichkeiten. Als erstes sollte man die **Anmeldeinformationen seines Routers ändern**. Natürlich ist es sinnvoll, ein sehr sicheres Passwort zu wählen, aber am wichtigsten ist tatsächlich, dass man es nicht bei den Standardwerten belässt. Die wenigsten Internetbetrüger werden sich die Mühe machen und versuchen, das Passwort zu knacken. Zusätzlich sollte man die Firmware des Geräts auf dem neuesten Stand bringen. Hersteller veröffentlich relativ regelmäßig Updates, die Sicherheitslücken schließen.

Um den eigenen PC zu sichern, sollte man sich vor Trojanern schützen. Das geht auf der einen Seite durch Anti-Viren-Software, auf der anderen Seite aber auch durch einen **umsichtigen Umgang mit Dateien im Internet**. Niemals sollte man Dateien von einer unbekannten oder fragwürdigen Quelle herunterladen.

Zusätzlichen Schutz bietet eine [VPN-Verbindung](https://www.ionos.de/digitalguide/server/knowhow/was-ist-ein-vpn-virtual-private-network/). Hierbei stellt der Nutzer nicht eine direkte Verbindung zu der gewünschten Website her, sondern lässt die Kommunikation über den Server eines [VPN-Services](https://www.ionos.de/digitalguide/server/tools/vpn-services/) laufen. Diese Verbindungen werden zudem in der Regel komplett verschlüsselt durchgeführt. Man-in-the-Middle-Attacken sind damit praktisch ausgeschlossen.

Generell schützen sich Nutzer vor allem – auch gegen anderen Gefahren im Internet – durch eine gewisse **Skepsis und jede Menge Vorsicht**. Man sollte gerade bei Websites, die sehr sensible Nutzerdaten verarbeiten (Online-Banking, Webshops, etc.), lieber einmal zu viel auf die Echtheit des Inhalts achten. Hinweise bieten beispielsweise [SSL-Zertifikate](https://www.ionos.de/digitalguide/websites/webseiten-erstellen/ssl-zertifikat/), die man sich einfach im Browser anzeigen lassen kann.

Inzwischen werden **sicherere Wege der Namensauflösung** entwickelt. Mit [DNS over HTTPS](https://www.ionos.de/digitalguide/server/knowhow/dns-over-https/) und [DNS over TLS](https://www.ionos.de/digitalguide/server/sicherheit/dns-over-tls/) will man die Übertragung verschlüsseln, somit gegen Man-in-the-Middle-Attacken schützen und generell die Privatsphäre von Nutzern erhöhen. Bisher haben sich diese Technik noch nicht als Standard für alle Systeme durchgesetzt.