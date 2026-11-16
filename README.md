# Firmabok Backup – Google OAuth-sidor

Den här mappen innehåller två statiska webbsidor som beskriver en **privat rclone-anslutning** för säkerhetskopiering av en självhostad Firmabok-installation till Google Drive.

## GitHub-beskrivning (Description)

> Privat rclone-integration för krypterade säkerhetskopior av Firmabok till Google Drive.

**Om kryptering inte har aktiverats ännu:** Beskrivningen beskriver det tilltänkta målet. Du kan i stället använda: `Privat rclone-integration för säkerhetskopior av Firmabok till Google Drive.`

## Lägg upp med GitHub Pages

1. Skapa ett **Public**-repository på GitHub med namnet `firmabok-backup` (eller använd ett befintligt).
2. Lägg upp `index.html` och `privacy.html` i repositoryts **rotmapp**. Du kan också lägga upp denna `README.md`.
3. Öppna **Settings → Pages → Build and deployment** och välj **Deploy from a branch** med `main` och `/(root)`, sedan **Save**.
4. Kontrollera att båda sidorna faktiskt visas offentligt utan inloggning:
   - Startsida: `https://DITT-GITHUB-NAMN.github.io/firmabok-backup/`
   - Integritetspolicy: `https://DITT-GITHUB-NAMN.github.io/firmabok-backup/privacy.html`
5. I **Google Cloud → Google Auth Platform → Branding** fyller du i de **verkliga, fungerande länkarna** som ovan, samt korrekt supportadress och appnamnet `Firmabok Backup`.
6. I **Authorized domains** anger du den domän som Google godtar för din Pages-adress, normalt `DITT-GITHUB-NAMN.github.io` om tillgängligt. Google kan kräva ägarverifiering. Om ett delat Pages-domännamn inte godtas behöver du använda en domän som du själv kontrollerar.
7. Gå till **Audience** och kontrollera om **Publish app** kan väljas. Att sidan finns garanterar inte att Google godkänner alla OAuth-behörigheter utan ytterligare verifiering.

## Viktigt

- **Lägg aldrig** `rclone.conf`, `.env`, Client Secret, token, lösenord eller säkerhetskopior i det publika GitHub-repositoriet.
- Webbplatsen skapar inte backup själv; den är endast information för Google OAuth. Ställ in och testa rclone crypt och backup separat.
- Policyn beskriver den tänkta privata användningen. Ändra texten om den inte motsvarar hur du faktiskt hanterar data.
- Ingen särskild e-postadress eller GitHub-användarnamn har skrivits in i filerna.

## Referens

Rclones instruktioner för eget Google Client ID: https://rclone.org/drive/#making-your-own-client-id

Googles krav på OAuth-sidor: https://developers.google.com/identity/protocols/oauth2/production-readiness/brand-verification
