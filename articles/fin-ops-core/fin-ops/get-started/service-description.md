---
title: Finantside ja toimingute rakenduste teenusekirjeldus
description: Selles artiklis antakse finantside ja toimingute rakenduste teenuse kirjeldus.
author: tomhig
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: whigginb
ms.search.validFrom: 2021-09-03
ms.openlocfilehash: 9e5160cc3961703475ffb8dc4a4daf2ae872aaba
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2022
ms.locfileid: "9124921"
---
# <a name="service-description-for-finance-and-operations-apps"></a>Finantside ja toimingute rakenduste teenusekirjeldus

[!include[banner](../includes/banner.md)]

Finantside ja toimingute rakendused on ettevõtte ressursiplaanimise (ERP) tarkvara teenusena (SaaS) pakkumistena, mis on üles ehitatud ja mille jaoks [Microsoft Azure](https://azure.microsoft.com/overview/what-is-azure/). Finantside ja operatsioonide teenus pakub organisatsioonidele ERP-funktsiooni, mis toetab nende kordumatuid vajadusi ning aitab neil kohaneda ärikeskkonna muutmisega, ilma et nad nõuaks infrastruktuuride haldamist. Finantside ja toimingute rakendused võivad sisaldada ühte või enamat järgmist lahendusevaldkonda:

- [Dynamics 365 Finance](/dynamics365/finance/)
- [Dynamics 365 Human Resources](/dynamics365/human-resources/)
- [Dynamics 365 Supply Chain Management](/dynamics365/supply-chain/)
- [Dynamics 365 Commerce](/dynamics365/commerce/)
- [Dynamics 365 Project Operations](/dynamics365/project-operations/)

Koos [äriteabega](/power-bi/fundamentals/power-bi-service-overview), [infrastruktuuriga](https://azure.microsoft.com/global-infrastructure/), [arvutus](/azure/service-fabric/service-fabric-overview) ja [andmebaasiteenusega](https://devblogs.microsoft.com/azure-sql/running-1m-databases-on-azure-sql-for-a-large-saas-provider-microsoft-dynamics-365-and-power-platform/), võimaldavad need rakendused organisatsioonidel käitada valdkonnaspetsiifilisi ja tegevuspõhiseid äriprotsesse. Kliendid määravad oma rakenduspartneri toetatud ärirakenduse loogika konfiguratsiooni, mis sobib kõige paremini nende kordumatute äriprotsessidega. Funktsioone ja äriprotsesse saab ühe või mitme järgmise lahenduse abil kas laiendada või laiendada:

- Integreeritud [isikupärastamise kogemus](personalize-user-experience.md)
- [Microsoft Power Platform](../../dev-itpro/power-platform/overview.md) tööriistad
- [Visual Studio](https://visualstudio.microsoft.com)–põhine [finants- ja operatsioonide tarkvara arenduskomplekt (SDK) ja koostamis](../../dev-itpro/dev-tools/developer-home-page.md)[Azure DevOps automatiseerimine](../../dev-itpro/dev-tools/developer-home-page.md#build-automation-using-azure)
- Sõltumatud tarkvara hankija (ISV) lahendused asukohast [AppSource](https://appsource.microsoft.com/partners)

Nõuete põhjal valivad kliendid oma lahenduse lähenemise. Nad töötavad koos oma rakenduspartneriga lahenduse määratlemiseks, arendamiseks ja testimiseks, kasutades parimaid praktikaid, mida pakub rakendus [Microsoft Dynamics Lifecycle Services (LCS)](../../dev-itpro/lifecycle-services/lcs.md). On olemas neli tavalist stsenaariumi:

- Standardsete finantside ja toimingute rakendused konfiguratsioonist väljas (laiendeid pole)
- Finantside ja toimingute rakenduste konfiguratsioon, mis sisaldab üht või enamat ISV-lahendust
- Finantside ja toimingute rakenduste konfiguratsioon, mis sisaldab ühte või enamat kliendiomast laiendust
- Finantside ja toimingute rakenduste konfiguratsioon, mis sisaldab kliendispetsiifiliste laienduste kombinatsiooni ja üht või enamat ISV-lahendust

Organisatsioonid saavad viia vastavusse oma äritegevuse kasvuga, lisades lihtsa, selge kordustellimuse mudeli kaudu lihtsalt kasutajaid ja äriprotsesse. Lisateavet vaata [Dynamics 365 litsentsensijuhend](https://www.microsoft.com/licensing/docs/view/Microsoft-Dynamics-365).

## <a name="operating-model"></a>Töömudel

Finantside ja toimingute rakenduste tegevusmudel määrab kliendi, rakenduspartneri ja Microsofti jaoks teenuse töötsükli jooksul kindlad rollid ja kohustused. Lisateavet vt [pilvetoimingud ja nende hooldamine](../../dev-itpro/lifecycle-services/cloud-operations-servicing.md).

### <a name="customer-activities"></a>Kohandatud tegevused

Kliendid töötavad koos oma partneri [ja Microsoft FastTrackiga](/dynamics365/fasttrack/)[, järgides Dynamics 365](https://community.dynamics.com/365/dynamics-365-fasttrack/p/dynamics365implementationguide) rakendusjuhendit, [Success by Design](/dynamics365/fasttrack/success-by-design-overview)[raamistikku](../../dev-itpro/lifecycle-services/lcs.md) ning töötsükli teenustes antud tööriistu ja heade tavade malle oma lahenduse rakendamiseks. Tavalised tegevused hõlmavad:

- Kasutaja identiteet ja turvahaldus
- Äriprotsesside määratlemine, arendamiseks ja käitamine
- Laienduste määratlemine, arendamine, testimine ja käitamine
- Tootmisväliste juurutuste jälgimine ja haldamine
- Halda rakenduse värskendusi ja kinnita laiendusi
- ISV-lahenduste ja 3nda osapoole integratsioonide haldamine

### <a name="microsoft-responsibilities"></a>Microsoft`i vastutused

Microsoft haldab finantside ja toimingute teenust, juurutades, jälgides ja hooldades klientide märkeruutu ja tootmiskeskkondasid Microsoft SaaS-i kordustellimuses. See haldus hõlmab nõutud süsteemi infrastruktuuri jaotamist teenuse käivitamiseks ja ennetavalt sidet klientidega teenuse seisundi kohta. Kohustuste hulka kuuluvad:

**Infrastruktuuri haldus**
- Turvalisus ja isolatsioon
- Operatsioonisüsteemid ja virtuaalsus
- Serverid, ladustamine ja serverid
- Andmekeskuse võimsus, võrgustumine, jahutus

**Rakenduse platvormi haldus**
- 24/7 rakenduse seire ja teatised
- Diagnostika, platvormi uuendused, paigad, teenuse värskendused
- Rakenduse marsruutimine, koormuse tasakaalustamine, saidi süntees
- Keskkonna varustamine ja haldamine
- Andmebaasihaldus, suure saadavusega (HA)/õnnetuse taaste (DR), skaala, toimingud
- Juurutuse arvutamine, suurendamine, vähendamine

## <a name="system-configuration"></a>Süsteemi konfiguratsioon

Finantside ja toimingute rakenduste skaala vastavalt kande mahule ja kasutaja koormusele. Iga kliendi rakendus loob kordumatu lahenduse, mis koosneb järgmistest elementidest:

- **Andmete koosseis** – Unikaalne parameetrite kogum, mis kontrollib käitumist, organisatsiooni paigutust, koondandmete struktuuri (nt finants- ja varude dimensioonid) ning kannete jälgimise detailsust.
- **Laiend ja konfiguratsioon** - koodilaiendeid, ISV-lahendusi ja kordumatuid konfiguratsioone kasutavad laiendusmehhanismid, mis hõlmavad töövooge, integratsioone ja aruande konfiguratsioone.
- **Kasutusmustrid** – kordumatu kombinatsioon võrgu- ja partiikasutusest koos võimalusega integreerida ühendatud andmevoo üles- ja allavoolu süsteemidega ning võimalus teha vahet teabevaadete alusel, mida kliendid oma äriprotsessides kasutavad.

Microsoft konfigureerib kliendi tootmiskeskkonnad, mille suurusega kogused käsitsevad kande mahte ja kasutaja konkurentsust. Microsoft vastutab järgmiste ülesannete eest:

- Tootmiskeskkondade ressursside õige jaotamine, mis põhineb kliendi profileerimisteabel [LCS-i kordustellimuse allutajas](../../dev-itpro/lifecycle-services/subscription-estimator.md)
- Tootmiskeskkondade teenuse kättesaadavuse pidev jälgimine ja diagnoosimine
- Süsteemi jõudlusprobleemide analüüsimine ja tõrkeotsing finantside ja toimingute rakendustega

Kindlustamaks, et rakendus on konfigureeritud kõrge jõudluse jaoks, peavad kliendid need ülesanded lõpule viima:

- Esitage täpne kasutusteave LCS-i kordustellimuste hindaja finantside [ja toimingute rakendamise kohta](../../dev-itpro/lifecycle-services/subscription-estimator.md).
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

Finantside ja toimingute rakendusi pakutakse mitmetest Azure'i aladelt üle terve maailma. Finantside ja toimingute rakendused pakuvad funktsioone eri riikide/regioonide ja emakeelte toetamiseks. Lisateavet vt [lokaliseerimine ja regulatiivsed funktsioonid](../../dev-itpro/lcs-solutions/country-region.md#localization-and-regulatory-features).

### <a name="countryregion-specific-considerations"></a>Riigi-/regioonikohane kaalutlused

- Kliendid reguleeritud tööstusharus või äriorganisatsioonides, mis on ärisuhted [Prantsusmaa üksustega, mis nõuavad kohalikke andmeid, peaksid läbi vaatama Finantsid ja toimingud Prantsusmaal](../../dev-itpro/deployment/france-local-deployment.md).
- Kliendid, kes käitavad Hiina operatsioone, peaksid üle vaatama [Azure China Playbooki](/azure/china/) ja [Finantsid ning toiminguid, mida haldab 21Vianet Hiinas](../../dev-itpro/deployment/china-local-deployment.md).
- Kliendid, kel on operatsioone Venemaal, peaksid üle vaatama [Venemaa isikuandmete lokaliseerimise seaduse](/business-applications-release-notes/october18/dynamics365-finance-operations/russian-regulations-on-prem#when-will-the-cloud-deployment-option-of-dynamics-365-for-finance-and-operations-be-generally-available-for-russia).

### <a name="general-data-protection-regulation-gdpr"></a>Isikuandmete kaitse üldmäärus (GDPR)

Finantside ja toimingute rakenduste puhul tegutseb Microsoft protsessorina. Andmeprotsessorina pakuvad finantsid ja toimingud protsesse ja funktsioone, mis aitavad klientidel JÄRGIda GDPR-kohustusi andmekontrollerina. Lisateavet vt teemast [GDPR ülevaade](../../dev-itpro/gdpr/gdpr-guide.md).

## <a name="environment-and-data-management"></a>Keskkond ja andmete haldus

See jaotis kirjeldab mõningaid tüüpilisi keskkonna- ja andmehalduse sündmusi, mis teenuses toimuvad.

### <a name="environment-and-data-management-events-for-production-instances"></a>Keskkonna- ja andmehalduse sündmused tootmiseksemplaride jaoks

LCS pakub [iseteenindustööriistu](../../dev-itpro/deployment/infrastructure-stack.md) ja [andmebaasi liikumistoiminguid](../../dev-itpro/database/dbmovement-operations.md), mida kasutatakse keskkonna ja andmehalduse ülesannete sooritamiseks. Järgmisena on toodud mõned näited.

**Sündmus:** [Tootmiseksemplari taotlemine](../imp-lifecycle/go-live-faq.md#when-can-i-configure-and-request-my-production-environment)

- Lõpetage Go-live'i [valmisoleku ülevaade](../imp-lifecycle/prepare-go-live.md) ja esitage see [Microsoft FastTracki meeskonnale](/dynamics365/fasttrack/).
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

SaaS-i kordustellimuse finants- ja toimingute keskkondade andmebaasid on automaatsete varundustega kaitstud. Tootmiskeskkondades säilitatakse automaatseid varusid 28 päevaks, kui Microsoft ei tee tagasipööramist. Liivakasti (Tier 2+) keskkondades säilitatakse neid seitsmeks päevaks. Tootmiskeskkonna tagasipööramine on võimalik juhul, kui mis tahes planeeritud hoolduse uuendamise käigus ilmneb tõrge.

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

Vastavalt tarkvara töötsükli [poliitikale](../../dev-itpro/migration-upgrade/versions-update-policy.md) järgivad finantsid ja toimingute rakendused Microsoft [Moderni elutsükli poliitikat](../../dev-itpro/migration-upgrade/versions-update-policy.md#modern-lifecycle-policy), mis hõlmab pidevat hooldust ja toetatud tooteid. 

Microsoft pakub finantside ja toimingute rakenduste jaoks igal aastal järgmiste kuude kohta kaheksa teenusevärskendust:

- jaanuar
- veebruar
- aprill
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

Finantside ja toimingute tootmiskeskkonna haldusjuurdepääs on rangelt kontrollitud ja logitud. Kliendiandmeid käsitletakse vastavalt [Microsoft`i võrguteenuste tingimustele](https://www.microsoft.com/licensing/terms/productoffering). 

### <a name="customer-administrative-access"></a>Kliendi haldusjuurdepääs

Kliendi rentnikuadministraator pääseb juurde tootmiseksemplaridele või mittetootmiseksemplaridele, nagu kirjeldatud järgmises tabelis.

| Keskkonna tüüp | Eesmärk | Kliendi juurdepääsu tase |
|---|---|---|
| **Mitte-tootmine**<br>Järgu 1 liivakast | Mittetootmiskeskkond, mida kliendid juurutavad arendus-, demo- või koolitusotstarbel. | Järgu 1 liivakast (mida nimetatakse ka pilve hostimise keskkonnaks) on kliendi hallatud VM, mis juurutatakse kliendi Azure'i kordustellimusele LCS-is. Kuna see on VM kliendi Azure'i kordustellimuses, on kliendil kaugtöölaua kaudu täielik haldusjuurdepääs keskkonnale. |
| **Mitte-tootmine**<br>2. järgu (või uuem) liivakast | Mittetootmiskeskkond, mille kliendid juurutavad kasutaja aktsepteerimise testimiseks, integratsiooni testimiseks, koolituseks, paigutamiseks või muuks eeltootmisstsenaariumiks. | Järgu 2 ja kõrgemad kaustad juurutatakse finantside ja toimingute SaaS-i kordustellimusele. Juurdepääs Azure SQL-andmebaasidele mis on seotud mittetootmiskeskkonnaga, antakse [reaalajas juurdepääsu kaudu](../../dev-itpro/database/database-just-in-time-jit-access.md). Kaugtöölaua juurdepääs pole saadaval. |
| **Tootmine** | Tootmiskeskkond juurutatakse siis, kui projekt [on valmis esialgseks otseülekanneks](../imp-lifecycle/environment-planning.md#production-system-readiness). | Tootmiskeskkonnad juurutatakse SaaS-i kordustellimusele. Kogu juurdepääs läbib brauseri, teenuse lõpp-punktid või LCS-i. |

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

Kui soovite tugitaotlusi LCS-i kaudu võrgus esitada, saavad kliendid Microsoft`il anda kõige efektiivsemal ja tõhusal viisil kiireid ja sügavu tehnilisi teadmisi. Ehkki telefonivalik on saadaval, tuleks seda kasutada ainult siis, kui võrguvalik ei ole saadaval. Lisateabe saamiseks vt [Telefoniteenuse suvandid](/power-platform/admin/support-overview?toc=%2Fdynamics365%2Ffin-ops-core%2Fdev-itpro%2Ftoc.json&bc=%2Fdynamics365%2Fbreadcrumb%2Ftoc.json#is-there-a-phone-number-i-can-call-to-contact-support).

## <a name="incident-management"></a>Juhtumite haldamine

Microsoft vastab ja parandab juhtumid tõsidusastmete alusel. Microsoft`i õnnetusjuhtumi tõsidusastmeid saab muuta juhtumi algsel hindamisel ja kuna lisateave mõju ja ulatuse kohta muutub kättesaadavaks. Kui õnnetusjuhtumit leevendatakse, siis õnnetusjuhtumi tõsidusastet ei muudeta.

Lisateavet tõsidusastmete kohta vt [sellest tõsidustabelist](/power-platform/admin/support-overview#what-is-initial-response-time-and-how-quickly-can-i-expect-to-hear-back-from-someone-after-submitting-my-support-request).

## <a name="business-continuity-through-high-availability-and-disaster-recovery"></a>Talitluspidevus suure kättesaadavuse ja õnnetuse taastamise kaudu 

Microsoft pakub äri järjepidevust ja sündmuste taastamist finantside ja toimingute rakenduste tootmiseksemplaride jaoks Azure'i regiooni hõlmavate ülekatkestuste korral. Lisateavet, k.a teenuse taastamise ajaeesmärk (TOOL) ja taastepunkti eesmärk (RPO), vt [talitlus järjepidevust ja katastroofide taastamist](../../dev-itpro/sysadmin/business-continuity-disaster-recovery.md).

- **Kõrge saadavus:** HA-funktsioon pakub võimalusi, et vältida ületunnitöö, mille põhjustajaks on ühe sõlme nurjumine Azure'i andmekeskuses. Iga teenuse pilve arhitektuur kasutab Azure'i kättesaadavuse komplekte andmetöötlusjärgu jaoks, et ennetada tõrkeid. Andmebaaside HA-d pakutakse [Azure SQL HA funktsioonide kaudu](/azure/azure-sql/database/high-availability-sla).
- **Õnnetusejärgne taastamine** – [Azure'i õnnetuse taaste funktsioonid](/azure/best-practices-availability-paired-regions) kaitsevad iga teenust, mis mõjutavad laias laastus tervet Azure`i andmekeskust. Mõned neist funktsioonidest:

    - Azure SQL-i aktiivne geograafiline andmeedastus esmasele andmebaasile (äriandmebaas).
    - Azure Blob Storage'i (sisaldab dokumendimanuseid) geograafiliselt üleliigsed koopiad teistes Azure'i piirkondades.
    - Sekundaarne piirkond Azure SQL-i ja Azure Blob Storage replikatsioonide jaoks.

Kui kliendile tootmiseksemplari taastamiseks kasutatakse eksemplari, vastavad Microsoft ja klient oma [juhtumihalduse](service-description.md#incident-management) kohustustele.

Microsoft`i katastroofidest taastamise plaane ja protseduure kontrollitakse regulaarselt System and Organization Controls (SOC) auditi kaudu. Need vastavuse auditid testivad Microsofti tehnilise ja protseduuriprotsessi, sealhulgas Dynamics 365 finantside ja toimingute rakendusi. [SOC vastavus](/compliance/regulatory/offering-soc-2) auditi aruanded ja kõik muud vastavusaruanded on saadaval Microsoft`i [Microsoft Trust Center Compliance Offerings](/compliance/regulatory/offering-home).

## <a name="finance-and-operations-support-offerings"></a>Finantside ja toimingute tugiteenustega seotud tegevused

Tehniline tugi on saadaval turus, kus pakutakse finants- ja operatsioonide teenuseid. [Tugikogemusi](../../dev-itpro/lifecycle-services/lcs-support.md) pakutakse LCS-s või finantside ja toimingute rakendustes. Järgmisena on toodud mõned näited.

- [Teema otsing](../../dev-itpro/lifecycle-services/issue-search-lcs.md) LCS-is
- [Integreeritud tehniline tugi finantside](../../dev-itpro/lifecycle-services/support-experience.md) ja toimingute rakendustes
- [Pilve-põhine tugi](../../dev-itpro/lifecycle-services/cloud-powered-support-lcs.md) LCS-s

Microsoft pakub finantsilisi ja operatsioonide kliente kolme tugiplaani:Rendi, Professional Direct ja tellimuses kaasatud tugi. Toetuse tase on plaaniti erinev. Järgnev tabel näitab kolme plaani võrdlust.

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

Finantside ja toimingute rakendusi hõlmavad juhtumid edastavad kliendid LCS-i kaudu Microsoftile tugiteenuseid. CSS tegeleb juhtumitega vastavalt kliendi tugiplaanile ja õnnetusjuhtumi tõsidusastmele, mille on CSS määranud.

### <a name="service-level-agreement"></a>Teenindustaseme leping

Microsoft kooskõlastatud kättesaadavuse määraga 99,9 protsenti teenuse kuu kohta. Kui Microsoft ei saavuta ega säilita teenuse taset, nagu on kirjeldatud teenusetaseme lepingus (SLA), võib kliendil olla õigus saada krediiti osa selle teenuse igakuistest teenustasudest. Teenusekrediidi algatamise kohta leiate teavet jaotise „Nõuded” alt [SLA](https://www.microsoft.com/licensing/docs/view/Service-Level-Agreements-SLA-for-Online-Services).

## <a name="important-resources"></a>Olulised ressursid

- **[Usalduskeskus](https://www.microsoft.com/trust-center)** – hankige teavet finantside ja toimingute andmete talletustingimuste kohta ning täiendavat teavet privaatsuse, vastavuse ja turvaprotseduuride kohta.
- **[Litsentsitingimused ja dokumentatsioon](https://www.microsoftvolumelicensing.com/)** – pääsege kiiresti juurde litsentsitingimustele, tingimustele ja täiendavale teabele, mis on oluline Microsoft`i hulgilitsentsiprogrammi kaudu litsentsitud toodete ja teenuste kasutamisel.
- **[Litsentsitingimused](https://www.microsoft.com/licensing/product-licensing/)** – selle lehe ressursid määravad tingimused tarkvarale ja võrguteenuste toodetele, mida ostate Microsoft`i litsentsiprogrammi kaudu.
- **[Microsofti elutsükli poliitika](/lifecycle/)**– see leht annab järjepidevad ja prognoositavad juhised toe saadavaloleku kohta kogu toote eluea jooksul.
- **[Litsentsimise juhend](https://www.microsoft.com/licensing/docs/view/Microsoft-Dynamics-365)**– kasutage seda juhendit, et saada lisateavet Rakenduse Dynamics 365 litsentsi kohta.
- **[Klienditugi](https://dynamics.microsoft.com/support/)** – hankige valdkonna juhtiv tugi Dynamics 365 rakendustele.
- **[Dynamics Lifecycle Services](https://lcs.dynamics.com/)** – hallake oma rakenduse töötsüklit ja liiguge prognoositavate, korratavate, kõrge kvaliteedi rakenduste suunas.
- **[Dynamics 365](https://aka.ms/D365ImplementationGuideFlip)** rakendusjuhend – Dynamics 365 Success by Design rakendusjuhend dokumenteerib aja jooksul läbiproovitud põhimõtted ja annab arhitektile, koostada, katsetada ja juurutada Dynamics 365 lahendusi.

## <a name="definitions"></a>Definitsioonid

### <a name="azure-region"></a>[Azure’i regioon](/azure/availability-zones/az-overview#regions)

Geograafiline piirkond, kus on üks või mitu Azure'i andmekeskust. Näited hõlmavad USA-d ja Euroopat.

### <a name="business-process-modeler-bpm"></a>[Äriprotsesside modelleerija (BPM)](../../dev-itpro/lifecycle-services/bpm-overview.md)

LCS-i tööriist, mis aitab täita antud rakenduse sobivuse vahe analüüsi, kasutades Ameerika tööviljakuse & kvaliteedikeskuse (APQC) äriprotsesside definitsioone, mida toetatakse finantside ja toimingute rakendustes.

### <a name="cloud-solution-provider"></a>Pilve lahenduse pakkuja

Partner, mis on osa Microsoft Cloud Solution Provider (CSP) programmist ja mis pakub klientidele lisaväärtusega pilveteenuseid, tuge, üht arvet ja kliendihaldust skaalal.

### <a name="customer"></a>Klient

Äriüksus, mis kasutab finantside ja toimingute rakendusi ning mida esindab rentnik üksuses Office 365.

### <a name="development-environment"></a>Arenduskeskkond

Tootmisvälise tootmiskausta keskkond, mida kasutatakse laiendite arendamiseks. Kliendid juurutavad seda keskkonda oma LCS-ist pärit Azure'i kordustellimusse. Seda keskkonda saab kasutada ka demonstreerimiseks, koolitusteks või muudeks testimisülesanneteks. Seda nimetatakse ka [Tase 1 liivakast](../imp-lifecycle/environment-planning.md#tier-1-vs-tier-2-and-higher).

### <a name="downtime"></a>Seisakuaeg

Mis tahes periood, mille jooksul kasutajad ei saa oma aktiivsesse rentnikusse sisse logida või nad ei pääse oma aktiivsesse rentnikusse tõrke tõttu, nagu Microsoft määratleb automatiseeritud terviseseirest ja süsteemilogidest. Seisakute hulka ei kuulu planeeritud seisakud, teenuse lisandmoodulite kättesaamatus, teenusele tehtud muudatuste tõttu teenusele juurdepääsu puudumised ega perioodid, mil skaalaühiku võimsus on ületatud.

### <a name="implementation-partner"></a>Juurutuspartner

Partner, mille klient valib oma finantside ja toimingute lahenduste kohandamiseks, konfigureerimiseks, rakendamiseks ja haldamiseks.

### <a name="incident"></a>Juhtum

Klientide jaoks finants- ja operatsioonide teenuse kasutamisel ilmnes probleem ja LCS-i kaudu pileti esitamine.

### <a name="microsoft-customer-support-services-css"></a>Microsoft`i Customer Support Services (CSS)

Microsofti globaalne tugimeeskond, mis on suunatud kvaliteediteenuse pakkumisele finantside ja toimingute rakenduste jaoks.

### <a name="microsoft-dynamics-lifecycle-services-lcs"></a>Microsoft Dynamics Lifecycle Services (LCS)

Halduse portaal finantside elutsükli haldamiseks ja toimingute rakenduste jaoks alates proovist, rakendamisest kuni tootmisjärgse halduse ja toeni. Lisateabe saamiseks vt [Lifecycle Services ressursid](../../dev-itpro/lifecycle-services/lcs.md).

### <a name="non-production-instance"></a>Mittetootmiseksemplarid

Mis tahes järgmistest teenusejuhtumitest, mida klient kasutab laienduste kinnitamiseks ja muude arendusülesannete täitmiseks:

- **Liivakast Tase 1** – arendaja eksemplar (kliendi majutatud)
- **Kausta Tase 2** – standardne aktsepteerimise testimise eksemplar
- **Liivakast Tase 3–5** – lisa liivakastid

Lisateavet järgud 2 kuni 5 kohta vt õige [järguga 2 või kõrgema keskkonna valimine](../imp-lifecycle/environment-planning.md#selecting-the-correct-tier-2-or-higher-environment).

### <a name="production-instance"></a>Tootmisjuhtum

Finants- ja toimingute keskkond, mida klient kasutab oma "reaalajas" igapäevaste kannete ja äriprotsesside haldamiseks.

### <a name="sandbox-environment"></a>Liivakastikeskkond

Mittetootmiskeskkond, mida klient kasutab demo-, koolitus-, kasutaja kinnituse testimiseks, laienduste valideerimiseks ja muudeks testimisülesanneteks.

### <a name="service"></a>Teenindus

Mis tahes tuumteenused, mis on kaasatud finantside ja toimingute rakendustesse.

### <a name="service-level-agreement-sla-for-microsoft-online-services"></a>Microsoft`i võrguteenuste teenusetaseme leping (SLA)

SLA kehtib Microsoft`i võrguteenuste kohta. Lisateavet vt teemast [Service Level Agreements](https://www.microsoft.com/licensing/docs/view/Service-Level-Agreements-SLA-for-Online-Services).

### <a name="service-update"></a>Teenusevärskendus

Microsofti teenuste finantsid ja toimingute keskkonnad on teenuse värskenduste kaudu järjepidevad. Kliendid seadistavad oma teenuse värskenduskalendri ärivajaduste alusel. Lisateavet vt teemast [Ühe versiooni teenuse värskendused](../../dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="success-by-design"></a>[Success by Design](/dynamics365/fasttrack/success-by-design-overview)

Raamistik, mis juhendab süsteemselt rakendust kriitilise järguga hindamise seeria kaudu, et tagada Dynamics 365 lahenduse optimaalne ülesehitus, turvalisus, jõudlus ja kasutajakogemus.

### <a name="user"></a>Kasutaja

Üksik isik, kes kasutab finants- ja tegevuskeskkondasid ning on seotud kliendi rentnikuga.

