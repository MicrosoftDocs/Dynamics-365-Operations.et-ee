---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent Core HR (6. detsember 2018)
description: Selles teemas kirjeldatakse funktsioone, mis on kas uued või muutunud rakenduses Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 12/07/2018
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
ms.search.validFrom: 2018-12-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 462b87a655e3e4017cffd2ba41cb6d1f18de3e50
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529158"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-december-6-2018"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent Core HR (6. detsember 2018)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

**Järk 8.1.2071**

Teema kirjeldab funktsioone, mis on Core HR-is kas uued või muudetud.


## <a name="platform-update-22-for-finance-and-operations"></a>Teenuse Finance and Operations platvormivärskendus 22

### <a name="export-up-to-1-million-rows-to-excel"></a>Kuin 1 miljoni rea eksportimine Excelisse

Excelisse eksportimise funktsiooni saab nüüd konfigureerida nii, et see võimaldab kasutajal rakenduse Talent ruudustikust eksportida kuni 1 miljon rida, märkimisväärselt rohkem eelmisest 10 000 rea piirist. 

### <a name="restyled-personalization-toolbar"></a>Ümberkujundatud isikupärastamise tööriistariba

Isikupärastamise tööriistariba on Finance and Operations platvormivärskendusega nr 22 ümberkujundatud, et aidata kasutajatel oma rakenduse Talent kogemust lihtsamini kohandada. Tehti järgmised muudatused. 

-  Nüüd näidatakse iga isikupärastamistööriista nime ikooni juures, mis aitab kasutajatel kiiresti ära tunda selle tööriista, mida nad kasutada soovivad.
-  Käesoleva tööriista kasutamise kirjeldust näidatakse nüüd samuti, see aitab kasutajal mõista, kuidas teha vajalikke isikupärastamisi.  
-  Kogu isikupärastamise tööriistariba saab liigutada lohistades mööda ekraani, kukutades selle konkreetsele alale tööriistaribast vasakul. See võimaldab kasutajal isikupärastada elemente, mida tööriistariba varem varjas.   

### <a name="optimized-is-one-of-filtering-experience"></a>Optimeeris filtri „üks (mitmest)“ kasutuse

"Üks (mitmest)" filtreerimise operaator on enamike väljade jaoks saadaval kasutades filtripaani ja ruudustiku päise rippmenüüsid. See operaator võimaldab kasutajal välja filtreerida põhinedes mitmele väärtusele. Uus ja täiustatud kogemus "üks (mitmest)" operaatorile on saadaval Finance and Operations platvormivärskendusega nr 22. Lisainfo saamiseks vt [Optimeeritud "üks (mitmest)" filtreerimiskogemus](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/improved-isoneof-filtering).

### <a name="paste-lists-from-excel-into-filter-fields-with-the-is-one-of-operator"></a>KKleepige "üks (mitmest) operaatoriga Execlist pärinevaid loendeid filtri väljadele

Mõnede ülesannete juures võib kasutajatel olla Excelis väärtuste loendud, mida nad sooviksid kasutada andmete filtreerimiseks rakenduses Talent. Näiteks või olla Inimressursside kasutaja määranud aruandest teatud töötajad, kes vajavad süsteemis lisanduvat uurimist, ja oleks ideaalne, kui see kasutaja saaks kopeerida selle nimekirja otse Excelist rakenduse Talent filtri väljale.

Alates Finance and Operations platvormivärskendusest nr 22, tunneb nüüd "üks (mitmest) operaator Filtripaani ja ruudustiku veeru filtreerimisel ära Excelist kopeeritud nimekirjad, nii et neid saab otse filtri väljale kleepida. See sisaldab erinevatest Exceli ridadest ja veergudest kopeeritud väärtuste kogu. Selle funktsiooni kohta lisateabe saamiseks vt [Excelist loendite kleepimine filtri väljadele "üks (mitmest)" operaatoriga](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/paste-filter-lists-from-excel).

## <a name="in-preview"></a>Eelvaates

### <a name="configure-uk-payroll-integration-between-talent-and-dayforce"></a>UK palgaarvestuse integratsiooni konfigureerimine Talenti ja Dayforce’i vahel

Integratsioon rakenduste Talent ja Ceridian Dayforce vahel on UK-s eelvaatena saadaval. Lisainfo saamiseks vaadake järgmist teemat, [Palgaarvestuse integreerimine rakenduste Talent ja Dayforce vahel](https://docs.microsoft.com/dynamics365/unified-operations/talent/configure-payroll-integration).

## <a name="coming-soon"></a>Peagi tulekul

### <a name="leave-and-absence-future-leave-and-forecasting-leave-balances"></a>Puhkus ja puudumine: tulevaste puhkuste ja puhkusesaldo ennustamine

Vabade päevade kuvamine on muutumas koos muutustega, mida tehakse võimaldamaks töötajatel ennustada vagu päevi ja esitada tulevikus vabade pävade taotlusi ilma praegust vabade pävade saldot mõjutamata. 

Praegu kuvatud saldo on taotlemiseks saadaval olev vabade päevade hulk, sealhulgas viitvõlad tänaseni ja kõik heakskiidetud puhkuseavaldused kuni aegade lõpuni. 

Kui ennustamise suutlikus on väljastatud, muutub kuvatav saldo puhkusepäevade hetkesaldoks, sealhulgas viitvõlad tänaseni ja tänased taotlused. Töötajad ja juhid näevad neid värskendatud saldosid töötaja ja juhi iseteeninduses kaardil **Vaba aeg** ja aknas **Puhkusesalde**. Personalijuhid näevad neid värskendatud saldosid tööruumise **Inimesed** ja töötaja aknas **Määratud puhkuseplaanid**.

## <a name="other-changes"></a>Muud muudatused 

### <a name="termination-code-is-not-populated-to-the-worker-position-assignment-record"></a>Lõpetamise koodi ei lisata töötaja ametikoha määramise kirjele

Rakendatud on muudatus, mis täidab töösuhte lõpetamisprotsessi käigus ametikohe määramise kirjele põhjuse koodi.

### <a name="validation-for-personnel-number-being-in-use-needs-additional-details"></a>Kasutuses oleva personalinumbri kinnitamine vajab lisaandmeid

Lisateavet kuvatakse siis, kui numbriseeriad on kasutuses, selleks, et mõista paremini probleeme juhul, kui uut numbrit ei saa genereerida.
 
### <a name="attachments-buttons-not-available-for-workers"></a>Manuste nupud pole töötajatele saadaval

ÕManuste parandamiseks on tehtud muudatusi. Töötajale uut manust lisades on nüüd saadaval nupud **Uus** ja **Redigeeri**, kui FactBoxes on töötaja aknas avatud. 

## <a name="known-issues"></a>Teadaolevad probleemid

### <a name="mapping-errors-in-the-integration-with-finance"></a>Vastendusvead Finance’iga integreerimisel

Praegusel mallil on tuvastatud rakenduse Talent integreerimisel rakendusega Finance järgmised probleemid. Uus mall avaldatakse varsti ja see rakendatakse kõigile uutele loodavatele integreerimisprojektidele. Olemasolevate integreerimisprojektide puhul saab ülesande vastendamist uuendada. Vaadake uuendatud vastendusi järgmisest tabelist. 

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

Värskendatud vastendused peaksid välja nägema sellised.

![Osakonnast Tootmisüksusesse ülesanne](./media/DepartmentMapping.png)


Töödelt Töö üksikasjade ülesanne vajab järgmiste vastenduste uuendamist.

| Olemasolev allika väli          | Uus allika väli                   |
| -------------------------------|------------------------------------|
| cdm_name (nimi)                | cdm_description (kirjeldus)      |
| cdm_name (kirjeldus)         | cdm_description (töökirjeldus)|


Värskendatud vastendused peaksid välja nägema sellised.

![Töödelt töö üksikasjadele ülesanne](./media/JobMapping.png)

Töötajatelt Tööülesandele ülesanne vajab järgmiste vastenduste uuendamist.

| Olemasolev allika väli                 | Uus allika väli                               |
| --------------------------------------|------------------------------------------------|
| cdm_emailaddress1 (e-posti aadress 1)   | cdm_primaryemailaddress (esmane e-posti aadress) |
| cdm_telephone1 (telefon 1)          | cdm_primarytelephone (esmane telefoninumber)       |

Soo välja muutmine vajab samuti värskendamist. Valige vastenduse tüüp **fn** (funktsioon) Soole ja värskendada järgmisi väärtuste vastendusi.

| Common Data Service Väärtus | Finance and Operations väärtus | | ------------|------------------ -----------| | 75440000 | Male | | 75440001 | Female | | 75440002 | Pole | | 75440003 | Mittespetsiifiline |

Värskendatud vastendused peaksid välja nägema sellised.

![Töötajatelt töötajale ülesanne](./media/WorkerMapping.png)

![Soo välja muutumine](./media/WorkerTransform.png)

