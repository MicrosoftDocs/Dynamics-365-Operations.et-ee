---
title: Aegunud funktsioonid
description: "See teema kirjeldab funktsioone, mis on eemaldatud või plaanitakse eemaldada."
author: sericks007
manager: AnnBe
ms.date: 07/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Platform, UnifiedOperations
ms.custom: 21821
ms.assetid: 31019808-4cbf-47d7-b1ba-d791db4281ae
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 6
ms.translationtype: HT
ms.sourcegitcommit: c73eeaaf28df8db720431d4bcd317c9721baa99d
ms.openlocfilehash: 3ebe8f2869b93050d320456ff457c0b5692c5eae
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="deprecated-features"></a>Aegunud funktsioonid

[!include[banner](../includes/banner.md)]

See teema kirjeldab funktsioone, mis on rakendusest Microsoft Dynamics 365 for Finance and Operations, Enterprise edition eemaldatud või mida plaanitakse eemaldada.

## <a name="features-that-have-been-deprecated-in-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017-with-platform-update-8"></a>Dynamics 365 for Finance and Operations, Enterprise editionist 2017. aasta juuli 8. platvormivärskendusega eemaldatud funktsioonid

### <a name="warehouse-mobile-devices-portal"></a>Lao mobiilsete seadmete portaal

Lao mobiilsete seadmete portaal (WMDP) oli eraldiseisev komponent, mis oli mõeldud ise toimivaks asutusesiseseks juurutamiseks. Microsoft Dynamics 365 for Finance and Operations, Enterprise edition ei toeta enam seda komponenti. WMDP funktsiooni on asendanud kasutajakogemust parandav omarakendus. 

|                                  |                                                 |
|----------------------------------|-------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Topeltfunktsioon.                        |
| **Asendatud teise funktsiooniga?** | Jah. See funktsioon on asendatud Finance and Operationsi ladustamise mooduliga. Lisateavet seadistamise ja eeltingimuste kohta leiate jaotisest [Microsoft Dynamics 365 for Finance and Operationsi mooduli Ladustamine installimine ja konfigureerimine](../../supply-chain/warehousing/install-configure-warehousing-app.md). |
| **Mõjutatud moodulid**             | Laohaldus, transpordihaldus |

### <a name="advanced-bank-reconciliation-matching-rule-for-manual-matching"></a>Täpsema panga vastavusseviimise vastavusreegel käsitsi sobitamiseks

Vastavusreeglit kasutati pangadokumendi valimiseks ja märkimiseks, kui dokumente vastavusseviimise töölehel käsitsi sobitati.

|                                  |                                                                                        |
|----------------------------------|----------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Piiratud kasutus.                                                                         |
| **Asendatud teise funktsiooniga?** | Nr Dokumentide leidmiseks, et neid vastavusse viia, tuleks kasutada veeru filtreerimise võimalusi. |
| **Mõjutatud moodulid**             | Sularaha- ja pangahaldus                                                               |

### <a name="windows-8-tablet-app"></a>Windows 8 tahvelarvuti rakendus

Windows 8 tahvelarvuti rakendus pakkus kulude sisestamise ja kinnitamise funktsioone.

|                                  |                                                                                          |
|----------------------------------|------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Finance and Operations ühildub tahvelarvutitega. Tahvelarvuti rakendust pole enam vaja. |
| **Asendatud teise funktsiooniga?** | Nr                                                                                      |
| **Mõjutatud moodulid**             | Kulude haldus                                                                       |


## <a name="features-that-have-been-deprecated-in-dynamics-365-for-operations-1611-with-platform-update-3"></a>Funktsioonid, mis on aegunud rakeduses Dynamics 365 for Operations 1611 platvormivärskendusega 3

### <a name="aeb-payment-formats-for-spain"></a>AEB maksevormingud Hispaania puhul

Consejo Superior Bancario maksevorminguid kasutatakse rahaülekandefailide saatmiseks panka kliendimaksete ja tarnijamaksete puhul. Nende vormingute sisu määrab Asociación Española de Banca. See hõlmab järgmist: Cuaderno 19 32 58 34.

|                              |                                                                          |
|------------------------------|--------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Maksevorminguid enam ei kasutata.                                  |
| **Asendatud teise funktsiooniga?** | Jah, ISO20022 kreeditiülekanne ja otsedeebeti maksevormingud Hispaania puhul |
| **Mõjutatud moodulid**             | Müügireskontro, ostureskontro                                    |

### <a name="bank-payments-transfer-for-lithuania"></a>Pangamaksete ülekanne Leedu puhul

Pangamakse ülekanded luuakse ja prinditakse, kasutades Leedu makseülekande ekspordivormingut. Leedu turg alustas LITAS-i (ühtlustatud elektroonilise pangandussüsteem) kasutamist 2005. aastal.

|                              |                                                            |
|------------------------------|------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Maksevorminguid enam ei kasutata.                    |
| **Asendatud teise funktsiooniga?** | Yes, ISO20022 kreeditiülekande maksevorming Leedu puhul |
| **Mõjutatud moodulid**             | Ostureskontro                                           |

### <a name="bbs-direkte-remittering-payment-formats-for-norway"></a>BBS Direkte Remitteringi maksevormingud Norra puhul

BBS Direkte Remitteringi maksevormingud hõlmavad kliendimakse kogumise eksporti (otsene deebet) ja tagastusteate importi.

|                              |                                                                                                                                                                |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Maksevorminguid enam ei kasutata.                                                                                                                        |
| **Asendatud teise funktsiooniga?** | AvtaleGiro Norra kliendimakse vormingut saab kasutada otsedeebeti teadete loomiseks. Tagastusteate importi juurutatakse tulevastes väljalasetes. |
| **Mõjutatud moodulid**             | Müügireskontro, ostureskontro                                                                                                                          |

### <a name="chart-of-accounts-tool-for-spain"></a>Kontoplaani tööriist Hispaania puhul

Seda tööriista kasutatakse siis, kui kontoplaan nõuab Hispaanias suuremaid muudatusi. Kasutajad saavad importida uue kontoplaani Microsoft Excelis või tekstivormingus ja saavad ka importida finantsaruandeid.

|                              |                |
|------------------------------|----------------|
| **Kasutuselt eemaldamise põhjus**       | Piiratud kasutus  |
| **Asendatud teise funktsiooniga?** | Ei             |
| **Mõjutatud moodulid**             | Pearaamat |

### <a name="dom80-payment-format-for-belgium"></a>Dom80 maksevorming Belgia puhul

Belgia pärandi maksevorming makse kogumiseks (otsedeebet).

|                              |                                                        |
|------------------------------|--------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**      | Maksevormingut enam ei kasutata.                  |
| **Asendatud teise funktsiooniga?** | Jah, ISO 20022 otsedeebeti maksevorming Belgia puhul |
| **Mõjutatud moodulid**            | Müügireskontro                                    |

### <a name="dtaezag-payment-formats-for-switzerland"></a>DTA/EZAG maksevormingud Šveitsi puhul

DTA-/EZAG-vormingud integreeritakse ESR-i süsteemi, kuna need saavad olla viitenumbril. Kuna viitenumber ei ole kohustuslik, saab neid vorminguid kasutada mis tahes hankija maksete töötlemiseks. Neid vorminguid kasutavad ettevõtted, millel on pangakonto asukohas, mis ei ole „finantsijärgne”.

|                              |                                                              |
|------------------------------|--------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Maksevorminguid enam ei kasutata.                      |
| **Asendatud teise funktsiooniga?** | Yes, ISO20022 kreeditiülekande maksevorming Šveitsi puhul |
| **Mõjutatud moodulid**             | Ostureskontro                                             |

### <a name="edifact-dirdeb-payment-format-for-austria"></a>EDIFACT-DIRDEB-i maksevorming Austria puhul

EDIFACT-DIRDEB-i maksevorming makse kogumiseks (otsedeebet).

|                              |                                                        |
|------------------------------|--------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Maksevormingut enam ei kasutata.                  |
| **Asendatud teise funktsiooniga?** | Jah, ISO 20022 otsedeebeti maksevorming Austria puhul |
| **Mõjutatud moodulid**             | Müügireskontro                                    |

### <a name="edivat-for-belgium"></a>EDIVAT Belgia puhul

EDIVAT on aegunud Belgia standard elektrooniliseks deklareerimiseks turvalise meili teel. Microsoft Dynamics AX 2012 säilitab kirjutuskaitstud lahenduse, et lubada juurdepääsu ajaloolistele andmetele.

|                              |                                      |
|------------------------------|--------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Funktsionaalsust enam ei kasutata. |
| **Asendatud teise funktsiooniga?** | Ei                                   |
| **Mõjutatud moodulid**             | Pearaamat                       |

### <a name="egiro-edifact-cremul-payment-import-format-for-norway"></a>eGiro EDIFACT CREMUL makse impordivorming Norra puhul

eGiro põhineb rahvusvahelisel UN EDIFACT CREMUL-i (Multiple Credit Advice Message) standardil, mida kasutatakse kliendimaksete automaatseks sisestamiseks. Microsoft Dynamics AX-is juurutatakse eGiro kliendimakse impordivorminguna.

|                              |                                                                                           |
|------------------------------|-------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Maksevormingut enam ei kasutata.                                                     |
| **Asendatud teise funktsiooniga?** | Nr Vorming asendatakse tulevastes väljalasetes ISO 20022 väljavõtte impordivormingutega. |
| **Mõjutatud moodulid**             | Müügireskontro                                                                       |

### <a name="external-inventory-for-poland"></a>Väliskaubavaru Poola puhul

Tõend kaupade hankijalt võtmise kohta ilma ostuta müügi puhul. Välislaos käsitletavad kaubad, mis ei mõjuta standardseid varusid, saab müüa ja seejärel automaatselt osta. See protsess loob reaalsed varude teisaldamised.

|                              |                                                 |
|------------------------------|-------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Asendatud teise funktsiooniga                     |
| **Asendatud teise funktsiooniga?** | Jah, sissetuleva veose põhufunktsioon |
| **Mõjutatud moodulid**             | Ostureskontro, laohaldus          |

### <a name="financial-reports-generator-for-eastern-europe"></a>Finantsaruannete generaator Ida-Euroopa puhul

Tööriista kasutatakse andmete kogumise seadistamiseks raamatupidamise ja maksuaruannete jaoks ja andmete XLS- ja DOC-aruande mallidesse eksportimiseks.

|                              |                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Piiratud kasutus                                                                            |
| **Asendatud teise funktsiooniga?** | Nr Tööriist asendatakse tulevastes väljalasetes elektroonilise aruandluse konfiguratsioonidega. |
| **Mõjutatud moodulid**             | Pearaamat                                                                           |

### <a name="import-of-customer-payment-transactions-for-finland"></a>Kliendimakse kannete import Soome puhul

Saate valida Soome maksete puhul impordivormingu, et importida kliendimakse kanded panga esitatud välisfailist.

|                              |                                                                                           |
|------------------------------|-------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Maksevormingut enam ei kasutata.                                                     |
| **Asendatud teise funktsiooniga?** | Nr Vorming asendatakse tulevastes väljalasetes ISO 20022 väljavõtte impordivormingutega. |
| **Mõjutatud moodulid**             | Müügireskontro                                                                       |

### <a name="import-of-payment-transactions-into-a-general-ledger-journal-for-finland"></a>Maksekannete importimine pearaamatu töölehele Soome puhul

Vormingut, mis on spetsiifiline Soomele, kasutatakse raamatupidamiskannete pearaamatusse importimiseks.

|                              |                                                                                           |
|------------------------------|-------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Maksevormingut enam ei kasutata.                                                     |
| **Asendatud teise funktsiooniga?** | Nr Vorming asendatakse tulevastes väljalasetes ISO 20022 väljavõtte impordivormingutega. |
| **Mõjutatud moodulid**             | Müügireskontro                                                                       |

### <a name="integration-with-isabel-synchronized-cis-for-belgium"></a>Integratsioon Isabeliga, sünkroniseeritud (CIS) Belgia jaoks

Isabel on e-panganduse raamistik Euroopas ja de facto standard Belgias.

|                              |                                                                                                                      |
|------------------------------|----------------------------------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Integratsioon Isabeli kliendiga on katkestatud.                                                                |
| **Asendatud teise funktsiooniga?** | Nr Maksevormingu, mida enam ei kasutata, asendatakse Belgia ISO20022 kreeditiülekande maksevorminguga. |
| **Mõjutatud moodulid**             | Ostureskontro                                                                                                     |

### <a name="modifications-in-the-chart-of-accounts-and-accounting-rules-for-spain"></a>Modifikatsioonid kontoplaanis ja raamatupidamisreeglites Hispaania puhul

Seda funktsiooni kasutatakse Hispaani kontoplaanides ja raamatupidamisreeglites muudatuste tegemiseks. See vastendab kontod, et aidata teisendada vanu kontoplaane uuteks kontoplaanideks, ja võrdleb eelnevat finantsaastat uue finantsaastaga, isegi kui need sisestati erinevatele kontonumbritele.

|                              |                |
|------------------------------|----------------|
| **Kasutuselt eemaldamise põhjus**       | Piiratud kasutus  |
| **Asendatud teise funktsiooniga?** | Ei             |
| **Mõjutatud moodulid**             | Pearaamat |

### <a name="pagamento-fornittori-vendor-payment-format"></a>Pagamento Fornittori hankijamakse vorming

Itaalia pärandi maksevorming kreeditülekannetele.

|                              |                                                        |
|------------------------------|--------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Maksevormingut enam ei kasutata.                  |
| **Asendatud teise funktsiooniga?** | Jah, ISO20022 kreeditiülekande maksevorming Itaalia puhul |
| **Mõjutatud moodulid**             | Ostureskontro                                       |

### <a name="payment-export-formats-for-estonia"></a>Makse ekspordivorming Eesti puhul

Telehansa ja Teleservice'i vorminguid kasutatakse pangamakse ekspordi jaoks.

|                              |                                                          |
|------------------------------|----------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**      | Maksevorminguid enam ei kasutata.                  |
| **Asendatud teise funktsiooniga?** | Jah, ISO20022 kreeditiülekande maksevorming Eesti puhul |
| **Mõjutatud moodulid**             | Ostureskontro                                         |

### <a name="payment-file-archive-for-norway"></a>Maksefaili arhiiv Norra puhul

Maksefailide loomisel arhiivib failiarhiiv automaatselt kõik loodavad failid, isegi varasemalt kirjutatud või loetud failid.

|                              |                                                                    |
|------------------------------|--------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Asendatud teise funktsiooniga                                        |
| **Asendatud teise funktsiooniga?** | Jah, elektroonilise aruandluse arhiivitud tööd                            |
| **Mõjutatud moodulid**             | Ostureskontro, müügireskontro, organisatsioonihaldus |

### <a name="payment-import-formats-for-estonia"></a>Makse impordivorming Eesti puhul

Telehansa ja TeleTeenuse vorminguid kasutatakse pangamakse ekspordi jaoks.

|                              |                                                                                            |
|------------------------------|--------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Maksevorminguid enam ei kasutata.                                                    |
| **Asendatud teise funktsiooniga?** | Nr Vormingud asendatakse tulevastes väljalasetes ISO 20022 väljavõtte impordivormingutega. |
| **Mõjutatud moodulid**             | Müügireskontro                                                                        |

### <a name="performance-management-goal-workflow"></a>Jõudlushalduse eesmärgi töövoog

Jõudlushaldus hõlmab eesmärgihaldust ja integreerimist jõudluse ülevaadetega.

|                              |                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Jõudlushaldus kujundati ümber ja eesmärgi lehtede arvu vähendati, et protsessi lihtsustada.                 |
| **Asendatud teise funktsiooniga?** | Nr Eesmärgid on nähtavad juhtidele juhi iseteeninduse portaali kaudu ja neid saab muuta ja vaadata vastav juht. |
| **Mõjutatud moodulid**             | Inimkapitali juhtimine                                                                                                 |

### <a name="postgirot-and-postgirot-utland-payment-formats-for-sweden"></a>Postgiroti ja Postgirot Utlandi maksevormingud Rootsi puhul

Postgiroti ja Postgirot Utlandi maksevormingud Rootsi puhul.

|                              |                                                         |
|------------------------------|---------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Maksevorminguid enam ei kasutata.                 |
| **Asendatud teise funktsiooniga?** | Jah, ISO20022 kreeditiülekande maksevorming Rootsi puhul |
| **Mõjutatud moodulid**             | Ostureskontro                                        |

### <a name="radio-frequency-identifier"></a>Raadiosageduse identifikaator

Raadioidentimine (RFID) on andmete kogumise tehnoloogia, mis kasutab identimisteabe talletamiseks elektroonilisi silte ja selle teabe hankimiseks otsenähtavuse olemasolu mitte eeldavat lugemisseadet.

|                              |                                               |
|------------------------------|-----------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Vähene kasutamine klientide seas ja piiratud funktsioonide kogum. |
| **Asendatud teise funktsiooniga?** | Ei                                            |
| **Mõjutatud moodulid**             | Varud                          |

### <a name="report-about-state-invoices-numbering-for-latvia"></a>Aruanne riigi arvete nummerdamise kohta Läti puhul

Läti seadusandlus annab teatud reeglid müügiarvete nummerdamise kohta. Funktsioon võimaldab müügiarvetele kasutaja või kasutajagrupi põhjal spetsiifilised numbrid määrata. Seejärel saate luua aruande või XML-faili. Samuti saate printida aruande kasutatavate arvenumbrite kohta.

|                              |                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Riiklike arvete nummerdamist ei pea enam säilitama. Aruanne kasutatud arvenumbrite kohta ei ole enam vajalik. |
| **Asendatud teise funktsiooniga?** | Ei                                                                                                                       |
| **Mõjutatud moodulid**             | Müügireskontro                                                                                                      |

### <a name="set-up-the-names-of-the-manager-and-general-accountant-of-a-company-for-lithuania"></a>Ettevõtte juhi ja pearaamatupidaja nimede seadistamine Leedu puhul

Ettevõtte juhi ja pearaamatupidaja nimed saab määrata ettevõtte teabes ja kasutada erinevates kohaliku aruande väljaprintides.

|                              |                                                                 |
|------------------------------|-----------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Asendatud teise funktsiooniga                                     |
| **Asendatud teise funktsiooniga?** | Jah, ametnike seadistamist saab kasutada samal otstarbel.   |
| **Mõjutatud moodulid**             | Ostureskontro, Müügireskontro, Sularaha- ja pangahaldus |

### <a name="telepay-payment-formats-for-norway"></a>Telepay maksevormingud Norra puhul

TelePay maksevormingud hõlmavad hankijamakse eksporti (kreeditiülekanne) ja kliendimakse kogumist (otsedeebet).

|                              |                                                                                                |
|------------------------------|------------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Maksevorminguid enam ei kasutata.                                                        |
| **Asendatud teise funktsiooniga?** | Jah, ISO20022 kreeditiülekande maksevorming ja AvtaleGiro kliendimakse vorming Norra puhul |
| **Mõjutatud moodulid**            | Müügireskontro, ostureskontro                                                          |

### <a name="vendor-payment-export-formats-for-finland"></a>Hankijamakse ekspordivormingud Soome puhul

Soome puhul on maksete eksportimiseks saadaval kaks vormingut. LM02 (FI) kasutatakse riigisisesteks makseteks ja LUM2 (FI) kasutatakse välismakseteks.

|                              |                                                          |
|------------------------------|----------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Maksevorminguid enam ei kasutata.                  |
| **Asendatud teise funktsiooniga?** | Jah, ISO20022 kreeditiülekande maksevorming Soome puhul |
| **Mõjutatud moodulid**            | Ostureskontro                                         |

### <a name="workflow-for-creating-goals"></a>Töövoog eesmärkide loomiseks

Töövoog töötaja eesmärkide loomise haldamiseks on üks mitmest töövoost, mis on saadaval, et aidata koordineerida jõudlushalduse protsessi.

|                              |                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Jõudlushaldus on rakenduses Microsoft Dynamics 365 for Finance and Operations täielikult ümber kujundatud.                                                                                                                                                                                                                                        |
| **Asendatud teise funktsiooniga?** | Ümberkujundatud jõudlushalduse funktsioon annab rohkem kontrolli eesmärkide sisu, progressi jälgimiseks kasutatavate mõõtmiste ja lisadokumentide manustamise üle. Eesmärke saab salvestada mallidena ja seejärel taaskasutada. See funktsioon saab aidata teil kiiremini oma töötajate jaoks täiendavaid eesmärke seadistada. |
| **Mõjutatud moodulid**            | Inimkapitali juhtimine                                                                                                                                                                                                                                                                                                               |

## <a name="features-that-have-been-deprecated-in-dynamics-ax-70-releases"></a>Dynamics AX 7.0 väljaannete aegunud funktsioonid

### <a name="ability-to-cancel-changes-to-a-vendor-invoice"></a>Võimalus hankijaarve muudatusi tühistada

|                              |                         |
|------------------------------|-------------------------|
| **Kasutuselt eemaldamise põhjus**       | Toimivuse täiustamine |
| **Asendatud teise funktsiooniga?** | Ei                      |
| **Mõjutatud moodulid**            | Ostureskontro        |

### <a name="aif-axd-and-axbc-integrations"></a>AIF, AxD ja AxBC integratsioonid

Rakenduste integreerimise raamistikus (AIF) saab vahetada andmeid välissüsteemidega äriloogika kaudu, mis on näidatud teenustena. Dynamics AX sisaldab teenuseid, mis põhinevad dokumentidel ja .NET Business Connectoril (AxBC). Dokument luuakse XML-i abil. XML sisaldab päiseteavet, mis lisatakse *sõnumi* loomiseks, mille saab Dynamics AX-i või sealt välja saata. Dokumentide näites on müügitellimused ja ostutellimused. Kuid peaaegu igasugune üksus (nt klient) võib olla kajastatud dokumendiga. Dokumentidel põhinevad teenused kasutavad klasse **Axd &lt;*Dokument*&gt;**.

|                              |                                                                                                                                                                                                          |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | AIF-i ja AxDs-i arhitektuuri ei saanud pilveteenusesse skaleerida. Hulgiimpordiga oli seotud jõudlusprobleeme.                                                                               |
| **Asendatud teise funktsiooniga?** | Dynamics AX-i praeguses versioonis on see funktsioon asendatud andmete importimise/eksportimise raamistikuga, mis toetab korduvat hulgiimportimist/eksportimist. AxBC puhul soovitame kasutada tegelikke tabeleid. |
| **Mõjutatud moodulid**             | AxDs, AxBCs ja AIF                                                                                                                                                                                     |

### <a name="boms-without-bom-versions"></a>Kooslused ilma koosluse versioonideta

Kui konfiguratsioonivõti **Koosluse versioonid** keelati, peideti koosluse versioonid kõigil vormidel ja süsteem sundis väljastatud toodete ja koosluste vahele 1:1 seose. Praeguses Dynamics AX-i versioonis ei saa konfiguratsioonivõtit **Koosluse versioonid** keelata.

|                              |                                                                                         |
|------------------------------|-----------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**      | Konfiguratsioonivõtme kasutamist koosluse versioonide juhtimiseks ei saa pilvekeskkonnas skaleerida. |
| **Asendatud teise funktsiooniga?** | Ei                                                                                      |
| **Mõjutatud moodulid**            | Tooteteabe haldus, Laohaldus                                    |

### <a name="brazilian-bordero"></a>Brasiilia Bordero

Spetsiifiline maksemeetod Braziilia ettevõtetele

|                              |                                                                                                       |
|------------------------------|-------------------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Tugi Brasiilia Bordero maksemeetodile on katkestatud Brasiilia lokalisatsioonist |
| **Asendatud teise funktsiooniga?** | Ei                                                                                                    |
| **Mõjutatud moodulid**             | Ostureskontro                                                                                      |

### <a name="brazilian-sintegra-statement"></a>Brasiilia Sintegra avaldus

Föderaalmaksu avaldus ICMS maksule

|                              |                                                                                                                       |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | See avaldus ei ole enam kohaldatav mõnedes Brasiilia osariikides.                                                     |
| **Asendatud teise funktsiooniga?** | Nr Kasutajad saavad kasutada üldist elektroonilist aruandlustööriista, et konfigureerida avaldust vastavalt konkreetsele olukorrale. |
| **Mõjutatud moodulid**             | Finantsraamatud                                                                                                          |

### <a name="brazilian-scan-contingency-mode-for-nf-e"></a>Brasiilia SCAN-i ettenägematute kulude režiim NF-e puhul

(SCAN) ettenägematute kulude keskkonda kasutatakse Nota Fiscal eletrônica (NF-e) oleku loomiseks, eksportimiseks ja importimiseks, kui Secretaria da Fazenda (SEFAZ) keskkond ei ole saadaval.

|                              |                                                                             |
|------------------------------|-----------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | See ettenägematute kulude meetod ei ole enam kohaldatav kõikides Brasiilia osariikides |
| **Asendatud teise funktsiooniga?** | Ei                                                                          |
| **Mõjutatud moodulid**             | Müügireskontro                                                         |

### <a name="business-analyzer"></a>Majandusanalüüs

See mobiilirakendus võimaldab kasutajatel ettevõtte võtmemõõdikuid üle vaadata.

|                              |                                                                                                                                                               |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | See funktsioon on asendatud teise funktsiooniga.                                                                                                      |
| **Asendatud teise funktsiooniga?** | Microsoft Power BI sisupakett Finantsnäitajate jälgimine sisaldab rahalisi võtmemõõdikuid, mis olid varem saadaval Business Analyzeris. |
| **Mõjutatud moodulid**             | Pearaamat                                                                                                                                                |

### <a name="business-statistics"></a>Äristatistika

Äristatistika päringute seadistamine, mis aitavad analüüsida organisatsiooni jõudlust

|                              |                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Vananenud lähenemine äriteabele, vähene kasutamine ja piiratud funktsioonide kogum |
| **Asendatud teise funktsiooniga?** | Uued äriteabe lahendused praegusele Dynamics AX-i versioonile                                      |
| **Mõjutatud moodulid**             | Hanked, Ostureskontro, Müük ja turundus, Müügireskontro         |

### <a name="change-document-date-function-in-invoice-approval-journal"></a>Dokumendi kuupäeva muutmise funktsioon arve kinnitamise töölehel

|                              |                                                                         |
|------------------------------|-------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Vähene kasutus                                                               |
| **Asendatud teise funktsiooniga?** | Jah. Sisestatud hankija kande dokumendi kuupäeva saab muuta. |
| **Mõjutatud moodulid**             | Ostureskontro                                                        |

### <a name="clieop03-payment-format-for-the-netherlands"></a>Hollandi maksevorming ClieOp03

|                              |                                                                                                            |
|------------------------------|------------------------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | See vorming ei kehti enam Hollandis, kuna see on asendatud SEPA funktsiooniga. |
| **Asendatud teise funktsiooniga?** | SEPA maksete eksport                                                                                       |
| **Mõjutatud moodulid**             | Kõik                                                                                                        |

### <a name="compliance-center"></a>Vastavuskeskus

Vastavuskeskus oli ettevõtteportaali sait dokumentide nõuete haldamiseks Sarbanes-Oxley seadusega seotud vastavusalgatuste puhul.

|                              |                                                                                                                        |
|------------------------------|------------------------------------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Kliendid ei kasuta. Microsoft SharePoint sisaldab sama võimalust, mis oli saadaval vastavuskeskuses. |
| **Asendatud teise funktsiooniga?** | Ei                                                                                                                     |
| **Mõjutatud moodulid**             | Vastavuse ja sisekontrollid                                                                                       |

### <a name="connector-for-microsoft-dynamics"></a>Microsoft Dynamicsi konnektor

Seda tööriista kasutati võtmeandmete integreerimiseks Microsoft Dynamics CRM-ist Microsoft Dynamics ERP rakendustesse.

|                              |                                                          |
|------------------------------|----------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | See funktsioon on asendatud teise funktsiooniga. |
| **Asendatud teise funktsiooniga?** | Dynamics Integrator                                      |
| **Mõjutatud moodulid**             | Microsoft Dynamicsi konnektor                         |

### <a name="container-unit-and-multi-dimension-on-hand"></a>Konteineriüksus ja mitmedimensiooniline laoseis

|                              |                                                                                                                                                                 |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Topeltfunktsioon                                                                                                                                         |
| **Asendatud teise funktsiooniga?** | Jah. Alates versioonist AX 2012 on see funktsioon asendatud konsolideeritud partii tellimuste funktsioonide kogumiga. See funktsioon sisaldab konsolideeritud laoseisu vaadet. |
| **Mõjutatud moodulid**             | Tooteteabe haldus, Tootmise juhtimine, Varude haldus, Müük ja turundus                                                                   |

### <a name="cue-group-metadata"></a>Vihjegrupi metaandmed

|                              |                                                                                                                                                                                                                               |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Vihjegruppe kasutati kiirinfo alal ühe või mitme vihje kuvamiseks. Selle kasutamine oli piiratud ja oli ka jõudlusprobleeme, kuna kirje muutmine põhivormil põhjustas vihjegrupis ühe päringu vihje kohta. |
| **Asendatud teise funktsiooniga?** | Ei                                                                                                                                                                                                                            |
| **Mõjutatud moodulid**             | Kõik                                                                                                                                                                                                                           |

### <a name="cue-metadata"></a>Vihje metaandmed

|                              |                                                                                                                                                                                                                                         |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Vihje metaandmed olid piiratud arvu või summa teabega.                                                                                                                                                                                   |
| **Asendatud teise funktsiooniga?** | Modelleerimisel paindlikkuse lisamiseks võeti kasutusele paani metaandmed. Näiteks saate modelleerida praegusi arve, navigeerimist ja tulemuslikkuse võtmenäitajaid (KPI-sid). Arvu paani metaandmed on vihje metaandmete otsene asendus. |
| **Mõjutatud moodulid**             | Kõik                                                                                                                                                                                                                                     |

### <a name="danish-check-format"></a>Taani tšekivorming

|                              |                                                                                                                         |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Taani tšekikavandi vormingu tugi on lõpetatud ja aruanne on DK lokaliseerimisest eemaldatud. |
| **Asendatud teise funktsiooniga?** | Ei                                                                                                                      |
| **Mõjutatud moodulid**             | Kõik                                                                                                                     |

### <a name="data-partitions"></a>Andmesektsioonid

Andmesektsioonid tagavad andmete loogilise eraldamise Microsoft Dynamics AX-i andmebaasis.

|   |   |
|---|---|
| **Kasutuselt eemaldamise põhjus**       | Microsoft Dynamics AX 2012 R2-s võeti andmete eraldamise võimaldamiseks kasutusele andmesektsioonid. Tavastsenaariumi puhul on ettevõttel tütarettevõtted ja ühe tütarettevõtte andmed ei tohiks olla teisele tütarettevõttele näha, kuigi mõlemaid tütarettevõtteid haldab sama IT-osakond. Kuid uute sektsioonide loomiseks ja nende täitmiseks andmetega ning sektsiooni andmete varundamiseks oli vaja kogu programmis lisaskripte ja halduse üldkulusid. Pilves, kus meil on juurdepääs platvormi teenusena (PaaS) andmebaasiteenustele (Microsoft Azure SQL-i andmebaas) on palju tõhusam kasutada andmebaasi eralduskonteinerina, kui teha eraldamine programmis. Olenemata sellest, kas andmete eraldamine on vajalik tütarettevõtetele, mitmele rentnikule või lihtsalt skaalale, usume, et neid stsenaariume saab käsitleda paremini mitme andmebaasi või mitme Dynamics AX-i eksemplari kaudu. |
| **Asendatud teise funktsiooniga?** | Tulevases väljaandes asendatakse andmesektsioonid mitme andmebaasi või Dynamics AX-i eksemplari toe kaudu.    |
| **Mõjutatud moodulid**             | Kõik  |

### <a name="database-and-file-share-storage-for-attachments"></a>Andmebaas ja ühine failiketas manuste jaoks
Microsoft Dynamics AX 2012 lubas manuste talletamist andmebaasis ja failiketastel. Kumbagi neist valikutest enam ei toetata.

|                              |                                        |
|------------------------------|----------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Ühist failiketast enam ei toetata, kuna pilve majutatud keskkonnad ei saa kohalike failiketastega suhelda. Andmebaasi talletamine on Azure’i bloobimälu kasuks taunitud. Azure’i bloobimälu on andmebaasis talletamisega samaväärne, kuna dokumentidele pääseb juurde ainult rakenduse Dynamics 365 for Finance and Operations kliendivormide kaudu. See pakub lisaeelist talletusruumi pakkumisel, mis ei mõjuta negatiivselt andmebaasi jõudlust. Bloobimälu on dokumendihalduse vaiketalletusmehhanism ja toimib viivitamatult. |
| **Asendatud teise funktsiooniga?** | Andmebaasi talletamine on Azure’i bloobimälu kasuks taunitud.       |
| **Mõjutatud moodulid**             | Kõik                   |

### <a name="delimitation"></a>Eraldamine

|                              |                                        |
|------------------------------|----------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Funktsiooni ei leidnud kasutamist. |
| **Asendatud teise funktsiooniga?** | Ei                                     |
| **Mõjutatud moodulid**             | Kellaaeg ja kohalolek                    |

### <a name="desktop-client"></a>Töölauaklient

|                              |                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Dynamics AX-i kliendikogemus on ümber kujundatud, et parandada kasutatavust mitme platvormi ja seadme lõikes.                      |
| **Asendatud teise funktsiooniga?** | Uus veebiklient põhineb töölauavormi metaandmetel ja programmeerimismudelil, mida on muudetud rikkaliku veebiplatvormi pakkumiseks. |
| **Mõjutatud moodulid**             | Kõik                                                                                                                                    |

### <a name="direct-database-connection"></a>Andmebaasi otseühendus

Dynamics AX 2012 R3-s sai tänapäevane jaemüügikassa luua kanaliandmebaasiga otse ühenduse samamoodi, nagu ettevõtte kassaga. See täiendas jaemüügikassa standardset sidepidamisviisi jaemüügiserveri kaudu.  

|                              |                                                                                         |
|------------------------------|-----------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Andmebaasi otseühenduvus nõudis madalamaid turbeprotokolle ja seda kasutati peamiselt kõrgeima jõudluse saavutamiseks. Finance and Operationsi jõudlus- ja turbetäiustuste tõttu põhjustab see funktsioon nüüd rohkem probleeme kui lahendab. |
| **Asendatud teise funktsiooniga?** | Nr Nüüd toetatakse ainult standardset jaemüügiserveri sidet.    |
| **Mõjutatud moodulid**             | Kanali andmebaas / tänapäevane jaemüügikassa                                    |

### <a name="dutch-swift-mt940"></a>Hollandi SWIFT MT940

|                              |                                                                                                                                                                                                                                       |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Lokaliseeritud funktsiooni asemel kasutatakse nüüd üldist funktsiooni.                                                                                                                                                                 |
| **Asendatud teise funktsiooniga?** | Jah, see funktsioon on asendatud pangakonto täpsema vastavusseviimise funktsiooniga. |
| **Mõjutatud moodulid**             | Kõik                                                                                                                                                                                                                                   |

### <a name="ebilanz-xbrl-for-germany"></a>eBilanz (Saksamaal XBRL)

See funktsioon andis keele eXtensible Business Reporting Language (XBRL) väljundi, mis on mõeldud spetsiaalselt Saksamaa rakenduse eBilanz taksonoomia jaoks.

|                              |                                                                                                                                                                        |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Kliendid ei kasuta                                                                                                                                                 |
| **Asendatud teise funktsiooniga?** | Seda funktsiooni pole asendatud teise funktsiooniga, kuid Saksamaa turul on saadaval mitu spetsiaalset XBRL-i paketti, mis pakuvad rikkalikult XBRL-i funktsioone. |
| **Mõjutatud moodulid**             | Management Reporter                                                                                                                                                    |

### <a name="enterprise-portal-client"></a>Ettevõtteportaali klient

|                              |                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Pakutakse ühe kliendi platvormi.                                                                                            |
| **Asendatud teise funktsiooniga?** | Uus veebiklient põhineb töölauavormi metaandmetel ja programmeerimismudelil, mida on muudetud rikkaliku veebiplatvormi pakkumiseks. |
| **Mõjutatud moodulid**             | Kõik                                                                                                                                    |

### <a name="environmental-sustainability"></a>Keskkonna jätkusuutlikkus

|                              |                                                    |
|------------------------------|----------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Vähene kasutamine klientide seas ja piiratud funktsioonide kogum       |
| **Asendatud teise funktsiooniga?** | Ei                                                 |
| **Mõjutatud moodulid**             | Vastavus ja sisekontroll, Ostureskontro |

### <a name="form-activex-and-managed-host-controls"></a>Vormi ActiveX ja Hallatud host juhtelemendid

|                              |                                                                                                                                                                                               |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | ActiveX-i ja hallatud hosti juhtelemendid põhinevad kasutuselt eemaldatud töölauakliendil.                                                                                                             |
| **Asendatud teise funktsiooniga?** | Laiendatav juhtimisraamistik toetab uusi HTML-il, CSS-il ja JavaScriptil põhinevaid uusi juhtelemente ja on Microsoft Visual Studio tööriistakeskkonnas esmaklassiline juhtelement. |
| **Mõjutatud moodulid**             | Kõik                                                                                                                                                                                           |

### <a name="generate-prenotes-by-using-a-batch"></a>Eelpäringute loomine partii abil

Eelpäringu loomine pole partii abil võimalik, kuid kasutaja saab seda siiski teha.

|                              |                                                                                                        |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Saadud eelpäringu faili säilitamiseks ja kuvamiseks partii abil loomisel pole ühtegi vormi. |
| **Asendatud teise funktsiooniga?** | Eelpäringuid saab siiski koostada ja kasutaja saab määrata faili salvestamise kohta.   |
| **Mõjutatud moodulid**             | Ostureskontro, Müügireskontro, Sularaha- ja pangahaldus                                        |

### <a name="german-dtaus-payment-export-and-account-statement-import-totals-and-transactions"></a>Saksa DTAUS-makse eksportimine ja konto väljavõtte importimine (kogusummad ja kanded)

|                              |                                                                                                                                                                                                                                                                                                |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | See vorming ei kehti enam Saksamaal, kuna see on asendatud ühtse euromaksete piirkonna (SEPA) funktsiooniga.                                                                                                                                                                 |
| **Asendatud teise funktsiooniga?** | Jah, selle funktsiooni on asendanud SEPA maksete eksportimine ja täiustatud panga vastavusseviimise funktsioon kontoväljavõtete importimiseks. |
| **Mõjutatud moodulid**             | Kõik                                                                                                                                                                                                                                                                                            |

### <a name="german-dtazv-payment-format"></a>Saksamaa DTAZV maksevorming

|                              |                                                                                                    |
|------------------------------|----------------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | See vorming ei kehti enam Saksamaal, kuna see on asendatud SEPA funktsiooniga. |
| **Asendatud teise funktsiooniga?** | SEPA maksete eksport                                                                               |
| **Mõjutatud moodulid**             | Kõik                                                                                                |

### <a name="german-mt940-import"></a>Saksa MT940 importimine

|                              |                                                                                                                                                                                                                                       |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Lokaliseeritud funktsiooni asemel kasutatakse nüüd üldist funktsiooni.                                                                                                                                                                 |
| **Asendatud teise funktsiooniga?** | Jah, see funktsioon on asendatud pangakonto täpsema vastavusseviimise funktsiooniga. |
| **Mõjutatud moodulid**             | Kõik                                                                                                                                                                                                                                   |

### <a name="german-xml-eu-sales-list"></a>Saksamaa XML EL-i käibearuanne

|                              |                                                                                                                                                                                    |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Saksa EL-i müügiloendi aruandluses XML-vormingut enam ei toetata. Saksa maksuametile EL-i müügiloendi aruande edastamiseks saab kasutada ainult ELMA5 tekstifaili vormingut. |
| **Asendatud teise funktsiooniga?** | Ei                                                                                                                                                                                 |
| **Mõjutatud moodulid**             | Maks                                                                                                                                                                                |

### <a name="gl-ssrs-reports"></a>GL SSRS-i aruanded

Järgmisi menüüelemente sisaldavad aruanded on eemaldatud. **Proovibilansi kokkuvõte**, **Üksikasjalik proovibilanss**, **Kontoplaan**, **Auditijälg**, **Saldod** ja **Saldoloend**.

|                              |                                                                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Rahalised Microsoft SQL Serveri teenuse Reporting Services (SSRS) aruanded on asendatud Management Reporteri võimaluste ja vaikearuannetega. |
| **Asendatud teise funktsiooniga?** | Management Reporter (selles Dynamics AX-i versioonis nimega **Finantsaruandlus**)                                                  |
| **Mõjutatud moodulid**            | Pearaamat                                                                                                                               |

### <a name="infopart-and-formpart-metadata"></a>Parameetrite InfoPart ja FormPart metaandmed

|                              |                                                                                                                                                                                                                                |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Parameetrite InfoPart ja FormPart metaandmed lubasid kahe kliendi kiirinfo loomise.                                                                                                                                    |
| **Asendatud teise funktsiooniga?** | Parameetri InfoPart metaandmed, mis oli lihtsustatud vormidefinitsioon, on versioonitäienduse tööriistadega vormiks teisendatud. Parameetri FormPart metaandmed, mis viitasid vormile, on asendatud otsesema viitega, mis on loodud versioonitäienduse tööriistadega. |
| **Mõjutatud moodulid**             | Kõik                                                                                                                                                                                                                            |

### <a name="main-account-list-page"></a>Põhikonto loendileht

Juriidilise isiku kontode loend ja seotud saldoteave

|                              |                                                                                                                                                                                    |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Saldoteave on saadaval loendilehel **Proovibilanss** kontode ja dimensioonide kaupa.                                                                                      |
| **Asendatud teise funktsiooniga?** | Leht **Põhikontod** sisaldab sama kontoloendit, mis loendileht **Põhikonto**. Ruudustikuvaade lehel **Põhikontod** näitab ka veelgi väiksemat ruudustikulaadset vaadet. |
| **Mõjutatud moodulid**             | Pearaamat                                                                                                                                                                     |

### <a name="malaysia-and-singapore-bank-cash-flow-report"></a>Malaisia ja Singapuri panga rahavooaruanne

See funktsioon võimaldab kasutajal printida rahavoo aruande, mis näitab valitud pangakontode sularaha sissetuleku ja väljamineku kandeid ja üksikasju konkreetse kuupäevavahemiku jooksul.

|                              |                                                                         |
|------------------------------|-------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Sama teavet saab pangakande päringu kaudu. |
| **Asendatud teise funktsiooniga?** | Pangakande päring                                            |
| **Mõjutatud moodulid**             | Sularaha- ja pangahaldus                                                |

### <a name="mexican-cfd-electronic-invoice"></a>Mehhiko CFD elektrooniline arve

See funktsioon lubas Mehhiko elektrooniliste arvete loomise, kasutades meetodit Comprobante Fiscal Digital (CFD), kus ettevõte allkirjastab arve, küsides valitsuselt vajalikku kinnitust. See funktsioon pakub ka igakuist aruannet, mis sisaldab kõiki perioodi jooksul väljastatud elektroonilisi arveid.

|                              |                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Seda meetodit ei rakendata enam. Maksuasutused eemaldasid kasutuselt elektrooniliste arvete koostamise meetodiga CFD ja asendasid selle meetodiga Comprobante Fiscal Digital a través de Internet (CFDI), kus allkirjastamine on delegeeritud muust osapoolest teenusepakkujale (PAC). Igakuine aruanne on eemaldatud ja päringu valik võimaldab kasutajatel varasemate kannete kohta päringuid esitada. |
| **Asendatud teise funktsiooniga?** | Ei                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Mõjutatud moodulid**             | Konto võlgnevused, Projekt                                                                                                                                                                                                                                                                                                                                                                              |

### <a name="mexico-realized-and-unrealized-vat"></a>Mehhiko realiseeritud ja realiseerimata käibemaks

Microsoft Dynamics AX 2012 haldas realiseerimata käibemaksu (KM), kasutades Mehhikos kehtivaid realiseerimata maksu funktsioone.

|                              |                                                                                                                     |
|------------------------------|---------------------------------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Topeltfunktsioon                                                                                             |
| **Asendatud teise funktsiooniga?** | Jah, see funktsioon on asendatud standardse tingimusliku käibemaksu tuumfunktsiooniga. |
| **Mõjutatud moodulid**             | Maks                                                                                                                 |

### <a name="microsoft-outlook-integration"></a>Microsoft Outlooki integratsioon

|                              |                                                                                |
|------------------------------|--------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | See funktsioon on asendatud Microsoft Exchange Serveri integratsiooniga. |
| **Asendatud teise funktsiooniga?** | Jah                                                                            |
| **Mõjutatud moodulid**             | Müük ja turundus                                                            |

### <a name="payroll-information-in-human-resources"></a>Palgateave inimressursside moodulis

Inimressursside palgateave

|                              |                                                                                                                                                                                                                                                                                                                              |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | See funktsioon on asendatud tuumlehtedega Palk ja Inimressurssid.                                                                                                                                                                                                                                              |
| **Asendatud teise funktsiooniga?** | **Soodustused**, **Tulud** ja muud seotud lehed, mis olid varem moodulis USA palk olemas, on nüüd ümber konfigureeritud ja kuuluvad inimressursside tuumkonfiguratsiooni, et aidata toetada välist palga töötlemist. Sellele funktsioonile pääseb juurde konfiguratsioonivõtmega **Inimressursid 1** &gt; **Palk**. |
| **Mõjutatud moodulid**             | Inimressursid, Palk                                                                                                                                                                                                                                                                                                     |

### <a name="private-blocking-of-inventory-and-warehouse-management-journals"></a>Varude ja laohalduse töölehtede privaatne blokeerimine

Varude ja laohalduse töölehed ei toeta enam võimalust märkida tööleht valitud kasutaja puhul privaatseks. Töölehtede privaatsena blokeerimise protsessi toetatakse ainult kasutajagruppide puhul ja redigeerimise ajal.

|                              |                                        |
|------------------------------|----------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Funktsiooni ei leidnud kasutamist. |
| **Asendatud teise funktsiooniga?** | Ei                                     |
| **Mõjutatud moodulid**             | Varude haldus                   |

### <a name="product-builder"></a>Tootekonstruktor

Tootekonstruktorit kasutati müügitellimuse, ostutellimuse, tootmistellimuse, müügipakkumise, projektipakkumise või kaubavajaduse üksuste dünaamiliseks konfigureerimiseks. Modelleerimise muutujatega tootemudeli põhjal sai kasutaja valida väärtusi kliendi nõudmiste täitmiseks ja kordumatu tootevariandi saamiseks, millel oli kooslus ja protsess.

|                              |                                                                                                                                                                                                         |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Tootekonstruktor avaldas X++ koodi lõppkasutajatele ja Dynamics AX-i praeguses versioonis seda ei toetata. See on eemaldatud kattuvate suurte koodibaaside haldamisel dubleerimise vältimiseks. |
| **Asendatud teise funktsiooniga?** | Toote konfiguratsioon                                                                                                                                                                                   |
| **Mõjutatud moodulid**             | Tooteteabe haldus, Müük ja turundus                                                                                                                                                     |

### <a name="rename-product-dimension"></a>Nimetage tootedimensioon ümber.

Selle funktsiooni abil saate määrata ühe toote standarddimensiooni (suuruse, värvi või stiili) nimeks teie ärivajadustele paremini vastava nime. Ümbernimetamine hõlmas kõiki silte, millel tootedimensiooni nime kasutati.

|                              |                                                                               |
|------------------------------|-------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Dynamics AX-i praegune versioon ei toeta käitusajal siltide muutmist. |
| **Asendatud teise funktsiooniga?** | Ei                                                                            |
| **Mõjutatud moodulid**             | Tooteteabe haldus                                                |

### <a name="retail-server-connectivity-using-http"></a>Jaemüügiserveri ühenduvus HTTP abil

Dynamics AX 2012 R3-s toimis jaemüügiserveri funktsioon HTTP-sidet (mitteturvalist) kasutades. See täiendas standardset sidet HTTP-si kaudu.

|                              |                                                                               |
|------------------------------|-------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Uute turbenõuete tõttu toetatakse nüüd ainult turvalist sidet, kasutades TLS 1.2 (või uuemat, kui on saadaval). Iseteeninduslik installiprogramm konfigureerib arvuti selle side jaoks automaatselt. |
| **Asendatud teise funktsiooniga?** | Nr Nüüd toetatakse ainult standardset HTTP-sidet.                                                                           |
| **Mõjutatud moodulid**             | Jaemüügiserver                                                |

### <a name="role-center-pages"></a>Rollikeskuse leheküljed

|                              |                                                                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Rollikeskuse lehed loodi kasutuselt eemaldatud ettevõtteportaali platvormile, mis on Dynamics AX-i praeguses versioonis asendatud uue veebikliendi platvormiga. |
| **Asendatud teise funktsiooniga?** | Uus tööruumi vormi struktuur pakub kasutajatele protsessikeskset kujundust, mis annab sageli kasutatavatele toimingutele hõlpsa juurdepääsu.                       |
| **Mõjutatud moodulid**             | Kõik                                                                                                                                                                      |

### <a name="sales-tax-jurisdictions"></a>Käibemaksu jurisdiktsioonid

|                              |                                              |
|------------------------------|----------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Vähene kasutamine klientide seas ja piiratud funktsioonide kogum |
| **Asendatud teise funktsiooniga?** | Ei                                           |
| **Mõjutatud moodulid**             | USA käibemaks                                 |

### <a name="shipping-carrier-interface"></a>Kättetoimetaja liides

|                              |                                                                                                                                                 |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Topeltfunktsioon                                                                                                                         |
| **Asendatud teise funktsiooniga?** | Jah, see funktsioon on osaliselt asendatud transpordihaldusega, kuid ei ole veel asendatud põhilise laohaldusega (WMS I). |
| **Mõjutatud moodulid**             | Müük ja turundus, varude haldus                                                                                                       |

### <a name="sites-services"></a>Sites Services

Sites Services võimaldab luua veebisaite, mis laiendavad äriprotsessid Internetti ilma IT-toeta.

|                              |                                                                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Dynamics AX-i kasutataval Microsoft Azure'i taristul on uusi funktsioone, mida saab selle asemel kasutada (näiteks Azure'i saidid). |
| **Asendatud teise funktsiooniga?** | Ei                                                                                                                                       |
| **Mõjutatud moodulid**             | Inimressursside värbamine, juhtumihaldus, pakkumiskutsed, hankija registreerimine                                                                  |

### <a name="ssas-demand-forecasting-strategy"></a>SSAS-i nõudluse prognoosi strateegia

|                              |                                                                              |
|------------------------------|------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Uues pilvarhitektuuris ei toetata selle funktsiooni kujundust. |
| **Asendatud teise funktsiooniga?** | Teenuse Azure Machine Learning nõudluse prognoosi strateegia                           |
| **Mõjutatud moodulid**             | Planeerimine                                                                     |

### <a name="travel-requisitions"></a>Reisiplaanid

|                              |                                                                 |
|------------------------------|-----------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Vähene kasutamine ja enamik funktsioone oli ettevõtteportaalis olemas. |
| **Asendatud teise funktsiooniga?** | Ei                                                              |
| **Mõjutatud moodulid**             | Kulude haldus                                              |

### <a name="vendor-invoice-pool-excluding-posting-details"></a>Hankija arve kaust ilma sisestamise üksikasjadeta

|                              |                                                                                                         |
|------------------------------|---------------------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Vähene kasutus. See funktsioon on asendatud arve töölehega, millel on töövoo funktsioon. |
| **Asendatud teise funktsiooniga?** | Arve töölehe töövoo võimalused.                                                           |
| **Mõjutatud moodulid**             | Ostureskontro                                                                                        |

### <a name="virtual-company-accounts"></a>Virtuaalsed ettevõtted

Virtuaalettevõtete funktsiooni ei toetata enam Dynamics AX-is. Virtuaalettevõtete funktsioon võimaldab kasutajatel seadistada ettevõtete kogumis jagatavaid tabeleid. Funktsiooni kirjelduse leiate siit: [Ettevõtete ja virtuaalettevõtete kontod](https://msdn.microsoft.com/en-us/library/aa834382(v=ax.10).aspx). See funktsioon rühmitab tabelid kogumitesse, mis on määratud virtuaalsetele ettevõtetele, mis on olemasolevate „tõeliste” ettevõtete grupid. Päringud koostatakse nii, et kõik virtuaalse ettevõtte ettevõtted pääsevad seotud tabelikogumites olevate tabelite andmetele juurde.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><b>Kasutuselt eemaldamise põhjus</b></td>
<td><ul>
<li>Enne andmete salvestamist tabelitesse tuleb seadistada virtuaalsed ettevõtted. Virtuaalsete ettevõtete paigutamine olemasolevasse süsteemi on väga raske.</li>
<li>Kuna Dynamics AX-i praeguses versioonis on nii palju andmeid normaliseeritud, on väga raske teada, mida tabelikogumitesse lisada. Näiteks on raske teada, milliseid tabeleid jagada. Kõik tabelid, millele virtuaalses ettevõttes olevad tabelid viitavad, tuleb samuti lisada. Tabeli normaliseerimise tõttu peavad isegi mitmesse tabelisse jaotatud lihtsad koondandmed olema virtuaalse ettevõtte osa. Mis tahes siin tehtud viga põhjustab funktsionaalseid probleeme.</li>
<li>Kui tabel on virtuaalettevõtte osa, kaotab see andmete päritolu andmed ja salvestatakse ainult virtuaalne ettevõte.</li>
</ul></td>
</tr>
<tr class="even">
<td><b>Asendatud teise funktsiooniga?</b></td>
<td>Selleks, et teha tabelid kättesaadavaks kõigi ettevõtete juurest, võib kasutada üldtabeleid. Praegu asendusi ei ole.</td>
</tr>
<tr class="odd">
<td><b>Mõjutatud moodulid</b></td>
<td>Pole kohaldatav</td>
</tr>
</tbody>
</table>

### <a name="warehouse-management-ii"></a>Laohaldus II

|                              |                                                                                                                                                                                                                                                                                                             |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Laohalduse II lahendus (WMS II) moodulis **Varude haldus** dubleerib funktsiooni, mis on olemas Microsoft Dynamics AX 2012 R3-ga välja antud moodulis **Laohaldus**.                                                                         |
| **Asendatud teise funktsiooniga?** | Rakendustes AX 2012 R3, Microsoft Dynamics AX 2012 R3 CU8 ja Microsoft Dynamics AX 2012 R3 CU9 välja antud moodul **Laohaldus** asendab mooduli Laohaldus II funktsioonid. Uuel moodulil on täiustatumad funktsioonid ja paindlikum laohalduse protsess kui moodulil Laohaldus II. |
| **Mõjutatud moodulid**             | Varude haldus, Müük ja turundus, Hanked                                                                                                                                                                                                                                         |

### <a name="worker-reminders-in-human-resources"></a>Töötajate meeldetuletused inimressursside moodulis

Inimressursside palgateave

|                              |                 |
|------------------------------|-----------------|
| **Kasutuselt eemaldamise põhjus**       | Vähene kasutus       |
| **Asendatud teise funktsiooniga?** | Ei              |
| **Mõjutatud moodulid**             | Inimressursid |

### <a name="workplanner"></a>Tööplaanija

|                              |                                                                                                                                                                      |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | Vähene kasutus                                                                                                                                                            |
| **Asendatud teise funktsiooniga?** | Ei, kuid leht **Reeglite suhe**, mis avaneb lehelt **Reegligrupid**, toetab sama äristsenaariumi kui mittesoovitatav leht **Tööplaanija**. |
| **Mõjutatud moodulid**             | Kellaaeg ja kohalolek                                                                                                                                                  |

### <a name="x-financial-statements"></a>X++ finantsaruanded

|                              |                                                                                             |
|------------------------------|---------------------------------------------------------------------------------------------|
| **Kasutuselt eemaldamise põhjus**       | See funktsioon on asendatud teise funktsiooniga.                                    |
| **Asendatud teise funktsiooniga?** | Management Reporter (selles Dynamics AX-i versioonis nimega **Finantsaruandlus**) |
| **Mõjutatud moodulid**             | Pearaamat                                                                              |


