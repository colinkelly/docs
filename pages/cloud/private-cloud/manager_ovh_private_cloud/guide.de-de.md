---
title: Einführung in das Kundencenter der OVHcloud Private Cloud
slug: manager-ovh-private-cloud
excerpt: Entdecken Sie alle Funktionen Ihres Private Cloud Kundencenters
section: Erste Schritte
order: 1
---

**Stand 31.07.2020**

## Einleitung

Das OVHcloud Kundencenter bietet zahlreiche Optionen für die Konfiguration Ihrer Private Cloud Infrastruktur.

**Diese Anleitung beschreibt die verschiedenen Konfigurationsmöglichkeiten.**

## Voraussetzungen

- Sie sind in Ihrem [OVHcloud Kundencenter](https://www.ovh.com/auth/?action=gotomanager&from=https://www.ovh.de/&ovhSubsidiary=de){.external} eingeloggt und befinden sich unter `Hosted Private Cloud`{.action} im Bereich `Private Cloud`{.action}.
- Sie verfügen über ein [Private Cloud](https://www.ovhcloud.com/de/enterprise/products/hosted-private-cloud/){.external} Produkt.


## Beschreibung

### Tab „Allgemeines“

Im Menüpunkt `Hosted Private Cloud`{.action} im Bereich `Private Cloud`{.action} Ihres [OVHcloud Kundencenters](https://www.ovh.com/auth/?action=gotomanager&from=https://www.ovh.de/&ovhSubsidiary=de){.external} finden Sie eine allgemeine Übersicht Ihrer Private Cloud:

![Allgemeine Informationen](images/controlpanel1.png){.thumbnail}

Im oberen Teil der Seite, `1 auf der Abbildung`, finden sie den Namen und die Beschreibung Ihrer Private Cloud. Diese können Sie gerne anpassen, was besonders nützlich ist, wenn Sie über mehrere Infrastrukturen verfügen. 

Auf der linken Seite, `2 auf der Abbildung`, finden Sie Ihre Private Cloud(s) sowie das bzw. die virtuellen Datacenter, aus denen diese besteht.


#### Allgemeine Informationen

In der linken Tabelle finden Sie die allgemeinen Informationen zu Ihrer Private Cloud.

![Allgemeine Informationen](images/controlpanel2.png){.thumbnail}


- die Beschreibung Ihrer Private Cloud (mit der Möglichkeit, den Namen zu ändern)
- die Version Ihrer Private Cloud
- die zugehörige kommerzielle OVHcloud Referenz
- das Datacenter und genauer, die Zone, in der sich Ihre Infrastruktur befindet
- die Zugangseinstellungen für Ihre Infrastruktur (`Offen` oder `Eingeschränkt`) mit den Einschränkungen nach Quell-IP
- die Anzahl der virtuellen Datacenter in Ihrer Infrastruktur
- die Anzahl der IP-Blöcke (mit der Möglichkeit, weitere Blöcke zu bestellen)


#### Optionen und Compliance

In der mittleren Tabelle wird Ihnen der Aktivierungsstatus der Optionen Ihrer Private Cloud angezeigt.

![Optionen](images/controlpanel3.png){.thumbnail}

#### Dienstverwaltung

In der rechten Tabelle können Sie Ihr Abonnement der OVHcloud Private Cloud Mailingliste verwalten.

Darüber hinaus wird hier auch das nächste Verlängerungsdatum Ihres Private Cloud Dienstes angezeigt. Rechts neben diesem Datum können Sie über den Button `...`{.action} eine Lizenz bestellen oder Ihren Private Cloud Dienst löschen.

![Optionen](images/controlpanel4.png){.thumbnail}

Weitere Informationen zur Kündigung eines Private Cloud Dienstes finden Sie in unserer Anleitung [How to cancel your Private Cloud offer](../eine-private-cloud-kuendigen/).

#### Datacenter

In diesem Tab finden Sie eine kurze Zusammenfassung der virtuellen Datacenter in Ihrer Private Cloud Lösung:

![Datacenter](images/controlpanel5.png){.thumbnail}

Weiter unten in dieser Anleitung finden Sie eine detailliertere Übersicht zu den virtuellen Datacentern.

> [!primary]
>
> Auf dieser Seite können Sie ein weiteres Datacenter hinzufügen. Dies verursacht keine zusätzlichen Kosten.
> 



#### Benutzer

In diesem Bereich werden alle Benutzer angezeigt, die sich auf vSphere einloggen können:

![Benutzer](images/controlpanel6.png){.thumbnail}

Sie können einen Benutzer erstellen, indem Sie links auf den Button `Benutzer erstellen`{.action} klicken.

Zu jedem Benutzer finden Sie verschiedene Benutzerinformationen sowie die für die gesamte Private Cloud geltenden Berechtigungen:

- Kennung
- Vorname (optional)
- Nachname (optional)
- E-Mail-Adresse (optional)
- Telefon-/Faxnummer (optional)
- *token validator*-Berechtigung, erlaubt die Bestätigung kritischer Operationen auf Private Clouds mit HDS- oder PCI-DSS-Option
- *IP*-Berechtigung, erlaubt Zugriff auf das OVH Network Plugin
- *Failover-IP*-Berechtigung, erlaubt die Verwaltung von mit Ihrer Private Cloud verbundenen Failover-IPs
- *NSX-Interface*-Berechtigung, erlaubt Zugriff auf das NSX-Interface, wenn diese Option in Ihrer Private Cloud aktiviert ist
- Status (Diagnose), zeigt an, ob der Benutzer erfolgreich erstellt wurde

Wenn Sie rechts in der Tabelle auf den Button `...`{.action} klicken, werden Ihnen mehrere Optionen angezeigt:

- Einträge dieser Tabelle bearbeiten (die zuvor eingesehenen Berechtigungen ändern, eine E-Mail-Adresse oder Telefonnummer hinzufügen)
- Berechtigungen des Benutzers je Datacenter anzeigen und bearbeiten
- Benutzerpasswort ändern
- Benutzer löschen

Nachfolgend sehen Sie die Berechtigungen je Datacenter im Detail:

![Benutzerrechte je Datacenter](images/controlpanel7.png){.thumbnail}

- `vSphere-Zugriff`{.action} \- hierbei handelt es sich um die globalen Rechte des Benutzers für vSphere:

|Berechtigung|Beschreibung|
|---|---|
|Keine|kein Zugriff|
|Nur Lesen|nur lesender Zugriff|
|Lesen/Schreiben|lesender und schreibender Zugriff|
|Operator|den OVHcloud Administratoren vorbehaltener Zugriff|

- `Zugriff auf VM Network`{.action} \- hierbei handelt es sich um die Rechteverwaltung für den öffentlichen Netzwerkbereich (im vSphere Interface als `VM Network` bezeichnet):

|Berechtigung|Beschreibung|
|---|---|
|Keine|kein Zugriff|
|Nur Lesen|nur lesender Zugriff|
|Operator|erlaubt die Konfiguration virtueller Maschinen (VMs) im öffentlichen Netzwerk|

- `Zugriff auf V(X)LAN`{.action} \- hierbei handelt es sich um die Rechteverwaltung für den privaten Netzwerkbereich, VXLAN für die Dedicated Cloud Reihe bzw. VLAN für die SDDC Reihe:

|Berechtigung|Beschreibung|
|---|---|
|Keine|kein Zugriff|
|Nur Lesen|nur lesender Zugriff|
|Operator|erlaubt die Konfiguration virtueller Maschinen (VMs) im privaten Netzwerk|
|Administrator|erlaubt die Verwaltung von Port-Gruppen des virtuellen Switch (erstellen, bearbeiten, löschen, ...)|

- `Hinzufügen von Ressourcen`{.action} \- dieser Button erlaubt die Vergabe bzw. das Entziehen der Berechtigung, zusätzliche Ressourcen über das OVH Plugin im vSphere Client hinzuzufügen.


#### Sicherheit

In diesem Tab können Sie die Sicherheitseinstellungen für Ihr vCenter einstellen:

![Sicherheitseinstellungen](images/controlpanel8.png){.thumbnail}

Sie können die Elemente im oberen Teil sowie in der Tabelle mit den Buttons rechts daneben konfigurieren. Folgendes kann konfiguriert werden:

- Dauer bis Sitzungstimeout

- Anzahl der erlaubten Simultanverbindungen

- Sicherheitseinstellungen, eingeschränkt oder nicht, mit Berechtigung je Quell-IP. Die IPs werden in der Tabelle angezeigt.
Die IP bzw. der IP-Bereich können geändert oder gelöscht werden, indem Sie auf den Button `...`{.action} rechts neben der Tabelle klicken.

> [!warning]
>
> Wenn Sie die Sicherheitseinstellungen in den Modus „Eingeschränkt“ versetzen und keine IP-Adresse eingeben, kann sich kein Benutzer im vSphere Client einloggen. Die virtuellen Maschinen bleiben jedoch weiterhin verfügbar.
> 


- Die Abmeldungseinstellungen bestimmen, ob der erste oder der letzte verbundene Benutzer ausgeloggt wird.
Wenn im vorliegenden Beispiel 50 Benutzer eingeloggt sind und sich ein 51\. Benutzer anmeldet, so wird der erste, der eine Verbindung hergestellt hat, ausgeloggt.

Es ist eine zweite Tabelle für die Option *VM Encryption* verfügbar.

Weitere Informationen zu dieser Option finden Sie in dieser [Anleitung](../vm-encrypt/).

#### Operationen

In diesem Tab finden Sie die aktuell auf Ihrer Infrastruktur ausgeführten Operationen:

![Operationen](images/controlpanel9.png){.thumbnail}

Sie können hier nachsehen, ob eine Operation fehlgeschlagen ist, Wartungsarbeiten geplant sind, ...

Sie können das Datum für eine Wartungsarbeit ändern, indem Sie rechts in der Tabelle auf den Button `...`{.action} klicken.

> [!primary]
>
> Wenn Sie nicht auf den vSphere Client zugreifen können, wird vielleicht gerade eine Wartungsarbeit durchgeführt. Dies können Sie in diesem Tab überprüfen.
>


#### Windows-Lizenz

Im Tab `Windows-Lizenz`{.action} können Sie Windows-SPLA-Lizenzen auf Ihrer Private Cloud aktivieren, indem Sie rechts daneben auf den Button klicken:

![Windows-SPLA-Lizenz](images/controlpanel10.png){.thumbnail}

Die Preisübersicht hierzu finden Sie [hier](https://www.ovhcloud.com/de/enterprise/products/hosted-private-cloud/images-licenses/){.external}.



### Datacenter-Ansicht

Eine Private Cloud kann mehrere Datacenter enthalten. Wenn Sie auf Ihre Private Cloud klicken, sehen Sie Folgendes:

![Datacenter-Ansicht](images/controlpanel11.png){.thumbnail}

Sie können den Namen Ihres Datacenters ändern oder eine angepasste Beschreibung hinzufügen, indem Sie auf das Stift-Symbol klicken.

Hier finden Sie die Hauptinformationen zu Ihrem Datacenter, seine Reihe sowie die Anzahl der Hosts und Datastores.
Bei Dedicated Cloud und Software Defined Datacenter Produkten können Sie über mehrere Datacenter in derselben Private Cloud Lösung verfügen.


#### Hosts

Hier werden die Hosts Ihres Datacenters angezeigt:

![Hosts](images/controlpanel12.png){.thumbnail}

In diesem Bereich finden Sie:

- die Namen der Hosts
- ihre Profile (M, L, L+, ...)
- den Abrechnungsmodus: Wenn Ihr Host stündlich abgerechnet wird, können Sie auf monatliche Abrechnung umstellen, indem Sie rechts in der Tabelle auf den Button klicken.
- den Host-Status
- die Anzahl der genutzten Stunden (nur bei stündlich abgerechneten Ressourcen)

Oben links über der Tabelle können Sie einen neuen, monatlich abgerechneten Host bestellen.


#### Datastores

Die Datastore-Tabelle gleicht der Tabelle für Hosts:

![Datastores](images/controlpanel13.png){.thumbnail}

In diesem Bereich finden Sie:

- die Namen der Datastores
- ihre Profile
- ihre Typen (Hybrid oder Full SSD)
- ihre Größe
- den Abrechnungsmodus
- den Status des Datastores, der anzeigt, ob dieser korrekt installiert ist
- die Anzahl der genutzten Stunden (nur bei stündlich abgerechneten Ressourcen)

Oben links über der Tabelle können Sie einen neuen, monatlich abgerechneten Datastore bestellen.


#### Backup

Im Backup-Tab können Sie die `Veeam Backup`-Lösung aktivieren.

![Backup](images/controlpanel14.png){.thumbnail}

Weitere Informationen zu dieser Option finden Sie in dieser [Anleitung](https://docs.ovh.com/gb/en/private-cloud/veeam-backup-as-a-service/){.external} (Englisch).


## Weiterführende Informationen

Für den Austausch mit unserer User Community gehen Sie auf <https://community.ovh.com/en/>.
