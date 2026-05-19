# Integritetspolicy — Copl

**Version 1.0 — gäller från 2026-05-19**

Den här policyn berättar vad Copl gör med den data du och din partner lägger in i appen. Vi har försökt skriva den i klartext — om något är otydligt, hör av dig.

---

## Vem är ansvarig

Pontus Brunzell, privatperson, är **personuppgiftsansvarig** för Copl.

Kontakt: copl-app@outlook.com

> *Notering under utveckling: när appen flyttar till bolag uppdateras detta avsnitt med bolagets namn, organisationsnummer och kontaktuppgifter.*

---

## Sammanfattning för dig som har bråttom

- **Du och din partner är de enda som ser ert innehåll.** Inte vi.
- **Inga reklam-SDK:er, inga analytics, inga trackers.** Inget.
- **All data lagras i Sverige.** Region: Stockholm (Supabase).
- **Du kan när som helst** se all data om dig, exportera den, eller radera ditt konto.
- **Känslig data** (intimitet, familj-anteckningar) kommer krypteras end-to-end — då kan inte ens vi som driftar se innehållet.

---

## 1. Vad samlas in

### 1.1 När du skapar ett konto

| Uppgift | Vad det är | Varför vi behöver det |
|---|---|---|
| **E-postadress** | Din mejl | Inloggning via magic link. Vi skickar bara en länk dit. |
| **Smeknamn** | Vad din partner ser | För att appen ska kunna säga "Eva har lagt till en uppgift" istället för ett ID-nummer |
| **Anonymt konto-ID** | Slumpat UUID | Internt — kopplar dig till dina data |

Vi frågar **aldrig** om:
- Riktigt för- eller efternamn
- Telefonnummer
- Adress
- Födelsedatum eller ålder
- Kön
- Profilbild med foto (frivillig avatar är möjlig men inte krav)

### 1.2 När du använder appen

Det innehåll du och din partner skriver in:
- Uppgifter, att-göra-listor, inköpslistor
- Kalenderhändelser
- Familjeinformation (namn på barn, skostorlek, läkare, allergier)
- Måltidsplanering
- Träningsloggar
- Veckorutiner
- Läxor
- Budget (inkomster, utgifter)
- Överenskommelser mellan er
- Uppskattningar ni skickar varandra
- Dagliga och veckovisa humör-checkins
- Intimitet-data (loggar, preferenser, mål) — endast om ni aktivt slår på modulen
- Påminnelser ni skickar varandra
- Korta meddelanden

Vi *ber inte* om något av detta — ni väljer själva vad ni lägger in.

### 1.3 Tekniska data

- **Push-token** för enheten (för att kunna skicka notiser till just den enheten)
- **Enhetstyp och appversion** (iOS/Android, för felsökning)
- **Tidstämplar** på dina handlingar (när du loggade in, när en rad skapades)

### 1.4 Vad vi **inte** samlar in

- Plats (GPS, IP-baserad geolocation)
- Kontakter / adressbok från din telefon
- Beteendetracking eller analytics
- Reklamidentifierare (IDFA, GAID)
- Cookies (appen använder inga)
- Banktransaktioner eller kortuppgifter
- Hälsodata utöver det du själv loggar in i intimitet-modulen

---

## 2. Varför vi behandlar data — rättslig grund

Per ändamål:

| Ändamål | Rättslig grund (GDPR) |
|---|---|
| Skapa konto, logga in | **Avtal** (Art. 6.1.b) — du ingår avtal med oss för att använda appen |
| Spara dina uppgifter och visa dem för din partner | **Avtal** |
| Skicka push-notiser om uppgifter och händelser | **Berättigat intresse** (Art. 6.1.f) — appen vore meningslös utan notiser; minimal påverkan på dig |
| Lagra intimitet-data | **Uttryckligt samtycke** (Art. 9.2.a) — du aktiverar modulen aktivt och kan stänga av när som helst |
| Felrapportering (när Sentry är aktivt) | **Berättigat intresse** — tekniska crash-rapporter utan personuppgifter |

Intimitet-data är en **särskild kategori av personuppgifter** enligt GDPR Art. 9. Vi hanterar det med extra försiktighet: opt-in, möjlighet att låsa med PIN, framtida end-to-end-kryptering.

---

## 3. Var data lagras

| Var | Vad | Geografi |
|---|---|---|
| **Supabase** | All databas-innehåll, autentisering, filer | **Sverige (Stockholm)** — EU-region, data lämnar aldrig EU |
| **Apple Push Notification Service (APNS)** | Push-token + notisinnehåll i transit | Apples globala infrastruktur |
| **Google Firebase Cloud Messaging (FCM)** | Push-token + notisinnehåll i transit | Googles globala infrastruktur |
| **Expo** | App-byggen, OTA-uppdateringar (ingen användardata) | USA |
| **Sentry** (när aktiv) | Crash-rapporter | EU-region (konfigurerat) |

Inga andra tredjeparter har tillgång till data.

---

## 4. Hur länge sparas data

- **Aktiva konton:** Ingen automatisk radering. Data lever så länge du använder appen.
- **Avslutade relationer** (där båda partners avslutat eller du raderat ditt konto): Soft-delete först. **Hård radering inom 30 dagar.**
- **Avslutade konton:** All din data raderas inom 30 dagar.
- **Backuper:** Vi tar manuella backuper med begränsad retention. Backuper äldre än 3 månader raderas.
- **Server-loggar:** Maximalt 7 dagar.

---

## 5. Vem ser data

### Du och din partner
Ni ser varandras innehåll inom er relation. Det är hela poängen med appen.

### Vi (driftansvariga)
- Tekniskt kan vi nå databasen via Supabase-administrationsverktyg.
- I praktiken tittar vi inte i användardata — det finns inga rutin-uppgifter som kräver det.
- Vid felsökning av specifikt fel kan vi behöva läsa enstaka rader, alltid med syftet att åtgärda problemet och inget annat.
- När **end-to-end-kryptering är på plats** kommer vi *inte ens kunna* läsa intimitet-data, familj-anteckningar eller överenskommelser — det är krypterat på din enhet innan det sparas.

### Tredjeparter
- **Supabase** lagrar datan men har inga rutiner som öppnar den. De har sin egen integritetspolicy.
- **Apple och Google** ser push-innehåll på vägen till din telefon. Vi skickar generiska notistexter ("Något nytt från din partner") där det är möjligt.
- **Inga andra.**

### Vad vi *inte* gör
- Vi **säljer aldrig** data.
- Vi **delar aldrig** data med reklamnätverk eller datamäklare.
- Vi **kombinerar inte** din data med externa datakällor.

---

## 6. Säkerhet

- **Row Level Security (RLS)** på alla databastabeller — det är tekniskt omöjligt för en användare att läsa data från en relation hen inte är medlem i.
- **HTTPS** krypterar all trafik mellan din telefon och våra servrar.
- **End-to-end-kryptering** kommer implementeras för känsliga fält (intimitet, familj-anteckningar, överenskommelser, uppskattningar) inför publik lansering. Då kommer inte ens vi som driftar att kunna läsa innehållet.
- **PIN-lås** på intimitet-modulen kan aktiveras lokalt på din enhet.
- **Diskret läge** döljer känsliga sektioner från appens startsida.
- **Lösenord existerar inte** — vi använder magic link via mejl, vilket eliminerar lösenords-läckage-risker.

---

## 7. Dina rättigheter enligt GDPR

Du har följande rättigheter och kan utöva dem när som helst:

| Rättighet | Så här gör du |
|---|---|
| **Få veta** vilken data vi har om dig | Inställningar → "Din data" — visar allt som lagras om dig personligen |
| **Få rättat** felaktig data | Du kan ändra allt eget innehåll direkt i appen |
| **Få raderat** dina data ("rätten att bli glömd") | Inställningar → Radera kontot — all data försvinner inom 30 dagar |
| **Få ut** dina data (dataportabilitet) | Inställningar → Exportera vår data (kommer i nästa version) — JSON-fil med alla rader |
| **Begränsa** behandlingen | Pausa relationen (Inställningar → Pausa) — då blir data read-only |
| **Invända** mot behandling | Kontakta oss (se nedan) |
| **Återkalla samtycke** för intimitet-modulen | Inställningar → stäng av Närhet/Intimitet — datan raderas |

Vi svarar på alla förfrågningar **inom 30 dagar**, normalt mycket snabbare.

---

## 8. Klagomål

Om du tycker att vi hanterar dina personuppgifter felaktigt kan du:

1. **Höra av dig till oss först** — vi vill veta och gärna fixa.
2. **Lämna in klagomål till Integritetsskyddsmyndigheten (IMY):**
   - Webb: https://www.imy.se
   - Telefon: 08-657 61 00
   - Post: IMY, Box 8114, 104 20 Stockholm

---

## 9. Automatiserade beslut och profilering

Vi använder **inga** automatiserade beslut eller profilering. Inga algoritmer drar slutsatser om dig som påverkar dig.

---

## 10. Barn

Copl är inte avsedd för barn under 16 år. Föräldrar kan lagra information *om* sina barn (namn, skostorlek, allergier) som del av familj-modulen — men barnen själva ska inte skapa konton.

Föräldrarna ansvarar för att informera barnen om vilken data som lagras om dem.

---

## 11. Ändringar i denna policy

Den här policyn kan komma att uppdateras när appen utvecklas eller när lagstiftning ändras. Större ändringar meddelas i appen och vid behov via mejl.

**Versionshistorik:**

| Version | Datum | Ändring |
|---|---|---|
| 1.0 | 2026-05-19 | Första publicerade versionen. |

---

## 12. Kontakt

För integritetsfrågor, GDPR-förfrågningar eller bara nyfikenhet:

**E-post:** copl-app@outlook.com

**Postadress:** lämnas på begäran

---

*Denna policy är skriven på svenska. Vid avvikelse från översättning gäller den svenska versionen.*

*Källdokument med tekniska detaljer (för utvecklare): [`docs/INTEGRITET.md`](docs/INTEGRITET.md) i kodbasen.*
