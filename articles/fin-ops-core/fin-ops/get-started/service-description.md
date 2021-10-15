---
title: Rakenduse Finance and Operations teenuse kirjeldus
description: Selles teemas antakse Finance and Operations rakenduste teenuse kirjeldus.
author: tomhig
ms.date: 09/29/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: whigginb
ms.search.validFrom: 2021-09-03
ms.openlocfilehash: a1547f0cc6c6f705cd0e2ff6e5be751cb97b946a
ms.sourcegitcommit: 79d19924ed736c9210fa9ae4e0d4c41c53c27eb5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/30/2021
ms.locfileid: "7581812"
---
# <a name="service-description-for-finance-and-operations-apps"></a>Rakenduse Finance and Operations teenuse kirjeldus

[!include[banner](../includes/banner.md)]

Finance and Operations rakenduseks on ettevõtte ressursiplaanimise (ERP) tarkvara kui teenuse (SaaS) pakkumine, mis on üles ehitatud ja mis on[Microsoft Azure](https://azure.microsoft.com/overview/what-is-azure/) jaoks. Teenus Finance and Operations pakub organisatsioonidele ERP-funktsiooni, mis toetab nende kordumatuid vajadusi ja aitab neil kohaneda ärikeskkonna muutmisega, ilma et nad nõuaks infrastruktuuride haldamise nõudmist. Finance and Operations rakendus võib sisaldada ühte või enamat järgmistest lahendusealadest:

- [Dynamics 365 Finance](/dynamics365/finance/)
- [Dynamics 365 Human Resources](/dynamics365/human-resources/)
- [Dynamics 365 Supply Chain Management](/dynamics365/supply-chain/)
- [Dynamics 365 Commerce](/dynamics365/commerce/)
- [Dynamics 365 Project Operations](/dynamics365/project-operations/)

Koos [äriteabega](/power-bi/fundamentals/power-bi-service-overview), [infrastruktuuriga](https://azure.microsoft.com/global-infrastructure/), [arvutus](/azure/service-fabric/service-fabric-overview) ja [andmebaasiteenusega](https://devblogs.microsoft.com/azure-sql/running-1m-databases-on-azure-sql-for-a-large-saas-provider-microsoft-dynamics-365-and-power-platform/), võimaldavad need rakendused organisatsioonidel käitada valdkonnaspetsiifilisi ja tegevuspõhiseid äriprotsesse. Kliendid määravad oma rakenduspartneri toetatud ärirakenduse loogika konfiguratsiooni, mis sobib kõige paremini nende kordumatute äriprotsessidega. Funktsioone ja äriprotsesse saab ühe või mitme järgmise lahenduse abil kas laiendada või laiendada:

- Integreeritud [isikupärastamise kogemus](personalize-user-experience.md)
- [Microsoft Power Platform](../../dev-itpro/power-platform/overview.md) tööriistad
- [Visual Studio](https://visualstudio.microsoft.com) põhine [Finance and Operations tarkvara arenduskomplekt (SDK)](../../dev-itpro/dev-tools/developer-home-page.md) ja [Azure DevOps koostamis automatiseerimine](../../dev-itpro/dev-tools/developer-home-page.md#build-automation-using-azure)
- Sõltumatud tarkvara hankija (ISV) lahendused asukohast [AppSource](https://appsource.microsoft.com/partners)

Nõuete põhjal valivad kliendid oma lahenduse lähenemise. Nad töötavad koos oma rakenduspartneriga lahenduse määratlemiseks, arendamiseks ja testimiseks, kasutades parimaid praktikaid, mida pakub rakendus [Microsoft Dynamics Lifecycle Services (LCS)](../../dev-itpro/lifecycle-services/lcs.md). On olemas neli tavalist stsenaariumi:

- Standard Finance and Operations rakenduste "kastist välja" konfiguratsioon (laiendusi pole)
- Finance and Operations rakenduste konfiguratsioon, mis sisaldab üht või enamat ISV-lahendust
- Finance and Operations rakenduste konfiguratsioon, mis sisaldab ühte või enamat kliendiomast laiendust
- Finance and Operations rakenduste konfiguratsioon, mis sisaldab kliendispetsiifiliste laienduste ja ühe või mitme ISV lahenduse kombinatsiooni

Organisatsioonid saavad viia vastavusse oma äritegevuse kasvuga, lisades lihtsa, selge kordustellimuse mudeli kaudu lihtsalt kasutajaid ja äriprotsesse. Lisateavet vaata [Dynamics 365 litsentsensijuhend](https://www.microsoft.com/licensing/docs/view/Microsoft-Dynamics-365).

## <a name="operating-model"></a>Töömudel

Rakenduste Finance and Operations töömudel määrab kindlaid rolle ja kohustusi kliendile, rakenduse partnerile ja Microsoftile kogu teenuse elutsükli jooksul. Lisateavet vt [pilvetoimingud ja nende hooldamine](../../dev-itpro/lifecycle-services/cloud-operations-servicing.md).

### <a name="customer-activities"></a>Kohandatud tegevused

Kliendid töötavad koos oma partneri ja [Microsoft FastTrack`iga](/dynamics365/fasttrack/) jälgides [Success by Design](/dynamics365/fasttrack/success-by-design-overview) raamistikku oma lahenduse rakendamiseks [Lifecycle Services](../../dev-itpro/lifecycle-services/lcs.md) tööriistu ja heade tavade malle. Tavalised tegevused hõlmavad:

- Kasutaja identiteet ja turvahaldus
- Äriprotsesside määratlemine, arendamine ja käitamine
- Laienduste määratlemine, arendamine, testimine ja käitamine
- Tootmisväliste juurutuste jälgimine ja haldamine
- Halda rakenduse värskendusi ja kinnita laiendusi
- ISV-lahenduste ja 3nda osapoole integratsioonide haldamine

### <a name="microsoft-responsibilities"></a>Microsoft`i vastutusalad

Microsoft haldab Finance and Operations teenust, juurutades, jälgides ja hooldades aktiivselt kliendiinfot ja tootmiskeskkondasid Microsoft SaaS-i kordustellimuses. See haldus hõlmab nõutud süsteemi infrastruktuuri jaotamist teenuse käivitamiseks ja ennetavalt sidet klientidega teenuse seisundi kohta. Kohustuste hulka kuuluvad:

**Infrastruktuuri haldus**
- Turvalisus ja isolatsioon
- Operatsioonisüsteemid ja virtuaalsus
- Serverid, ladustamine ja võrgustumine
- Andmekeskuse võimsus, võrgustumine, jahutus

**Rakenduse platvormi haldus**
- 24/7 rakenduse seire ja teatised
- Diagnostika, platvormi uuendused, paigad, teenuse värskendused
- Rakenduse marsruutimine, koormuse tasakaalustamine, saidi süntees
- Keskkonna varustamine ja haldamine
- Andmebaasihaldus, suure saadavusega (HA)/õnnetuse taaste (DR), skaala, toimingud
- Juurutuse arvutamine, suurendamine, vähendamine

## <a name="system-configuration"></a>Süsteemi konfiguratsioon

Finance and Operations rakenduse skaala vastavalt kande mahule ja kasutaja koormusele. Iga kliendi rakendus loob kordumatu lahenduse, mis koosneb järgmistest elementidest:

- **Andmete koosseis** – Unikaalne parameetrite kogum, mis kontrollib käitumist, organisatsiooni paigutust, koondandmete struktuuri (nt finants- ja varude dimensioonid) ning kannete jälgimise detailsust.
- **Laiend ja konfiguratsioon** - koodilaiendeid, ISV-lahendusi ja kordumatuid konfiguratsioone kasutavad laiendusmehhanismid, mis hõlmavad töövooge, integratsioone ja aruande konfiguratsioone.
- **Kasutusmustrid** – kordumatu kombinatsioon võrgu- ja partiikasutusest koos võimalusega integreerida ühendatud andmevoo üles- ja allavoolu süsteemidega ning võimalus teha vahet teabevaadete alusel, mida kliendid oma äriprotsessides kasutavad.

Microsoft konfigureerib kliendi tootmiskeskkonnad, mille suurusega kogused käsitsevad kande mahte ja kasutaja konkurentsust. Microsoft vastutab järgmiste ülesannete eest:

- Tootmiskeskkondade ressursside õige jaotamine, mis põhineb kliendi profileerimisteabel [LCS-i kordustellimuse allutajas](../../dev-itpro/lifecycle-services/subscription-estimator.md)
- Tootmiskeskkondade teenuse kättesaadavuse pidev jälgimine ja diagnoosimine
- Süsteemi jõudlusprobleemide analüüsimine ja tõrkeotsing Finance and Operations rakendustega

Kindlustamaks, et rakendus on konfigureeritud kõrge jõudluse jaoks, peavad kliendid need ülesanded lõpule viima:

- Esitage täpne kasutusteave Finance and Operations juurutamise kohta [LCS-i kordustellimuse hindaja](../../dev-itpro/lifecycle-services/subscription-estimator.md).
- Jõudluse ja ulatuse laiendite ehitamine ja testimine.
- Testige andmekonfiguratsioonid sobivalt jõudluse jaoks.
- Tagage skaleeritavus [tehes jõudluse testimist](https://community.dynamics.com/365/b/techtalks/posts/performance-testing-approach-april-30-2018) enne otseülekannet.

## <a name="onboarding-and-implementation"></a>Rakendamine ja juurutamine

Järgnev tabel näitab tavalisi sisse- ja rakendussündmusi.

| Taotlus | Microsoft`i eeldatav tegevus | Eeldatav kliendi/rakenduspartneri tegevus |
|---|---|---|
| Algne pakkumise ost | Pärast pakkumise ostmist luuakse LCS-projekt, mis põhineb kliendi käivitanud sündmusel. | Läbige Enterprise Agreement (EA) või Cloud Solution Provider (CSP) [äriprotsess](before-you-buy.md). Partner loob kliendile rentniku, kui see on rakendatav. |
| Lisa ost | Andke kliendile juurdepääs lisandmoodulile, mis valitakse rakendamise ajal. | Pole kohaldatav |
| Rakendamise planeerimine ja analüüs | Pakuvad asjassepuutuvaid tööriistu LCS-s, nt [Business process modeler (BPM)](../../dev-itpro/lifecycle-services/bpm-overview.md) ja [koostalitlusvõime rakendusega Azure DevOps](../../dev-itpro/lifecycle-services/synchronize-bpm-vsts.md). | Planeerige projekte, seadistage Azure DevOps, lõpetada süsteemi sisseostmine ja seadistage administraatori kontod. |

Lisateavet vt teemast [Rakendusprojekti juurutamine](../imp-lifecycle/onboard.md).

## <a name="globalization"></a>Globaliseerimine

Finance and Operations rakendusi pakutakse mitmes Azure'i piirkonnas üle terve maailma. Finance and Operations rakendused pakuvad funktsioone eri riikide/regioonide ja emakeelte toetamiseks. Lisateavet vt [lokaliseerimine ja regulatiivsed funktsioonid](../../dev-itpro/lcs-solutions/country-region.md#localization-and-regulatory-features).

### <a name="countryregion-specific-considerations"></a>Riigi-/regioonikohane kaalutlused

- Kliendid reguleeritud tööstuses või äriorganisatsioonides, mil on ärisuhted Prantsusmaa üksustega, mis nõuavad kohalikke andmeid, peaksid üle vaatama [Finance and Operations Prantsusmaal](../../dev-itpro/deployment/france-local-deployment.md).
- Kliendid, kes käitavad operatsioon Hiinas, peaksid läbi vaatama [Finance and Operations 21Vianeti poolt Hiinas](../../dev-itpro/deployment/china-local-deployment.md).
- Kliendid, kel on operatsioone Venemaal, peaksid üle vaatama [Venemaa isikuandmete lokaliseerimise seaduse](/business-applications-release-notes/october18/dynamics365-finance-operations/russian-regulations-on-prem#when-will-the-cloud-deployment-option-of-dynamics-365-for-finance-and-operations-be-generally-available-for-russia).

### <a name="general-data-protection-regulation-gdpr"></a>Isikuandmete kaitse üldmäärus (GDPR)

Finance and Operations rakenduste puhul käitub Microsoft protsessorina. Andmeprotsessorina pakub Finance and Operations protsesse ja funktsioone, mis aitavad klientidel järgida GDPR-kohustusi andmekontrollerina. Lisateavet vt teemast [GDPR ülevaade](../../dev-itpro/gdpr/gdpr-guide.md).

## <a name="environment-and-data-management"></a>Keskkond ja andmete haldus

See jaotis kirjeldab mõningaid tüüpilisi keskkonna- ja andmehalduse sündmusi, mis teenuses toimuvad.

### <a name="environment-and-data-management-events-for-production-instances"></a>Keskkonna- ja andmehalduse sündmused tootmiseksemplaride jaoks

LCS pakub [iseteenindustööriistu](../../dev-itpro/deployment/infrastructure-stack.md) ja [andmebaasi liikumistoiminguid](../../dev-itpro/database/dbmovement-operations.md), mida kasutatakse keskkonna ja andmehalduse ülesannete sooritamiseks. Järgmisena on toodud mõned näited.

**Sündmus:** [Tootmiseksemplari taotlemine](../imp-lifecycle/prepare-go-live.md#requesting-the-production-environment)

- Lõpetage [Go-live'i kontroll-loend](../imp-lifecycle/prepare-go-live.md) ja esitage see [Microsoft FastTrack`i](/dynamics365/fasttrack/) meeskonnale.
- Viige [LCS-i kordustellimuse hindaja](../../dev-itpro/lifecycle-services/subscription-estimator.md) lõpule enne, kui taotlete tootmiseksemplari.
- Viige lõpule kõik rakendusülesanded, mis on määratud [LCS-i metodoloogias](../../dev-itpro/lifecycle-services/create-methodology.md).

**Sündmus:** [Sisendkausta andmebaasi kopeerimine tootmiseksemplari](../../dev-itpro/database/dbmovement-scenario-goldenconfig.md)

- Teostatud näidis live'i minek või tegelik live`i üleminek.

**Sündmus:** [Hooldusrežiim](../../dev-itpro/sysadmin/maintenance-mode.md)

1. Lülitage hooldusrežiim välja.
2. Viige nõutud hooldus lõpule.
3. Lülitage LCS-s hooldusrežiim välja.

### <a name="environment-and-data-management-events-for-non-production-instances"></a>Keskkonna- ja andmehalduse sündmused mittetootmis eksemplaride jaoks

LCS pakub [iseteenindustööriistu](../../dev-itpro/deployment/infrastructure-stack.md) ja [andmebaasi liikumistoiminguid](../../dev-itpro/database/dbmovement-operations.md), mida kasutatakse keskkonna ja andmehalduse ülesannete sooritamiseks. Järgmisena on toodud mõned näited.

**Sündmus:** [uue liivakasti eksemplari juurutamine](../../dev-itpro/deployment/deployenvironment-newinfrastructure.md)

- Veenduge, et kõik nõutud eksemplarid on [plaanitud](../imp-lifecycle/environment-planning.md) ja et rakendatavad lisandmooduli pakkumised on ostetud.
- Juurutamisprotsessi käitamine LCS-s.
- Viige lõpule kõik rakendusülesanded, mis on määratud LCS kontroll-loendis.
    
>[!NOTE]
>Arendusliivakasti keskkond on virtuaalne masin (VM), mis [juurutatatkse Azure'i kordustellimusele](../../dev-itpro/dev-tools/access-instances.md) ja mida haldab klient.

**Sündmus:** [Kuldse konfigurqatsiooni andmebaasi kopeerimine liivakastist tootmisesse](../../dev-itpro/database/dbmovement-scenario-goldenconfig.md)

- Teostatud näidis live'i minek või tegelik live`i üleminek.

**Sündmus:** [tootmisphetke varuplaani taastamine tootmisväliseks eksemplariks](../../dev-itpro/database/database-pitr-prod-sandbox.md)

- Käitage [Andmebaasi värskendamise](../../dev-itpro/database/database-refresh.md) suvand LCS-s.
- Järelkoopia: kustutage või hägustage tundliku loomuga andmeid skriptide kaudu, kohandage keskkonnaspetsiifilisi rakenduse konfiguratsioone (nt integratsiooni lõpp-punktid) ja lubage või lisage kasutajaid. Neid muudatusi tehakse [andmepaketti kasutades](../../dev-itpro/data-entities/data-entities-data-packages.md#import-a-data-package).

**Sündmus:** [tootmisvälise eksemplari andmebaasi ajaline taastamine](../../dev-itpro/database/database-point-in-time-restore.md)

- Aktsepteerige, et protsessi ei saa tagasi võtta.
- Saate käivitada ajapunkti taastamistoimingu LCS-s.

**Sündmus:** 2. järguinfo andmebaasi kopeerimine arenduse tekstiväljale tõrkeotsinguks ja [silumiseks](../../dev-itpro/database/dbmovement-scenario-debugdiag.md)

- Käivitab andmebaasi eksporditoimingu LCS-s 2. järgu kausta keskkonnas.
- Saate importida ja uuendada andmebaasi arenduskeskkonnas.

## <a name="data-backup-and-retention"></a>Andmete varundamine ja säilitamine

Finance and Operations SaaS-i kordustellimuse keskkonnaandmebaasid on automaatsete varundustega kaitstud. Tootmiskeskkondades säilitatakse automaatseid varusid 28 päevaks, kui Microsoft ei tee tagasipööramist. Liivakasti (Tier 2+) keskkondades säilitatakse neid seitsmeks päevaks. Tootmiskeskkonna tagasipööramine on võimalik juhul, kui mis tahes planeeritud hoolduse uuendamise käigus ilmneb tõrge.

Lisateavet automaatsete varunduste kohta vt [automaatsetest varundustest – Azure SQL-andmebaas & SQL-i hallatud eksemplar](/azure/azure-sql/database/automated-backups-overview?tabs=single-database).

## <a name="service-activity-responsibilities"></a>Teenindustegevuse kohustused

Järgmises tabelis kirjeldatakse teenuse tavalisi stsenaariume ja tegevusi. Samuti näitab see, kas Microsoft, klient või mõlemad Microsoft ja klient on tegevuste eest vastutajad.

| Tegevus | Microsoft`i vastutus | Kliendi vastutus |
|---|---|---|
| **Algsete rentnike eraldamine** | | |
| Suurendage LCS-s prognoositava koormuse suurust, kasutades tellimuse hindamise tööriista, ja taotlege teatud keskkondade varustamist. | | X |
| Kõigi tootmiseksemplaride ja mittetootmiseksemplaride ettevalmistamine. | X | |
| Kõigi tootmiseksemplaride ja mittetootmiseksemplaride valideerimine. | | X |
| **Teenuse värskendused** | |
| Rakendage teenuse värskendusi määratud mittetootmis- ja tootmiseksemplaride suhtes. | X | |
| Saate LCS-i teenuseuuendused kastist käsitsi rakendada. Saate määratleda, piiritleda, testida uuendust ning anda koodivärskenduse pakett tagasi LCS-i. | | X |
| Taotlege ja planeerige laienduse uuenduste rakendamist tootmiseksemplari puhul. | | X |
| Looge kood ja andmete varundamine tootmiseksemplari jaoks enne mis tahes uuenduste rakendamist. | X | |
| Tõrke korral tuleb tootmiseksemplar tagasi pöörata koodile ja andmete varundamisele. | X | |
| **Andmehaldus (varundamine, taastamine ja värskendamine)** | | |
| Varundage andmebaas. | X | |
| Määratlege kõrge saadavus ja katastroofide taastamise plaan. | X | |
| Saate jälgida tootmiseksemplari andmebaasi jõudlust. | X | |
| Häälestage tootmisjuhtumite andmebaasi jõudlust. | X | |
| Tootmiseksemplari andmebaasi ajapunkti värskendamine mittetootmiseksemplariks. | | X |
| **Infrastruktuuri uuendamine** | | |
| Plaanige tavalised infrastruktuuri uuendused. | X | |
| **Skaala suurendamine ja vähendamine (kasutajad, ladustamine ja eksemplarid)** | | |
| Ostke lisakasutajaid ja tootmiseväliseid lisandmooduleid. | | X |
| Uuendage kasutusmuudatused LCS-i kordustellimuse hindaja tööriistas. | | X |
| Teatage olulistest jõudlusprobleemidest, mis mõjutavad teenuse kasutamist. | | X |
| Halda ennetavalt ressursse, mis on vajalikud rakendatava teenuse jaoks. | X | |
| Uurida ja teha tõrkeotsinguid. | X | |
| **Turvalisus (kasutaja juurdepääs)** | | |
| Andke kasutajale juurdepääs teenusele. | | X |
| LCS-i projektile juurdepääsu andmine LCS-i kaudu juurutatud eksemplaride haldamiseks ja käitamiseks. | | X |
| **Tootmiseksemplaride seire** | | |
| Tootmisjuhtumite seire 24/7. | X | |
| Teavitage ennetavalt klienti tootmiseksemplari kaasatud juhtumitest. | X | |
| **Mittetootmiseksemplaride haldamine ja seire** | | |
| Hallake mittetootmiseksemplarid LCS-i kasutades. | | X |
| Mittetootmiseksemplaride seire. | | X |

## <a name="service-update-strategy"></a>Teenusevärskenduste strateegia

Vastavalt [tarkvara töötsükli poliitikale](../../dev-itpro/migration-upgrade/versions-update-policy.md), Finance and Operations järgivad rakendused Microsoft [Modern Lifecycle poliitikat](../../dev-itpro/migration-upgrade/versions-update-policy.md#modern-lifecycle-policy), mis hõlmab pidevat hooldust ja toetatud tooteid. 

Microsoft vabastab rakendustele kaheksa Finance and Operations teenusevärskendust igal aastal järgmiste kuude jooksul:

- Jaanuar
- Veebruar
- Aprill
- Mai
- Juuli
- August
- Oktoober
- November

>[!NOTE]
>Aprill ja oktoober on peamised funktsioonide vabastamise lained. Kliendid võivad peatada üksiku teenuse uuendamise kuni kolme järjestikuse uuendamistsükli puhul.

Lisateabe saamiseks vaata järgmisi teemasid:

- [Ühe versiooni teenusevärskenduste ülevaade](../../dev-itpro/lifecycle-services/oneversion-overview.md)
- [Teenusevärskenduste konfigureerimine läbi LCS](../../dev-itpro/lifecycle-services/configure-service-updates.md)
- [Teenusevärskenduste peatamine läbi LCS](../../dev-itpro/lifecycle-services/pause-service-updates.md)
- [Teenusevärskenduste kohta teadete saamine läbi LCS](../../dev-itpro/lifecycle-services/notifications-service-updates.md)
- [Regressioontesti tööriistad teenusevärskenduste kinnitamiseks](../../dev-itpro/perf-test/rsat/rsat-overview.md)
- [Dynamics 365 rtegevuskava ja vabastuse lained](https://dynamics.microsoft.com/roadmap/overview/)

## <a name="security-and-administrative-access"></a>Turvalisus ja administraatori juurdepääs

Haldusjuurdepääs Finance and Operations tootmiskeskkonnale on rangelt kontrollitud ja logitud. Kliendiandmeid käsitletakse vastavalt [Microsoft`i võrguteenuste tingimustele](https://www.microsoft.com/licensing/terms/productoffering). 

### <a name="customer-administrative-access"></a>Kliendi haldusjuurdepääs

Kliendi rentnikuadministraator pääseb juurde tootmiseksemplaridele või mittetootmiseksemplaridele, nagu kirjeldatud järgmises tabelis.

| Keskkonna tüüp | Eesmärk | Kliendi juurdepääsu tase |
|---|---|---|
| **Mitte-tootmine**<br>Järgu 1 liivakast | Mittetootmiskeskkond, mida kliendid juurutavad arendus-, demo- või koolitusotstarbel. | Järgu 1 liivakast (mida nimetatakse ka pilve hostimise keskkonnaks) on kliendi hallatud VM, mis juurutatakse kliendi Azure'i kordustellimusele LCS-is. Kuna see on VM kliendi Azure'i kordustellimuses, on kliendil kaugtöölaua kaudu täielik haldusjuurdepääs keskkonnale. |
| **Mitte-tootmine**<br>2. järgu (või uuem) liivakast | Mittetootmiskeskkond, mille kliendid juurutavad kasutaja aktsepteerimise testimiseks, integratsiooni testimiseks, koolituseks, paigutamiseks või muuks eeltootmisstsenaariumiks. | Järgu 2 ja kõrgemad kaustad juurutatakse Finance and Operations SaaS-i kordustellimusele. Juurdepääs Azure SQL-andmebaasidele mis on seotud mittetootmiskeskkonnaga, antakse [reaalajas juurdepääsu kaudu](../../dev-itpro/database/database-just-in-time-jit-access.md). Kaugtöölaua juurdepääs pole saadaval. |
| **Tootmine** | Tootmiskeskkond juurutatakse siis, kui projekt [on valmis esialgseks otseülekanneks](/imp-lifecycle/environment-planning.md#production-system-readiness). | Tootmiskeskkonnad juurutatakse SaaS-i kordustellimusele. Kogu juurdepääs läbib brauseri, teenuse lõpp-punktid või LCS-i. |

### <a name="microsoft-administrative-access"></a>Microsoft`i haldusjuurdepääs

Järgmine tabel näitab erinevate Microsoft`i administraatorite juurdepääsutasemeid:

| Administraator | Klienditeave |
|---|---|
| Toimingute vastuste meeskond<br>(ainult võtmepersonali suhtes piiratud) | Juurdepääs on antud tugipileti kaudu. Juurdepääs auditeeritakse ja piiratakse tugitegevuse kestusega. |
| Microsoft`i Customer Support Services (CSS) | Pole otsest juurdepääsu. Klient saab kasutada ekraani ühiskasutust, et töötada tugipersonaliga probleemide silumiseks. |
| Tootearendus | Pole otsest juurdepääsu. Operatsioonide vastuse meeskond saab kasutada ekraani ühiskasutust, et töötada inseneritööga probleemide silumiseks. |
| Teised Microsoft`is | Juurdepääs puudub. |

## <a name="monitoring"></a>Seire

Microsoft`il on palju abivahendeid klientide tootmiseksemplaride jälgimiseks ja diagnoosimiseks. Microsoft jälgib klientide tootmiskeskkondasid 24 tundi päevas, 7 päeva nädalas. Lisateavet vt [Tootmise tugi ja seire](../imp-lifecycle/production-support-monitoring.md).

| Microsoft`i vastutus | Kliendi vastutus |
|---|---|
| <ul><li>Saate jälgida teenuse kättesaadavust.</li><li>Jälgige ja teavitage pidevalt tervisemõõdustiku ja jälgija kaudu kriitiliste komponentide nagu Application Object Server (AOS), Batch, Data Import/Export Framework (DIXF), Commerce ja Management Reporter.</li><li>Jälgige jõudluse halvenemist, mis on põhjustatud infrastruktuuriteenustest (nagu näiteks Azure Active Directory \[Azure AD\] ja Azure SQL).</li><li>Kui Microsoft määratleb, et aberratsioone põhjustab üks protsess või pakett-töö, lõpetatakse see protsess või töö pärast kliendiga suhtlemist.</li></ul> | <ul><li>Saate jälgida rakenduse konfiguratsioonide ja laienduste muudatusi, mis võivad põhjustada funktsiooni- ja jõudlusprobleeme.</li><li>Rakendusvead tuleb seiretööriistade abil diagnoosida. Kasutage neid tööriistu kasutaja teatatud jõudluse aberratsioonide diagnoosimiseks.</li><li>Teavitage Microsoft`i, kui süsteemis on oodatud koormust peale eeldatava tippkasutuse.</li><li>Kui rakendatav teenus ei ole tootmiseksemplari puhul saadaval, saab klient kasutada LCS-i [tootmisestaaži aruandeks](../../dev-itpro/lifecycle-services/report-production-outage.md).</li></ul> |

Kui soovite tugitaotlusi LCS-i kaudu võrgus esitada, saavad kliendid Microsoft`il anda kõige efektiivsemal ja tõhusal viisil kiireid ja sügavu tehnilisi teadmisi. Ehkki telefonivalik on saadaval, tuleks seda kasutada ainult siis, kui võrguvalik ei ole saadaval. Lisateabe saamiseks vt [Telefoniteenuse suvandid](/power-platform/admin/support-overview.md?toc=/dynamics365/fin-ops-core/dev-itpro/toc.json&bc=/dynamics365/breadcrumb/toc.json#is-there-a-phone-number-i-can-call-to-contact-support).

## <a name="incident-management"></a>Juhtumite haldamine

Microsoft vastab ja parandab juhtumid tõsidusastmete alusel. Microsoft`i õnnetusjuhtumi tõsidusastmeid saab muuta juhtumi algsel hindamisel ja kuna lisateave mõju ja ulatuse kohta muutub kättesaadavaks. Kui õnnetusjuhtumit leevendatakse, siis õnnetusjuhtumi tõsidusastet ei muudeta.

Lisateavet tõsidusastmete kohta vt [sellest tõsidustabelist](/power-platform/admin/support-overview#what-is-initial-response-time-and-how-quickly-can-i-expect-to-hear-back-from-someone-after-submitting-my-support-request).

## <a name="business-continuity-through-high-availability-and-disaster-recovery"></a>Talitluspidevus suure kättesaadavuse ja õnnetuse taastamise kaudu 

Microsoft pakub äri järjepidevust ja sündmuste taastamist Finance and Operations rakenduste tootmiseksemplaride jaoks Azure'i regiooni hõlmavate rakenduste korral. Lisateavet vt jaotisest [Talitluspidevus ja katastroofist taastumine](../../dev-itpro/sysadmin/business-continuity-disaster-recovery.md).

- **Kõrge saadavus:** HA-funktsioon pakub võimalusi, et vältida ületunnitöö, mille põhjustajaks on ühe sõlme nurjumine Azure'i andmekeskuses. Iga teenuse pilve arhitektuur kasutab Azure'i kättesaadavuse komplekte andmetöötlusjärgu jaoks, et ennetada tõrkeid. Andmebaaside HA-d pakutakse [Azure SQL HA funktsioonide kaudu](/azure/azure-sql/database/high-availability-sla).
- **Õnnetusejärgne taastamine** – [Azure'i õnnetuse taaste funktsioonid](/azure/best-practices-availability-paired-regions) kaitsevad iga teenust, mis mõjutavad laias laastus tervet Azure`i andmekeskust. Mõned neist funktsioonidest:

    - Azure SQL-i aktiivne geograafiline andmeedastus esmasele andmebaasile (äriandmebaas).
    - Azure Blob Storage'i (sisaldab dokumendimanuseid) geograafiliselt üleliigsed koopiad teistes Azure'i piirkondades.
    - Sekundaarne piirkond Azure SQL-i ja Azure Blob Storage replikatsioonide jaoks.

Andmeedastus toetab esmaste andmekaupluste salvestamist. Seetõttu kasutage iga teenuse komponente, nt Management Reporter ja üksuseladu, esmasest andmebaasist üle saadetud andmeid. Need andmed tuleb luua pärast seda, kui taastamise sait on häälestatud ja teenus on käivitatud. Kliendikoodide artefaktide ja taastatud andmekaupluste abil saab saiti uuesti kasutada. Uuestiehtmine võimaldab andmetöötlussõlmede oleku andmeedastust koos oleku ja muude komponentidega kasutada taastatud andmesalvi teisese saidi häälestamiseks. Kui kliendile tootmiseksemplari taastamiseks kasutatakse eksemplari, vastavad Microsoft ja klient oma [juhtumihalduse](service-description.md#incident-management) kohustustele.

Microsoft`i katastroofidest taastamise plaane ja protseduure kontrollitakse regulaarselt System and Organization Controls (SOC) auditi kaudu. Need vastavuse auditid kinnitavad Microsoft`i DR-i, kaasa arvatud Dynamics 365 Finance and Operations rakenduste tehnilist ja protseduurilist protsessi. [SOC vastavus](/compliance/regulatory/offering-soc-2) auditi aruanded ja kõik muud vastavusaruanded on saadaval Microsoft`i [Microsoft Trust Center Compliance Offerings](/compliance/regulatory/offering-home).

| Microsoft`i vastutused | Kliendi vastutused |
|---|---|
| Microsoft sisaldab esmase tootmiseksemplari juurutamisel Azure'i paaristatud andmekeskuse teisese keskkonna. Lisateavet vt jaotisest [Talitluspidevus ja katastroofist taastamine (BCDR): Azure paaritud piirkonnad](/azure/best-practices-availability-paired-regions). | None |
| Microsoft võimaldab esmase tootmiseksemplari juurutamisel kasutada Azure SQL-i ja Azure Blob Storage`i geokoondamist. | None |
| Microsoft võimaldab automaatset Azure SQL-i andmebaaside varundamist. | None |
| <p>Sidekatkestuse ilmnemisel määrab Microsoft, kas kliendi puhul tuleb teha üleminekut ja kas toimub andmekadu. Andmekadu võib olla kuni viis sekundit. Lisateavet vt [Azure SQL-andmebaasi geo-taastamine](https://azure.microsoft.com/blog/azure-sql-database-geo-restore).</p><p>Andmete kaotsimineku korral taotleb Microsoft kliendi sisselogimist tõrke tõttu.</p> | Andmekao korral võib kliendil olla vaja teha mahakandmine, et käivitada ülemineku nurjumine. |
| Tõrke korral töötab rakendatav teenus piiratud režiimis. Uuenduste hooldust ei saa käivitada tõrkesiirderežiimis. | Klient ei saa tõrkerežiimis taotleda paketi juurutamist ega muid regulaarse hoolduse taotlusi. |
| Kui andmekeskus muutub tööks, ebaõnnestub Microsoft tagasi tootmiseksemplari juurde esmases Azure'i regioonis. Normaalsed toimingud jätkuvad. | Võimalik, et klient peab esmases Azure'i regioonis tootmiseksemplari tõrke korral välja logima. |

## <a name="finance-and-operations-support-offerings"></a>Finance and Operations tugiteenuste pakkumine

Tehniline tugi on saadaval turul, kus Finance and Operations teenuseid pakutakse. [Tugikogemusi](../../dev-itpro/lifecycle-services/lcs-support.md) pakutakse LCS-s või Finance and Operations rakendustes. Järgmisena on toodud mõned näited.

- [Teema otsing](../../dev-itpro/lifecycle-services/issue-search-lcs.md) LCS-is
- [Integreeritud tehniline tugi](../../dev-itpro/lifecycle-services/support-experience.md) rakenduses Finance and Operations
- [Pilve-põhine tugi](../../dev-itpro/lifecycle-services/cloud-powered-support-lcs.md) LCS-s

Microsoft pakub Finance and Operations klientidele kolme tugiplaani: esmane, professionaalne ja kordustellimuses sisalduv tugi. Toetuse tase on plaaniti erinev. Järgnev tabel näitab kolme plaani võrdlust.

| Tugifunktsioon | Peamine | Professional Direct | Kordustellimus |
|---|---|---|---|
| Piiramatu katkestuse/parandusjuhtumi esitamine | Jah | Jah | Jah |
| 24/7 juurdepääs LCS-i kaudu | Jah | Jah | Jah |
| Juhtumi reageerimisaeg | Vähem kui tund | Vähem kui tund | Järgmine tööpäev |
| Nõustamisajad | Kaustu hangitakse lepingu alusel. | Ei | Ei |
| Sihtotstarbelise tugikonto haldur | Jah | Ei | Ei |
| Sihtotstarbelise tugiinsener | Tegevuses eraldi lepingu alusel | Ei | Ei |

Lisateavet leiate jaotisest [Toe ülevaade](/power-platform/admin/support-overview).

### <a name="process-to-engage-support"></a>Tugiteenuste kaasamisprotsess

Rakendustega seotud juhtumite korral Finance and Operations rakendustes, esitavad kliendid Microsoft`ile LCS kaudu tugipileteid. CSS tegeleb juhtumitega vastavalt kliendi tugiplaanile ja õnnetusjuhtumi tõsidusastmele, mille on CSS määranud.

### <a name="service-level-agreement"></a>Teenindustaseme leping

Microsoft kooskõlastatud kättesaadavuse määraga 99,9 protsenti teenuse kuu kohta. Kui Microsoft ei saavuta ega säilita teenuse taset, nagu on kirjeldatud teenusetaseme lepingus (SLA), võib kliendil olla õigus saada krediiti osa selle teenuse igakuistest teenustasudest. Teenusekrediidi algatamise kohta leiate teavet jaotise „Nõuded” alt [SLA](https://www.microsoft.com/licensing/docs/view/Service-Level-Agreements-SLA-for-Online-Services).

## <a name="important-resources"></a>Olulised ressursid

- **[Usalduskeskus](https://www.microsoft.com/trust-center)** – saate teavet selle kohta, kuhu Finance and Operations andmed on talletatud, ning täiendavat teavet privaatsuse, vastavuse ja turvaprotseduuride kohta.
- **[Litsentsitingimused ja dokumentatsioon](https://www.microsoftvolumelicensing.com/)** – pääsege kiiresti juurde litsentsitingimustele, tingimustele ja täiendavale teabele, mis on oluline Microsoft`i hulgilitsentsiprogrammi kaudu litsentsitud toodete ja teenuste kasutamisel.
- **[Litsentsitingimused](https://www.microsoft.com/licensing/product-licensing/)** – selle lehe ressursid määravad tingimused tarkvarale ja võrguteenuste toodetele, mida ostate Microsoft`i litsentsiprogrammi kaudu.
- **[Microsofti elutsükli poliitika](/lifecycle/)**– see leht annab järjepidevad ja prognoositavad juhised toe saadavaloleku kohta kogu toote eluea jooksul.
- **[Litsentsimise juhend](https://www.microsoft.com/licensing/docs/view/Microsoft-Dynamics-365)**– kasutage seda juhendit, et saada lisateavet Rakenduse Dynamics 365 litsentsi kohta.
- **[Klienditugi](https://dynamics.microsoft.com/support/)** – hankige valdkonna juhtiv tugi Dynamics 365 rakendustele.
- **[Dynamics Lifecycle Services](https://lcs.dynamics.com/)** – hallake oma rakenduse töötsüklit ja liiguge prognoositavate, korratavate, kõrge kvaliteedi rakenduste suunas.

## <a name="definitions"></a>Definitsioonid

### <a name="azure-region"></a>[Azure’i regioon](/azure/availability-zones/az-overview#regions)

Geograafiline piirkond, kus on üks või mitu Azure'i andmekeskust. Näited hõlmavad USA-d ja Euroopat.

### <a name="business-process-modeler-bpm"></a>[Äriprotsesside modelleerija (BPM)](../../dev-itpro/lifecycle-services/bpm-overview.md)

Tööriist LCS-s, mis aitab täita antud rakenduse sobivuse vahe analüüsi, kasutades rakendustes toetatud äriprotsesside definitsioone American Productivity & Quality Center-ist (APQC), mida toetavad Finance and Operations rakendused.

### <a name="cloud-solution-provider"></a>Pilve lahenduse pakkuja

Partner, mis on osa Microsoft Cloud Solution Provider (CSP) programmist ja mis pakub klientidele lisaväärtusega pilveteenuseid, tuge, üht arvet ja kliendihaldust skaalal.

### <a name="customer"></a>Klient

Äriüksus, mis Finance and Operations tarbib rakendusi ja mida esindab rentnik Office 365 üksuses.

### <a name="development-environment"></a>Arenduskeskkonnad

Tootmisvälise tootmiskausta keskkond, mida kasutatakse laiendite arendamiseks. Kliendid juurutavad seda keskkonda oma LCS-ist pärit Azure'i kordustellimusse. Seda keskkonda saab kasutada ka demonstreerimiseks, koolitusteks või muudeks testimisülesanneteks. Seda nimetatakse ka [Tase 1 liivakast](../imp-lifecycle/environment-planning.md#tier-1-vs-tier-2-and-higher).

### <a name="downtime"></a>Seisakuaeg

Mis tahes periood, mille jooksul kasutajad ei saa oma aktiivsesse rentnikusse sisse logida või nad ei pääse oma aktiivsesse rentnikusse tõrke tõttu, nagu Microsoft määratleb automatiseeritud terviseseirest ja süsteemilogidest. Seisakute hulka ei kuulu planeeritud seisakud, teenuse lisandmoodulite kättesaamatus, teenusele tehtud muudatuste tõttu teenusele juurdepääsu puudumised ega perioodid, mil skaalaühiku võimsus on ületatud.

### <a name="implementation-partner"></a>Juurutuspartner

Partner, mille klient valib oma lahenduste kohandamiseks, konfigureerimiseks, juurutamiseks ja Finance and Operations lahenduste haldamiseks.

### <a name="incident"></a>Juhtum

Probleem, millega kliendid Finance and Operations teenuse kasutamisel kokku puutuvad ja mille kohta nad LCS-i kaudu pileti esitavad.

### <a name="microsoft-customer-support-services-css"></a>Microsoft`i Customer Support Services (CSS)

Microsoft`i globaalne tugimeeskond, mis on mõeldud Finance and Operations rakendustele kvaliteediteenuse pakkumiseks.

### <a name="microsoft-dynamics-lifecycle-services-lcs"></a>Microsoft Dynamics Lifecycle Services (LCS)

Finance and Operations rakenduste elutsükli haldamise haldusportaal alates prooviperioodist kuni juurutamiseni, tootmisjärgse haldamise ja toeni. Lisateabe saamiseks vt [Lifecycle Services ressursid](../../dev-itpro/lifecycle-services/lcs.md).

### <a name="non-production-instance"></a>Mittetootmiseksemplarid

Mis tahes järgmistest teenusejuhtumitest, mida klient kasutab laienduste kinnitamiseks ja muude arendusülesannete täitmiseks:

- **Liivakast Tase 1** – arendaja eksemplar (kliendi majutatud)
- **Kausta Tase 2** – standardne aktsepteerimise testimise eksemplar
- **Liivakast Tase 3–5** – lisa liivakastid

Lisateavet järgud 2 kuni 5 kohta vt õige [järguga 2 või kõrgema keskkonna valimine](../imp-lifecycle/environment-planning.md#selecting-the-correct-tier-2-or-higher-environment).

### <a name="production-instance"></a>Tootmisjuhtum

Finance and Operations keskkond, mida klient kasutab oma "reaalajas" igapäevaste kannete ja äriprotsesside haldamiseks.

### <a name="sandbox-environment"></a>Liivakastikeskkond

Mittetootmiskeskkond, mida klient kasutab demo-, koolitus-, kasutaja kinnituse testimiseks, laienduste valideerimiseks ja muudeks testimisülesanneteks.

### <a name="service"></a>Teenus

Mis tahes tuumteenused, mis on Finance and Operations rakendustes kaasatud.

### <a name="service-level-agreement-sla-for-microsoft-online-services"></a>Microsoft`i võrguteenuste teenusetaseme leping (SLA)

SLA kehtib Microsoft`i võrguteenuste kohta. Lisateavet vt teemast [Service Level Agreements](https://www.microsoft.com/licensing/docs/view/Service-Level-Agreements-SLA-for-Online-Services).

### <a name="service-update"></a>Teenusevärskendus

Microsoft`i teenuste Finance and Operations keskkonnad on teenusevärskenduste kaudu järjepidevad. Kliendid seadistavad oma teenuse värskenduskalendri ärivajaduste alusel. Lisateavet vt teemast [Ühe versiooni teenuse värskendused](../../dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="user"></a>Kasutaja

Üksik isik, kes Finance and Operations keskkondi kasutab ja on seotud kliendi rentnikuga.
