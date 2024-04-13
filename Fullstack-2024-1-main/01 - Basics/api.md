# API Übung

GitHub stellt eine sehr umfangreiche API bereit, welche auf der folgenden Seite dokumentiert ist: https://docs.github.com/en/rest   
Um Zugriff als Benutzer zu erhalten, muss zunächst ein sogennanter **Personal Access Token** generiert werden. Mit diesem kann der API Aufruf (Basic Auth) sich authentifizieren.

In dieser Aufgabe sollen eure Profil Informationen angepasst werden.

Nutze zur Lösung der Aufgabe den [Postman Client](https://www.postman.com/product/rest-client/).

## Aufgaben

1. Erzeuge einen Personal Access Token.   
https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token   
**Beachte den erforderlichen Scope!**

2. Lass dir dein eigenes Profil über die GitHub API anzeigen.   
API URL: `https://api.github.com/user`   
**Zur Abfrage muss der API-Request mit Authentifizierung erfolgen (Basic Auth).**
![Postman](images//postman.png)

3. Passe deine Biografie (Bio) an.   
https://docs.github.com/en/rest/reference/users#update-the-authenticated-user   
Die neue Profilinformation wird im **Body** des Requests im JSON-Format übermittelt.   
*Postman: JSON Daten können über Body -> raw hinterlegt werden.*   
Sofern die Änderung erfolgreich war, sollte die Rückmeldung dein neues Profil beinhalten.
    ```json
    {
        "bio" : "Meine neue Bio"
    }
    ```

4. Überprüfe die Änderung über die GitHub Webseite.
