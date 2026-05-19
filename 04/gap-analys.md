# Gap-analys: NordicShop AB mot ISO 27001:2022 Annex A

## Instruktioner

1. Läs organisationsbeskrivningen för NordicShop AB (`case.md`).
2. Gå igenom de 15 kontrollerna nedan en i taget.
3. Sätt **status** och **mognadsnivå** för varje:
   - **Status:** U = Uppfyllt | D = Delvis | E = Ej uppfyllt | N/A = Ej tillämplig
   - **Mognad (0–5):** 0 = Obefintlig | 1 = Ad hoc | 2 = Definierad | 3 = Etablerad | 4 = Mätt | 5 = Optimerad
4. Skriv en kort motivering (1–2 meningar) baserad på caset.
5. Välj ut era **fem viktigaste gap** och fyll i handlingsplanen.
6. Välj ut ett **"värsta gap"**.

## Kontrollista (urval från ISO 27001:2022 Annex A)

| # | Kontroll | Krav (kort) | Status | Mognad | Motivering |
|---|----------|-------------|:------:|:------:|------------|
| **5.1** | Policies for information security | Informationssäkerhetspolicy beslutad av ledning, publicerad och kommunicerad |Ej tillämplig |Ad Hoc |Finns ingen informationssäkerhetspolicy. Finns en "IT-policy" från 2019 som ingen läser. |
| **5.2** | Information security roles and responsibilities | Definierade roller och ansvar för informationssäkerhet |Ej uppfyllt |Obefintlig |Finns ingen dedikerad säkerhetsroll. Markus "har hand om säkerheten när han har tid" |
| **5.9** | Inventory of information and other associated assets | Uppdaterad tillgångsförteckning med ägare |Ej uppfyllt |Ad Hoc |Finns en lista från 2022 som underhålls i mån av tid/påminnelse |
| **5.12** | Classification of information | Klassificeringsschema finns och används |Ej tillämplig |Obefintlig |Finns ingen klassificeringsschema |
| **5.19** | Information security in supplier relationships | Leverantörsriskbedömningar och avtalskrav |Ej uppfyllt |Ad Hoc |Finns inga riskbedömning men avtal finns dock ej kontrollerade |
| **5.24** | Incident management planning and preparation | Dokumenterad incidenthanteringsprocess med roller |Ej tillämplig |Obefintlig |Finns inga formella incidenthanteringsplaner utan man ringer Markus om något händer. |
| **5.30** | ICT readiness for business continuity | Kontinuitetsplan för IT, testad |Ej uppfyllt |Obefintlig |Finns ingen kontinuitetsplan eller katastrofplan, tester för backup har aldrig gjorts. |
| **6.3** | Information security awareness, education and training | Återkommande utbildning för all personal |Ej uppfyllt |Obefintlig |Inga utbildningar utfördes förutom en webbbaserad kurs från 2022 om GDPR där 60% slutförde den |
| **8.2** | Privileged access rights | Kontroll och uppföljning av priviligierad åtkomst |Ej tillämplig |Ad Hoc | Inga rutiner för när någon slutar(offboarding), adminåtkomster delas mellan flera, inga rutiner för åtkomstgenomgångar. |
| **8.5** | Secure authentication | MFA och stark autentisering för åtkomst till känsliga system |delvis |Ad Hoc |MFA är aktiverad men om man klagar för mycket så tas MFA bort |
| **8.8** | Management of technical vulnerabilities | Sårbarhetshantering, skanning och patchning |Ej uppfyllt |Ad Hoc |Patchning, skanning och sårbarhetshantering sker när det passar. Rutiner måste införas. |
| **8.13** | Information backup | Backup tas, skyddas och **återställning testas regelbundet** |Delvis |Ad Hoc |AWS och fortnox backas upp dagligen men backuper testas aldrig. rutiner måste införas |
| **8.15** | Logging | Loggar samlas in, skyddas och granskas |Ej tillämplig |Obefintlig |Inga uppgifter om loggar samlas in, skyddas eller granskas. |
| **8.16** | Monitoring activities | Övervakning av system för att upptäcka onormala beteenden |Ej uppfyllt |Ad Hoc |Standardkonfig för brandväggen i AWS som gjordes 2020 samt endast Microsoft Defender. |
| **6.5** | Responsibilities after termination or change of employment | Offboarding — återkallande av åtkomst och tillgångar vid avslut |Ej uppfyllt |Ad Hoc |Inga fasta rutiner för offboarding. Ibland glöms det bara bort |

## Handlingsplan: de fem viktigaste gapen

| # | Gap (kort) | Åtgärd | Ansvarig | Deadline | Kostnad (L/M/H) | Prioritet (1–5) |
|---|-----------|--------|----------|----------|:---------------:|:---------------:|
| 1 |Offboarding missar konton |Rutiner/Checklistor |HR |1 vecka |L |4 |
| 2 |Backuper testas aldrig |Rutiner för backuptester.Testerna skall utföras varannan månad med dokumentation och signering |IT/VD |1 månad |H |1 |
| 3 |Ingen uppdaterad inventorylista |Kontrolleras var 3e månad med signering och dokumentation |Chefer/VD |1 månad |L |5 |
| 4 |Utbildningar utförs inte |Utbildningar krävs minst 1 gång/år. Hyr in konsulter som utbildar fysiskt på plats |HR |6 mån |M |2 |
| 5 |Riskbedöming av leverantörer saknas |införa särskilda rutiner för riskbedömningar vid nya/befintliga avtal |HR |3 mån |M |3 |

- **Kostnad:** L = < 50 KSEK, M = 50–300 KSEK | H = > 300 KSEK
- **Prioritet:** 1 = omedelbart, 5 = kan vänta

---

## Vårt "värsta gap"

**Kontroll nr:2** 

**Varför är detta det värsta gapet?** (max 3 meningar)

```txt
Fungerar inte backupen vid ett angrepp så står företaget stilla. Kunder, personal samt företaget drabbas kraftigt


```

**Vilken är den enskilt viktigaste åtgärden?**

```txt
Att regelbundet testa backuperna. Testerna ska utföras varannan månad och det ska dokumenteras samt signeras av 3e person alt. chef/VD.



```

## Reflektionsfrågor

1. Vilka gap var lättast att identifiera?
2. Vilka gap är "quick wins", det vill säga snabba att åtgärda med liten insats?
3. Vilka gap är svårast att åtgärda och varför? (kultur, kostnad, teknik, beroenden?)
4. Om NordicShop bara fick 500 000 SEK att spendera det första året, vad skulle ni prioritera?

