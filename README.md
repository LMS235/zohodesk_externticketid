# Custom Function für externe Ticketnummern

Eine Custom Function um externe Ticketnummern auslesen zu können und in den Betreff und ein Feld zu schreiben.

## Vorbereitung

### Felder
Damit das sauber funktioniert brauchen wir 2 Felder unter den Kontakten (um entsprechende Suchmuster hinterlegen zu können).

Hier im Beispiel heißen diese:
  * cf_ext_ticket_pre (das ist der API Name des Feldes)
  * cf_ext_ticket_post (das ist der API Name des Feldes)
  
Weiterhin natürlich ein Feld im Ticket selbst für die ExterneID.

Hier im Beispiel eben:
  * cf_external_id (das ist der API Name des Feldes)
  
### OAuth Verbindung

1. Click on Setup > Developer Space > Connections 
2. Click on Create Connection
3. Choose Zoho OAuth
4. Name Connection and connection link as `extticketid`
5. In Scope Choose all value `Desk.tickets.READ`
6. Click on Create and Connect
7. Click on Connect
8. Click on Accept and proceed

### Mapping im Code

  * ticketID => Ticket Id
  * ticketsub => Subject
  * ticketcontact => Contact Id


# Einbau als Workflow

Das ganze sollte man dann als Workflow entsprechend einbauen. Hier kann man z.B. auch sagen "nur wenn Feld ExternalID leer" um unnötiges ausführen zu verhindern.

Code wird "as is" zu Verfügung gestellt. Keinerlei Haftung oder Support.

