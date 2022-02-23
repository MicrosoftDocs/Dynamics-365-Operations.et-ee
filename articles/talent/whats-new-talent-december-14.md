---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent Core HR (14. detsember 2018)
description: Selles teemas kirjeldatakse funktsioone, mis on kas uued või muutunud rakenduses Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 12/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-12-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 9887d22a513e820c35c51b6c702e2d9d34ab1214
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529752"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-december-14-2018"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent Core HR (14. detsember 2018)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

**Järk 8.1.2085**

Teema kirjeldab funktsioone, mis on Core HR-is kas uued või muudetud.

## <a name="changes"></a>Muudatused

### <a name="us---aca-affordable-care-act-support-for-tax-year-2018-1095-b-and-1095-c-forms"></a>US - ACA (Taskukohase ravikindlustuse eelnõu) toetavad maksuaasta 2018 1095-B ja 1095-C vorme

Igal aastal peab Kohaldatav suur tööandja (ALE) andma igale täistööajaga töötajale vormi 1095-C. PEale selle, kui tööandja pakub enda kindlustust, peab ta väljastama vormi 1095-C (kui nad on ALE) ja 1095-B (kui nad on väike tööandja) kõigile töötajatele, täis- või osalise tööajaga, kes on nende pakutava tervisekindlustusega kaetud. See funktsioon annab vormide 1095-C ja 1095-B prinditavad vormid.

### <a name="during-import-submittedbypersonid-field-on-hcmperfjournalentity-is-ignored"></a>Importimise ajal eiratakse HcmPerfJournalEntity välja SubmittedByPersonId

Jõudluse töölehe kannete importimisel/eksportimisel ignoreeritakse välja **Edastaja**. Selle muudatusega peegeldab väärtus **imporditud/eksporditud** tabeli väärtust ekspordi ajal, kui importides uuendatakse süsteemi impordifailis antud väärtusega.

### <a name="analytics-tab-on-leave-and-absence-workspace-displays-openconnectionerror-error-for-non-system-admin-roles"></a>Analüüsi vahekaart tööruumis "Puhkused ja puudumine" kuvab mitte-administraatori rollide korral viga "OpenConnectionError"

Selle värkendusega ei anta vahekaardi **Analüüs** avamisel tööruumis **Puhkused ja puudumine** viga.

### <a name="employee-self-service-position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a>Töötaja iseteeninduskeskuses ei saa ametikoha hierarhia süvitsi minemine emasõlme

Tehtud on muudatus vea "Emasõlme hankimine ebaõnnestus" parandamiseks juhul, kui ametikoha hierarhia on kohandatud ilmuma olemasolevasse tööruumi ja hierarhias valitud ametikohale.  

### <a name="must-be-system-admin-to-see-the-payroll-tab-in-the-position-page"></a>Ametikoha lehel vahekaardi Palk nägemiseks peab olema süsteemiadministraator

Tehtud on muudatus õige turvaelemendid kaasamiseks olemasolevas privileegis: "Palga töötaja ja ametikoha üksikasjade säilitamine". Selle muudatusega on Palgaarvestuse administraatoril vaikimisi juurdepääs ametikoha lehekülge palga väljadele.

### <a name="error-when-submitting-performance-review-to-manager-and-the-reviewsperfperiod-placeholder-is-used-in-the-submission-instructions"></a>Tõrge jõudluse ülevaate esitamisel juhile ja kohatäidet %Reviews.PerfPeriod% kasutatakse saatmisjuhistes

Tehtud on muudatus, mis parandab vea "Nullviide" kohatäite %Reviews.PerfPeriod% kasutamisel saatmisjuhistes.

### <a name="workforce-power-bi-report-shows-error-when-worker-seniority-date-is-a-leap-day"></a>Tööjõu Power BI aruandes kuvatakse tõrge, kui töötaja staaži kuupäv on liigaastal

Selle muudatusega toetab Power BI nüüd liigaastaid.

### <a name="integration-between-core-hr-and-attract"></a>Integratsioon Core HR ja Attracti vahel

Tehtud on muudatus Core HR ja Attracti palgatavate kandidaatide integratsiooni värskendamiseks. Et palgatavad kandidaadid oleksid tööruumis **Personalihaldus** nähtavad, kasutatakse järgmisi rakenduse Common Data Service üksuseid:

Tööavaldus
- Olek Põhjus peab olema määratud Pakkumine vastu võetud peale
-   Annab kandidaadi ja vaba töökoha

Kandidaat
-   Annab kandidaadi teabe

Vaba töökoht
-   Annab vaba töökoha ID ja vaba töökoha osalejad

Vaba töökoha osalised
-   Annab värbamisjuhi

Kui kandidaat lisatakse Personalihaldusesse, saab kandidaati nüüd kandidaadi kaardil oleva uue valiku abil kõrvale jätta.

## <a name="coming-soon"></a>Peagi tulekul

### <a name="leave-and-absence-future-leave-and-forecasting-leave-balances"></a>Puhkus ja puudumine: tulevaste puhkuste ja puhkusesaldo ennustamine

Vabade päevade kuvamine on muutumas koos muutustega, mida tehakse võimaldamaks töötajatel ennustada vagu päevi ja esitada tulevikus vabade pävade taotlusi ilma praegust vabade pävade saldot mõjutamata. 

Praegu kuvatud saldo on taotlemiseks saadaval olev vabade päevade hulk, sealhulgas viitvõlad tänaseni ja kõik heakskiidetud puhkuseavaldused kuni aegade lõpuni. 

Kui ennustamise suutlikus on väljastatud, muutub kuvatav saldo puhkusepäevade hetkesaldoks, sealhulgas viitvõlad tänaseni ja tänased taotlused. Töötajad ja juhid näevad neid värskendatud saldosid töötaja ja juhi iseteeninduses kaardil **Vaba aeg** ja aknas **Puhkusesalde**. Personalijuhid näevad neid värskendatud saldosid tööruumise **Inimesed** ja töötaja aknas **Määratud puhkuseplaanid**.

## <a name="known-issue"></a>Teadaolev probleem

### <a name="mapping-errors-in-the-integration-with-finance"></a>Vastendusvead Finance’iga integreerimisel

Praegusel mallil on tuvastatud rakendustega Dynamics 365 Finance integreerimisel järgmised probleemid. Uus mall avaldatakse varsti ja see rakendatakse kõigile uutele loodavatele integreerimisprojektidele. Olemasolevate integreerimisprojektide puhul saab ülesande vastendamist uuendada. Vaadake uuendatud vastendusi järgmisest tabelist. 

>[!NOTE]
> Andmete integreerimine Ametikohtast Ametikoha peamisele tööülesandele ei toimi. Seda probleemi praegu uuritakse. Praegusele vastendusele lahendust ei ole. 

Osakonnast tootmisüksusele ülesanded vajavad järgmiste vastenduste uuendamist.

| Olemasolev allika väli          | Uus allika väli |
| -------------------------------|------------------|
| cdm_description (kirjeldus)  | cdm_name (nimi)  |

Lisada tuleb ka lisanduv vastendamine. Valige Viimane väli **Puudub**, et lisada järgmine vastendamine.

| Lähteväli                   | Sihtväli    |
| -------------------------------|----------------------|
| cdm_description (kirjeldus)  | NAMEALIAS (NAMEALIAS)|

Värskendatud vastendused peaksid välja nägema nagu järgmisel pildil.

![Osakonnast Tootmisüksusesse ülesanne](./media/DepartmentMapping.png)


Töödelt Töö üksikasjade ülesanne vajab järgmiste vastenduste uuendamist.

| Olemasolev allika väli          | Uus allika väli                   |
| -------------------------------|------------------------------------|
| cdm_name (nimi)                | cdm_description (kirjeldus)      |
| cdm_name (kirjeldus)         | cdm_description (töökirjeldus)|


Värskendatud vastendused peaksid välja nägema nagu alloleval pildil.

![Töödelt töö üksikasjadele ülesanne](./media/JobMapping.png)

Töötajatelt Tööülesandele ülesanne vajab järgmiste vastenduste uuendamist.

| Olemasolev allika väli                 | Uus allika väli                               |
| --------------------------------------|------------------------------------------------|
| cdm_emailaddress1 (e-posti aadress 1)   | cdm_primaryemailaddress (esmane e-posti aadress) |
| cdm_telephone1 (telefon 1)          | cdm_primarytelephone (esmane telefoninumber)       |

Soo välja muutmine vajab samuti värskendamist. Valige vastenduse tüüp **fn** (funktsioon) Soole ja värskendada järgmisi väärtuste vastendusi.

| Common Data Service väärtus                   | Finance and Operations väärtus                     |
| ----------------------------|--------------------------------------------------|
| 75440000                    | Mees                                             |
| 75440001                    | Naine                                           |
| 75440002                    | None                                             | 
| 75440003                    | NonSpecific                                      |

Värskendatud vastendused peaksid välja nägema nagu järgmistel piltidel.

![Töötajatelt töötajale ülesanne](./media/WorkerMapping.png)

![Soo välja muutumine](./media/WorkerTransform.png)
