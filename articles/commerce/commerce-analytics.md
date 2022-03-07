---
title: Commerce Analytics (eelvaade)
description: Selles teemas üksikasjad analüüsivõimaluste installist ja kasutamisest selles Dynamics 365 Commerce.
author: AamirAllaq
ms.date: 11/15/2021
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2021-11-12
ms.openlocfilehash: 7f3e51cc3f7314bd33bca9e598bd0b1c9118caef
ms.sourcegitcommit: 9f8da0ae3dcf3861e8ece2c2df4f693490563d5e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/16/2021
ms.locfileid: "7817454"
---
# <a name="commerce-analytics-preview"></a>Commerce Analytics (eelvaade)

[!include [banner](includes/banner.md)]

Commerce'i analüüs on rakendusesse kaasatud funktsionaalne analüüs Dynamics 365 Commerce. See teema kirjeldab üksikasjalikult Commerce'i analüüsi ja selgitab selle installimist. 

## <a name="system-architecture"></a>Süsteemi ülesehitus
### <a name="key-components"></a>Põhikomponendid
Commerce Analytics koosneb järgmistest võtmekomponentidest:
- Interaktiivsete aruannete kasutamiseks Power BI valmis
- SQL-i vaated Azure Synapse analüüsis
- Üksus ja ontoloogiaandmed teenuses Azure DataEtt
- Toorandmed Azure Data Azure'is

![Commerce Analyticsi süsteemiarhitektuur](media/CommerceAnalytics.png)

### <a name="data-flow"></a>Andmevoog
#### <a name="step-1-data-generation"></a>1. etapp: andmete loomine
Andmed pärinevad kas kandeandmetena või käitumusandmetena ühest järgmistest allikatest:
- Kõnekeskuse seostamine Commerce HQ kliendi abil müügitellimuste töötlemiseks
- Kassapidaja müügikohas (POS) müügikannete töötlemine
- Kohandatud rakendustes loodud müük, kasutades Headless Commerce'i (Commerce Scale Unit)
- E-commerce'i ostleja sirvimine oma e-äri veebisaidi sirvimisel 
- E-commerce'i ostleja, kes paigutab tellimuse teie e-äri veebisaidile
- Teiste süsteemidega, nagu näiteks süsteemiga < a1/& loodud andmed Dynamics 365 Connected Spaces

#### <a name="step-2-ingestion-and-pre-processing"></a>2. etapp: sisseseadmine ja eeltöötlus
Kandeandmed sisestavad Commerce HQ kas otse (otse Commerce HQ-kliendis hõivatud tellimused) või Commerce Scale Unitilt (kassas, e-kaubanduses või kohandatud klientarvutites hõivatud tellimused, kasutades Headless Commerce'i). 

Kandeandmed kopeeritakse seejärel funktsiooniGa Ekspordi Data Feature toorandmetena Azure Data Ülekandesse ja andmed talletatakse **·** kausta "Tabelid". E-äri veebitegevuse andmed saadetakse otse andmetesse.

Teiste süsteemide toodetud andmed, nagu Dynamics 365 Connected Spaces näiteks, saadetakse otse andmetesse.

#### <a name="step-3-transformation-and-aggregation"></a>3. etapp: teisendamine ja liitmine
Kui toorandmed on andmekaustas, loeb Commerce Analytics Service andmeid, teisendab ja koondab need tagasi andmeüksusesse kausta "Üksused" loogiliste olemite kujul ja koondab meetermõõdud kaustas "Ontologies". 

#### <a name="step-4-querying"></a>4. etapp: päringud
Liidese T-SQL kaudu päringusse tiksatud andmeid Azure Synapse analüüsi abil. Liides hõlmab SQL-i vaadei, mis võimaldavad andmete liitpäringuid kas otse T-SQL-i klienti sihtanalüüsiks kasutades või sellise visualiseerimistööriista nagu Power BI.

#### <a name="step-5-modeling-and-serving"></a>5. etapp: modelleerimine ja teenimine
Analüüsi kaudu Azure Synapse päringusse tehtud andmed lähevad siis Power BI semantilisele mudelile. Olenevalt andmetüübist imporditakse see kas perioodiliselt mälus või on see Power BI käitusaja jooksul otse päringusse esitatud. 

Viimane etapp on andmete renderdamine visuaalsetes Power BI andmetes, mida kasutajad saavad vaadata ja nendega suhelda. 

## <a name="commerce-analytics-functional-overview"></a>Commerce Analyticsi funktsionaalne ülevaade
### <a name="1-summary"></a>1. Kokkuvõte
#### <a name="top-level-filters"></a>Ülemise taseme filtrid
1.  Kuupäevasätted
    1. Aasta
    2. Kvartal    
    3. Kuu    
    4. Nädal    
    5. Päev
2. Kanali sätted
    1. Juriidiline isik    
    2. Kanali tüüp    
    3. Kliendi tüüp    
    4. Müügi tüüp    
    5. Kanal    
    6. Organisatsioonihierarhia
3. Tootesätted
    1. Kategooriahierarhia    
    2. Kategooria

#### <a name="a-product"></a>a. Toode
1. Müük
2. Marginaal
3. Tagastused

#### <a name="b-customer"></a>b. Klient
1. Müük
2. Marginaal
3. Tagastused

#### <a name="c-channel"></a>c. Kanal
1. Müük
2. Marginaal
3. Tagastused

### <a name="2-sales"></a>2. Müük
1. Tarne asukoha järgi
2. Kanali/kaupluse/terminali järgi
3. Töövõtja alusel
4. Kuupäeva järgi
5. Tunni järgi
6. Tootekategooria alusel

### <a name="3-margin"></a>3. Veeris
1. Tarne asukoha järgi
2. Kõrvalsaadus
3. Kuupäeva järgi

### <a name="4-return"></a>4. Tagastamine
1. Tagastus summa järgi
    1. Kaupluse alusel    
    2. Kõrvalsaadus    
    3. Kuupäeva järgi
2. Tagastus kande alusel
    1. Kaupluse alusel    
    2. Kõrvalsaadus    
    3. Kuupäeva järgi

### <a name="5-discount"></a>5. Allahindlus
1. Kaupluse alusel
2. Kõrvalsaadus
3. Kuupäeva järgi
4. Eraldamine
    1. Juriidiline isik    
    2. Kauplus    
    3. Allahindluse tüüp    
    4. Allahindluse nimi    
    5. Toode

### <a name="6-payment"></a>6. Makse
1. Kanali/terminali järgi
2. Makseviisi/-tüübi alusel
3. Kuupäeva järgi
4. Eraldamine
    1. Juriidiline isik    
    2. Kanali tüüp    
    3. Kauplus    
    4. Terminal    
    5. Makseviis

### <a name="7-customer"></a>7. Klient
1. Eluea väärtus (LTV): eluaja väärtus arvutatakse kliendi poolt kõikide Äriregistri kanalite (POS, e-commerce ja kõnekeskus) kogu kulutatud summa põhjal.
2. Recency – recency arvutatakse päevade arvu põhjal, mis on möödunud kliendi viimasest tehingust organisatsiooniga. Recency ei arvesta kandeväliseid teenuse tugevusi, nagu näiteks e-kaubanduse sirvimistegevus.
3. Sagedus: sagedus arvutatakse kliendi kandepõhise seotuse alusel organisatsiooniga. Sagedus ei arvesta kandeväliseid teenuse annab signaali, nagu näiteks e-kaubanduse sirvimistegevus.
4. Seose pikkus: seose pikkus arvutatakse päevade arvu põhjal alates kliendikirje loomisest süsteemis. 
5. Kannete arv

### <a name="8-comparison"></a>8. Võrdlus
1. Toote võrdlus ajaperioodi alusel
    1. Müügi- ja müügierinevus
    2. Marginaali ja marginaali erinevus
2. Klient ajaperioodi alusel
    1. Müügi- ja müügierinevus
    2. Marginaali ja marginaali erinevus

### <a name="9-web-activity"></a>9. Veebitegevus

#### <a name="top-level-filters"></a>Ülemise taseme filtrid
1. Kuupäevavahemik
2. Kanali tüüp
3. Kanal
4. Kategooriahierarhia

#### <a name="a-acquisition"></a>a. Soetus
1. Lehekülje vaated
    1. Riigi/regiooni järgi    
    2. Kõrvalsaadus    
    3. Kasutaja sisse logitud olek    
    4. Kuupäeva järgi
2. E-äri tellimused
3. Valuutakurss
    1. Kuupäeva järgi
4. Teisenduse leht
    1. Lehevaade lehe tüübi järgi (avaleht, kategooria lehekülg, toote üksikasjade leht)  
    2. Lisa korvi    
    3. Maksmine   
    4. Ost

#### <a name="b-session"></a>b. Seanss
Seanss on määratletud kasutaja külastuste seansina teie e-äri veebisaidile. Seanss loetakse lõpetatuks pärast 30 minutit passiivsust või pärast 24 tundi aktiivset kasutamist.
1. Riigi/regiooni järgi
2. Päritolu järgi (väline viitaja)
3. Kasutaja sisse logitud olek
4. Seansiloendus
    1. Kuupäeva järgi    
    2. Sisestuslehe järgi
5. Tellimus seansi kohta
    1. Kuupäeva järgi
6. Seansi määra määraks on seanss määratletud kui seanss, kus kasutaja lahkub kohe pärast teie e-äri veebisaidi külastamist. 
7. Klõpsab seansi kohta

#### <a name="c-visitor"></a>c. Külastaja
Teie e-kaubanduse saidi anonüümne nimi määratakse kordumatu ID põhjal selle konkreetse seadme brauseri piires. Commerce Analytics ei jälgi anonüümseid kasutajaid eri brauserites või seadmetes. Anonüümne kasutaja, kes kasutab sama brauserit samal arvutil määratakse kordumatult mitme kasutajaseansi lõikes, kuni brauseri vahemälu andmed on tühjendatud või tavaliselt kuni 12 kuu perioodini, olenevalt sellest, kumb toimub esimesena.

Commerce analytics võib anda teile rohkem teavet oma e-äri saiti sisse loginud meiliaadresside sirvimise kohta. Teave põhineb olemasolevatel suhetel nende kasutajatega, kaasa arvatud ostud, mida kasutajad on teie organisatsioonist sooritanud kõigis Commerce'i müügikanalites (POS, kõnekeskus ja e-commerce) ning kaasab hiljutisuse, seose pikkuse, eluea väärtuse ja sageduse.

1. Veeris
2. Keskmised ligemahinnaga tellimused
3. Keskmine keskmine müügisumma
4. E-commerce'i countus
    1. Kuupäeva järgi
    2. Asukoha alusel: ärianalüüs saab anda riigi/regiooni tasemel ainult e-kaubanduse vihjete jaoks granulaarsust.     
    3. Hiljutisuse (recency) puhul arvutatakse Recency päevade arvu alusel, mis on möödunud kliendi viimasest tehingust organisatsiooniga. Recency ei arvesta kandeväliseid teenuse tugevusi, nagu näiteks e-kaubanduse sirvimistegevus.    
    4. Seose pikkuse alusel: seose pikkus arvutatakse päevade arvu põhjal alates kliendikirje loomisest süsteemis.     
    5. Eluea väärtuse (LTV) alusel: eluea väärtus arvutatakse kliendi kulutatud kogusumma alusel kõigis Commerce'i müügikanalites (POS, e-commerce ja kõnekeskus).
    6. Sageduse järgi– sagedus arvutatakse kliendi organisatsiooniga seotud kandepõhise seotuse põhjal. Sagedus ei arvesta kandeväliseid teenuse annab signaali, nagu näiteks e-kaubanduse sirvimistegevus.

#### <a name="d-impression"></a>p Mulje
Esmamulje määratletakse iga toote visuaalse vaatena e-kaubanduse kaudu. Näiteks kui e-kaubanduse vihje navigeerib teie veebisaidi avalehele ja vaadete põhjal vaadete mati toode ülemise müügiloendi moodulis ning samuti kuvatakse sama mati toode valikus teie loendimoodulile, loetakse need suhtlused kaheks tootemuljeks. Näitamised jälgivad tootevaateid järgmistel pinnal:
1. Loendid (nt soovitatav, tippmüümine, teile valikuid valiv, trendid)
2. Ostukorvimoodul
3. Otsingutulemuse konteiner
4. Kategooria otsingutulemuse konteiner
    
Värvimoodulis või kohandatud visuaalis renderdatud tooteid ei arvestata näitamismõõdikutes.

**Näitamise** aruandeleht sisaldab järgmisi mõõdulehti:
1. Näitamiste arv
    1. Lehekülje tüübi ja mooduli järgi: lehe tüüp on üldine lehetüüp, mis on määratletud iga lehe jaoks teie e-äri veebisaidil. Mooduli tüüp määratleb e-kaubanduse visuaalse mooduli tüübi, milles toode kuvatakse. Teil võib tekkida vajadus minna süvitsi leheküljel ja moodulis visuaalselt, et vaadata teateid moodulite järgi.    
    2. Kõrvalsaadus    
    3. Kasutaja sisse logitud olek    
    4. Kuupäeva järgi
2. Näitamise klõpsamiste arv: esmamulje klõpsamine on määratletud kui e-kaubanduse ikoonil klõpsamine toote visuaalsel valikul, mis tavaliselt navigeerib kasutajaid selle toote toote üksikasjade lehele.     
3. Näitamise läbimismäär (CTR): läbim klõpsamismäär on määratletud kui kuvamisk klõpsamiste koguarv, mis on jagatud kuvamiste koguarvu arvuga.

## <a name="install-commerce-analytics"></a>Commerce Analyticsi installimine

> [!NOTE]
> Commerce analytics on eelvaate faasis Ameerika Ühendriikides, Kanadas, Ühendkuningriigis, Euroopas, Lõuna-Ida-Aasias, Ida-Aasias, Austraalias ja Jaapanis. Kui teie keskkond asub mingis nimetatud regioonis, saate oma keskkonnas lubada Commerce Analyticsi koos Microsoft Dynamics elutsükli teenustega (LCS). Enne Commerce Analyticsi kasutamist vaadake teemat [Eksportimise konfigureerimine azure Data Commerce'i](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

### <a name="enable-and-configure-commerce-analytics"></a>Commerce Analyticsi lubamine ja konfigureerimine
Commerce Analyticsi installimiseks on vaja luba ressursside loomiseks Azure'i kordustellimuses ja luba lisandmoodulite installimiseks LCS-is. Commerce Analyticsi lubamiseks ja konfigureerimiseks läbige allpool kirjeldatud etapid.
1. [Commerce Analyticsi (eelvaade) eelvaate vormi esitamine](#submit-the-preview-intake-form-for-commerce-analytics).
2. [Lubage ja konfigureerige Eksport Andmetesse](#enable-and-configure-export-to-data-lake).
3. [Lubage ja konfigureerige Commerce Analyticsi (Eelvaade) lisandmoodul](#enable-and-configure-commerce-analytics-add-in).
4. [Saate luua ladustamiskonto SAS-i](#generate-storage-account-sas-token) loa.
5. [Laadi vaadete jaoks alla Azure Synapse juurutusskriptid.](#download-deployment-scripts-for-azure-synapse-views)
6. [Installige ja konfigureerige Azure Synapse](#install-and-configure-azure-synapse-workspace) tööruum.
7. [Installi Power BI](#install-power-bi-template-app) mallirakendus. 

### <a name="submit-the-preview-intake-form-for-commerce-analytics"></a>Commerce Analyticsi eelvaate vormi esitamine
Vormi Commerce [analytics (Preview) täielik ja esitamine](https://forms.office.com/r/vW5VLJGXZ2) Lubage taotluse töötlemiseks kuni kolm tööpäeva. Kui vorm on töödeldud, saadetakse kinnitusmeil vormil antud meiliaadressile.

### <a name="enable-and-configure-export-to-data-lake"></a>Andmetesse eksportimise lubamine ja konfigureerimine Selle teabega
Commerce analytics toetub rakenduse Commerce HQ andmete eksportimiseks Azure Data Azure'i funktsiooni ekspordiga ja säilitab **·** andmed värskena. Enne Commerce'i analüüsi konfigureerimist lubage ja konfigureerige AndmeteSeosse eksportimine, järgides **·** Azure Data [Analyticsi eksportimise konfigureerimise](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md) etappe. Funktsiooni Ekspordi **andmetesse** konfigureerimisel pange tähele järgmist teavet. Selle teabe peate sisestama järgmistesse etappidesse.
1. Võtme vault DNS-i nimi ja salanimed, kuhu te rakenduse ID ja rakenduse saladuse salvestate. Lisateavet vt jaotisest [Turvahoidlasse saladuste](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#addsecrets) lisamine.
2. Ladustamiskonto nimi eksemplari Azure Data Azure'i jaoks. Lisateavet vt oma [kordustellimuses konto Data Storage (Gen2)](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createsubscription) loomine.

### <a name="enable-and-configure-commerce-analytics-add-in"></a>Commerce Analyticsi lisandmooduli lubamine ja konfigureerimine
Commerce Analyticsi lisandmooduli installimiseks LCS-i peate olema LCS-i keskkonnaadministraator keskkonnas, mida plaanite kasutada.

Commerce Analyticsi lisandmooduli konfigureerimiseks vajate järgmist teavet. 

|Field | Teabeallikas| Näide|
|----|----|----|
|Azure AD Rentniku ID teie keskkonna jaoks| Teie Azure AD rentniku ID Azure'i portaalis. Logige sisse **Azure'i portaali** ja avage **Azure Active Directory** teenus. Avage lehekülg **·** Atribuudid ja kopeerige väärtus väljale Kausta **·** ID.| 72f988bf-0000-0000-00000-2d7cd011db47|
|Teie võtme VAUlt DNS-i nimi|Sisestage [oma võtme](#enable-and-configure-export-to-data-lake) vault'i DNS-i nimi.| `https://contosod365datafeedpoc.vault.azure.net/`|
|Avalduse ID-d sisaldav saladus| Sisestage [avalduse](#enable-and-configure-export-to-data-lake) ID talletamissaladuse nimi. See on sama väärtus, mida kasutasite **Data Lisamise lisamise installimisel Data Lisamise** installimisel.|app-id|
|Rakendussaladust sisaldav saladus| Sisestage [avalduse](#enable-and-configure-export-to-data-lake) saladust talletav salanimi. See on sama väärtus, mida kasutasite **Data Lisamise lisamise installimisel Data Lisamise** installimisel.| app-secret|

1. Logige sisse [elutsükli](https://lcs.dynamics.com/) teenustesse ja navigeerige oma keskkonda.
2. Valige **lehel** Keskkond vahekaart Keskkonna **·** lisandmoodulid.
3. Valige **suvand Installi uus lisandmoodul ja valige dialoogiboksis** **Ärianalüüs (eelvaade).** Kui **ärianalüüsi (Preview)** loendis pole, kontrollige, et olete Insider Programiga ühendatud.
4. Sisestage **dialoogiboksis** Seadistuse lisandmoodul nõutud teave, nagu ülaltoodud tabelis kirjeldatakse.
5. Nõustuge pakkumise tingimustega, märkides ruudu ja seejärel valige **·** Installi.

Süsteem installib ja konfigureerib keskkonna Commerce Analyticsi (Eelvaade). Toiminguks võib olla mõni minut. Pärast installi ja konfigureerimise lõpetamist **on Commerce Analytics (Preview) loetletud lehel Keskkond ja olek on** **·** **Installitud**.

### <a name="generate-storage-account-sas-token"></a>Ladustamise konto SAS-i loa loomine
> [!NOTE]
> Commerce Analyticsi (Eelvaade) tuntud piirang on see, et kui SAS-i luba aegub, kaotab eksemplar juurdepääsu Azure Synapse andmele. Peate seadistama oma organisatsiooni turvapoliitikas lubatud maksimaalse aegumiskuupäeva, kui genereerite sastud ühiskasutusega juurdepääsu allkirja (SAS) loa.

SAS-i luba võimaldab välisüksustel pääseda juurde teie ladustamiskontole koos kindla privileegide komplektiga piiratud aja jooksul. Azure Synapse kasutab SAS-i luba, et pääseda juurde Azure Data Azure'i andmete põhiandmetele. SAS-i loa loomiseks täitke alltoodud juhised.
1. Minge andmete eksportimise konfigureerimisel Loodud Azure'i portaali ladustamiskontole, nagu on välja toodud kordustellimuses andmete **·** Storage [(Gen2) konto](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createsubscription) loomisel.
2. Vasakul **oleval** suvandite paanil salvestuskonto all valige **ühiskasutusega juurdepääsu allkiri.**
3. Valige SAS-i valikute lehel järgmised valikud:

    | Valiku nimi | Suvandi väärtus |
    |-------------|--------------|
    | Lubatud teenused | Valige **bloobi** valik. |
    | Lubatud ressursitüübid | Valige **·** teenus, **konteiner** ja **·** objekt.|
    | Lubatud õigused | Valige **·** lugemine, **·** kirjutamine, **·** kustutamine, **·** **·** loend, lisamine ja **·** loomine. |
    | Bloobiversioonide õigused | Lubab **versioonide** kustutamise. |
    | Alguskuupäev ja aegumiskuupäev/-kellaaeg | Seadistage sass-loa lõppkuupäev ja -kellaaeg vastavalt vajadusele. |
    | Lubatud IP-aadressid | Jäta tühjaks. |
    | Lubatud protokollid | Valige **ainult** HTTPS. |
    | Eelistatud protsessikiht | Valige **baas** (vaikimisi). |
    | Allkirjastamisvõti | Valige **vastavalt** vajadusele võti **1 või** klahv2. |

4. Valige **Loo SAS ja ühendusstring.**
5. Kopeerige väärtus **SAS-i loa** tekstiboksi tekstiredaktorisse nagu Notepad.

### <a name="download-deployment-scripts-for-azure-synapse-views"></a>Laadi vaadete jaoks alla Azure Synapse juurutusskriptid
Vajalike vaadete loomiseks ja Azure Synapse avaldamiseks tööruumis peate laadima alla ja käivitama skriptide komplekti. Skriptide allalaadimiseks viige lõpule järgmised sammud.
1. Avage rakendus [microsoft/Dynamics365Commerce.Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions) GitHub repo. Skriptid on saadaval repongis.
2. Skriptide alla laadimiseks kohalikku arvutisse saate skripte kasutada nii rakenduse tele, kui ka skript on sihtfailina alla laaditud.

### <a name="install-and-configure-azure-synapse-workspace"></a>Tööruumi installimine ja Azure Synapse konfigureerimine
Tööruumi installimiseks ja Azure Synapse konfigureerimiseks läbige alltoodud juhised.
1. Installige Azure Synapse tööruum oma Azure'i kordustellimuses, järgides [QuickStartis toodud etappe: looge Sünonüüm.](/azure/synapse-analytics/quickstart-create-workspace)
2. Avage Notepadis setupSapse.sql-skriptifail kohaliku arvuti kaustast, kus te laadisite või laadisite alla Dynamics365Commerce.Solutionsi uuesti. Lisateavet vaadake jaotisest [Kuvade juurutusskriptide Azure Synapse](#download-deployment-scripts-for-azure-synapse-views) allalaadimine. Skriptifail asub kaustas "/Pipeline/CommerceAnalyticsexiapse/". Redigeerige skripti, et asendada kohatäite tekst allolevate väärtustega.

   | Kohatäite tekst | Asendusväärtus |
   |------------------|-------------------|
   | placeholder_storageaccount | Asendage andmete eksportimise konfigureerimisel loodud ladustamiskonto nimega, nagu on kirjeldatud tellimuses Data **·** Storage [(Gen2) konto](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createsubscription) loomisel. |
   | <a name="phContainer"></a> placeholder_container | Asendage pärast LCS-ist andmeekspordi lisandmooduli **LCS-i eksportimist Teie Azure Data Azure'i eksemplaris loodud ladustamisümbrise** nimega. Konteineri nime saamiseks peate talletuskonto sirvimiseks kasutama Azure'i portaalis lao explorer. |
   | placeholder_sastoken | Asenda ladustamise konto SAS-i loaga kopeeritud [SAS-i](#generate-storage-account-sas-token) loaga. Eemaldage kindlasti **"?"** SAS-i loa väärtuse algusest. |
   | <a name="phUserPwd"></a> placeholder_password | Asendage oma valiku tugeva parooliga. Tehke parooli kohta märkus. Parool seadistatakse skriptis loodud uue kasutaja reportreadonlyuser paroolina. **ÄRGE** sisestage siia konto sqladminuser parooli.  |

3. Minge uuele tööruumile Azure Synapse Azure'i portaalis. Valige **ülevaate lehel suvand Ava Sünapse** **·** Studio.
4. Kopeerige selle `SetupSynapse.sql` sisu, mida uuendas ülal sammus 2. Valige Sünapse Studios Azure'i portaalis **> SQL-skripti jaoks** uus. Kleebi sisu SQL-skripti redaktorisse Sünapse Studios.
5. **Kontrollige, kas andmebaasi kasutamine on seatud** väärtusele **·** Koond. Skripti **·** käivitamiseks valige käsk Käita.
6. Oodake, kuni skript lõpetatakse. Skript loob andmebaasi Commerce Analyticsi jaoks, mandaadi juurdepääsuks Azure DataAatidele ja kirjutuskaitstud kasutajakonto, mida kasutatakse eksemplariga Power BI ühenduse Azure Synapse loomiseks.
7. Avage kohalikus arvutis PowerShell haldusrežiimis. Minge kausta "/Pipeline/CommerceAnalyticsSapiapse/" kaustas, kuhu te kogusite või laadisite alla Dynamics365Commerce.Solutionsi uuesti, nagu on kirjeldatud vaadete allalaadimise [Azure Synapse juurutusskriptis.](#download-deployment-scripts-for-azure-synapse-views)
8. PowerShelli käivitamispoliitika häälestamiseks käivitage PowerShelli aknas järgmine käsk:

   ```powershell
   Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
   ```
   
9. Installige SQL Server PowerShelli moodul, käivitades PowerShelli aknas järgmise käsu:

   ```powershell
   Install-Module sqlserver
   ```
   
   > [!NOTE]
   > Kui teil on juba SQL Serveri moodul installitud, võite selle sammu vahele jätta. Selle mooduli installimise ajal võidakse teilt küsida pakkuja NuGet installimist. Vajutage **pakkuja** installimise jätkamiseks klahvi NuGet Y. Võite saada ka teate, et installite moodulid ebausaldusväärsest hoidlast. Installi **jätkamiseks vajutage klahvi Y.** Võite hoidlat usaldamiseks `Set-PSRepository` käivitada ka `PSGallery` cmdlet-käsu.
   
10. Avaldage Azure Synapse vaated, kasutades PowerShelli aknas järgmist käsku:

    ```powershell
    .\PublishSynapseViews.ps1 -serverName SERVER_NAME -password PASSWORD -storageAccount STORAGE_ACCOUNT -containerName CONTAINER_NAME -datarootpath DATA_ROOT_PATH
    ```
    
    Asendage käsu kohatäiteväärtused järgmiselt:
    
    | Kohatäite väärtus | Asendusväärtus |
    |-------------------|-------------------|
    | SERVER_NAME | Asenda serverita Azure Synapse SQL-i lõpp-punkti nimega. Selle väärtuse saate Azure'i Azure Synapse portaali **tööruumi ülevaate** lehelt. |
    | PAROOL | Asendage sqladminuseri parooliga. |
    | STORAGE_ACCOUNT | Asendage laokonto nimega Azure Data Azure'i jaoks. |
    | CONTAINER_NAME | Asendab konteineri nimega, mis loodi **ekspordiga Data Theo.** Nimi on samale konteinerile, mille määrasid [ülalma placeholder_container](#install-and-configure-azure-synapse-workspace) väärtuses. |
    | DATA_ROOT_PATH | Asendab kausta nimega konteineri all, mis sisaldab kõiki andmeid. |

    > [!NOTE]
    > Talletuskonto nime, konteineri nime ja andmete juurtee leiate Azure'i portaalist, kasutades Azure'i laobrauseli oma Azure Data Azure'i salvestuskontoga.

11. Oodake, kuni skript lõpetatakse. Skript loob serverita SQL-i Azure Synapse eksemplaris SQL-vaated.

### <a name="install-power-bi-template-app"></a>Installi Power BI mallirakendus
Commerce Power BI Analyticsi mallirakenduse installimiseks läbige järgmised sammud.
1. Logige oma organisatsiooni [Power BI](https://powerbi.microsoft.com/) ID abil portaali sisse.
2. Installige rakenduse Commerce Power BI analytics mall, st [https://aka.ms/cdireport-installapp](https://aka.ms/cdireport-installapp). Võite saada hoiatuse rakenduse loetlemata AppSource kohta. Valige **Installi**.
3. Kui te installite rakenduse esmakordselt, jätkake sammuga 5. Kui rakendus on juba installitud, esitatakse teile rakenduse uuendamiseks järgmised valikud.
   1. Värskendage tööruumi ja rakendust: see suvand värskendab olemasolevat mallirakendust ja kirjutab üle rakenduse sätted, nagu rakenduse eksemplari nimi ja õiguste konfiguratsioonid.
   2. Värskendage tööruumi sisu ilma rakendust värskendamata: see suvand värskendab olemasolevat mallirakendust ja säilitab rakenduse sätted. See on **·** rakenduse uuendamiseks soovitatav valik.
   3. Installige rakenduse teine koopia uude tööruumi. See suvand loob rakenduse uue koopia uude tööruumi, mis luuakse teie jaoks. Olemasolev tööruum on alles.      
4. Valige üks neist suvanditest ja seejärel **·** installi.
5. Avage installitud rakendus, **valides** vasakul paanil menüü Apps (Rakendused) üksuse ja valides seejärel rakenduse.
6. Ühendage rakendus andmeallikaga, valides **·** ühenduse. Kui see pole rakenduse esmakordsel installimisel, valige **suvand Ühenda andmed** kollasel teaberibal.
7. Sisestage järgmised parameetriväärtused:

   | Parameetri nimi | Väärtus |
   |----------------|-------|
   | Server       | Sisestage jaotistes Installi ja Konfigureeri tööruum loodud serverita Azure Synapse [SQL-lõpp-punkti Azure Synapse](#install-and-configure-azure-synapse-workspace) nimi. Selle väärtuse leiate Azure Synapse Azure'i portaali tööruumi ülevaate **·** lehelt. |
   | Andmebaas | Sisestage väärtus CommerceAnalytics.
   | Keel | Valige ripploendist soovitud väärtus. Sätet kasutatakse teie lokaliseeritud toote- ja kategoorianimede jaoks. Väärtus on case-tundlik. |
   | Kuupäevavahemik | Valige ripploendist soovitud väärtus. Valitud kuude arvu andmed imporditakse Power BI andmekomplekti. Andmekomplekti suurus ja sünkroonimiseks vajalik aeg sõltuvad valitavast väärtusest. |

8. Valige **Edasi**. Teil palutakse sisestada mandaadid SQL-andmebaasiga ühenduse Azure Synapse loomiseks. Sisestage järgmised väärtused:

   | Parameetri nimi | Väärtus |
   |----------------|-------|
   |Autentimismeetod|Valige **·** põhiline.|
   |Kasutajanimi| Sisestage "reportreadonlyuser".|
   |Parool|Sisestage väärtus, mida kasutate placeholder_password [...](#install-and-configure-azure-synapse-workspace) SetupSexiapse.sql skriptis. See on kasutaja reportreadonlyuser konto parool.| 

9. Valige **sisselogimine ja looge** ühendus.
10. Oodake, kuni andmekomplekti värskendatakse. Seejärel minge rakenduse tööruumi, valides **ikooni Redigeeri** rakendust. Saate kontrollida tööruumi andmekomplekti värskendusolekut. Saate ka oma andmekomplektile automaatvärskenduse graafikuid seadistada, õigusi hallata ja rakenduseeksemplari ümber nimetada.

### <a name="privacy"></a>Privaatsus
Teie privaatsus on meie jaoks oluline. Lisateavet privaatsuse kohta leiate meie [privaatsusavaldusest.](https://go.microsoft.com/fwlink/?LinkId=521839)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
