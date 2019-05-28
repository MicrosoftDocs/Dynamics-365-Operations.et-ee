---
title: Tootmise parameetrid moodulis Tootmise käivitamine
description: See teema käsitleb tootmise parameetrite seadistamist moodulis Tootmise käivitamine.
author: johanhoffmann
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgProdParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: bf1afd18132e92cf081b7bde5067e1be90314467
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565553"
---
# <a name="production-parameters-in-manufacturing-execution"></a>Tootmise parameetrid moodulis Tootmise käivitamine

[!include [banner](../includes/banner.md)]

See teema käsitleb tootmise parameetrite seadistamist moodulis Tootmise käivitamine.

Moodul **Tootmise käivitamine** on mõeldud peamiselt tootmisettevõtetele. Seda saab kasutada aja- ja kaubakulu registreerimiseks tootmistöödel või projektidel. Enne mooduli Tootmise käivitamine kasutamise alustamist tööde registreerimiseks tuleb seadistada mitmesugused tootmisparameetrid, mis määratlevad, kuidas ja kus registreerimised tootmisprotsessi käigus sisestatakse. Tootmisparameetrite sätted mõjutavad varude haldust, tootmise haldust ja kulude arvutamist.

Enne, kui töötajad hakkavad tootmistöid registreerima, tuleks lehel **Tootmise parameetrid** kõik sätted hoolega läbi mõelda. Klõpsake valikuid **Tootmise juhtimine** &gt; **Seadistus** &gt; **Tootmise käivitamine** &gt; **Tootmistellimuse vaikesätted**. Kui teie ettevõte kasutab mitme laoala funktsiooni, võite igale laoalale erinevad tootmise parameetrid seadistada. Parameetrid integreerimiseks mooduliga **Tootmine** seadistatakse lehel **Tootmise parameetrid**.

- **Üldine** – tootmistööde üldised parameetrisätted tootmise käivitamisel.
- **Käivita** – tootmistegevuste alustamisel kasutatavad parameetrid.
- **Toimingud** – tootmisprotsessi ajal tootmistoimingutele ja toimingute tagasisidele rakendatavad parameetrid.
- **Kinnita lõpetamine** – parameetrid, mida kasutatakse, kui kaubad tootmistellimuse viimases toimingus lõpetatuks registreeritakse.
- **Koguste kinnitamine** – tootmistellimuste alustamise ja tagasiside koguste kinnitamiseks kasutatavad parameetrid.

## <a name="types-of-production-jobs"></a>Tootmistööde tüübid
Tootmistööd, mille puhul on nõutav registreerimine, saate valida leheküljel **Töö registreerimine** vahekaardil **Toimingud**.

Tavaliselt teevad töötajad registreeringuid seadistus- ja protsessitööde jaoks. Kui tööde plaanimine on rakendatud, saate siiski tootmistellimuse töötlemisel töötajate registreeritavateks töödeks valida ka muid töö tüüpe. Näiteks võite nõuda registreerimisi transporditööde puhul.

> [!IMPORTANT]
> Kontrollige, et valiksite kõik asjakohased töö tüübid. Muidu ei pruugi tööd leheküljel **Töö registreerimine** registreerimiseks saadaval olla. Teie valikud peaksid ühtima valikutega veerus **Töö haldus** vahekaardil **Seadistus** lehel **Protsessigrupid** (**Tootmise juhtimine** &gt; **Seadistus** &gt; **Protsessid** &gt; **Protsessigrupid**).

Kui protsessigrupis on valitud **Töö haldus**, märgitakse see töö tüüp tootmistellimuses lõpetatuks, kui see töö tüüp on moodulis Tootmise käivitamine lõpetatuks märgitud. Kui kõik jaotises **Töö haldus** valitud töö tüübid on toimingu lõpetatuks kinnitanud, kinnitatakse toiming lõpetatuks ka moodulis Tootmise käivitamine.

> [!NOTE]
> Mõningaid töö tüüpe saab tootmistöölehtede kaudu käsitsi registreerida. Praegusel juhul valige töö tüübiks **Töö haldus**, kuid ärge valige töö tüüpi registreerimiseks mooduli Tootmise käivitamine vahekaardil **Toimingud** lehel **Tootmise parameetrid**.

## <a name="bom-consumption-and-picking-list-journals"></a>Koosluse tarbimine ja komplekteerimislehe töölehed
Koosluse tarbimise järjepidev seadistus on oluline, kuna see aitab garanteerida varude halduse tõhususe. Näiteks kui koosluse tarbimise parameetreid pole moodulis Tootmise käivitamine õigesti seadistatud, võidakse materjalid arvata varudest maha kaks korda või üldse mitte.

Lehel **Tootmise parameetrid** seadistatakse automaatne koosluse tarbimine kolmes etapis.

- Tootmise alustamisel. Seadistage see etapp vahekaardil **Käivita**.
- Tootmisprotsessi käigus, kui mõni toiming lõpetatakse. Seadistage see etapp vahekaardil **Toimingud**.
- Kui tootmistellimus lõpetatuks märgitakse. Seadistage see etapp vahekaardil **Kinnita lõpetamine**.

Igas etapis võimaldab väli **Automaatne koosluse tarbimine** valida ühe kolmest meetodist kaupade komplekteerimiseks tootmistellimuse jaoks.

- **Automaatse tarbimise põhimõte** – seda valikut kasutatakse koos valikuga, mis on määratud kooslusele moodulis **Tootmine**. Klõpsake valikuid **Tootmise juhtimine** &gt; **Üldine** &gt; **Tootmistellimused** &gt; **Kõik tootmistellimused**. Valige lehel **Kõik tootmistellimused** loendist tootmistellimus ja klõpsake siis toimingupaanil valikut **Kooslus**. Lehel **Kooslus** vahekaardil **Seadistus** väljal **Automaatse tarbimise põhimõte** valige üks kolmest võimalusest.

  - **Alustamine**
  - **Lõpetamine**
  - **Käsitsi**
  - Tühi (pole märgitud ühtki valikut.)
  - **Asukohas saadaval**

    Kui moodulis Tootmise käivitamine on valitud **Automaatse tarbimise põhimõte** väljal **Automaatne koosluse tarbimine** vahekaardil **Käivita**, siis arvestatakse kõik materjalid, mille olekuks koosluses on määratud **Käivita**, toimingu alustamisel varudest maha. Valikut **Asukohas saadaval** kasutatakse toodete puhul, millele on lubatud täpsemad laoprotsessid. Kui valite selle automaatse tarbimise põhimõtte, siis eemaldatakse materjal, kui toormaterjali komplekteerimise laotöö on lõpetatud. Materjal eemaldatakse ka siis, kui seda automaatse tarbimise põhimõtet kasutav koosluse rida lattu väljastatakse ja materjal on toodangu sisestuskohas saadaval.

    > [!NOTE]
    > Kui väli **Automaatse tarbimise põhimõte** on mooduli Tootmise käivitamine vahekaardil **Käivita** määratud, tuleb valida sama põhimõte vahekaardil **Toimingud** või vahekaardil **Kinnita lõpetamine**. See nõue aitab tagada, et materjalid arvestatakse varudest maha koosluste puhul, mis kasutavad tootmistellimuse eemaldamise põhimõttena valikut **Lõpetamine**. Kui vahekaardil **Toimingud** või vahekaardil **Kinnita lõpetamine** pole valitud sama automaatse tarbimise põhimõtet, võidakse materjalid varudest kaks korda maha arvestada.

- **Alati** – kui teete etapi puhul selle valiku, arvestatakse materjalid varudest alati selles etapis maha. Näiteks arvestatakse tootmiseks vajalikud materjalid maha tootmistellimuse alustamisel. See säte nõuab, et vahekaartidel **Toimingud** ja **Kinnita lõpetamine** oleks valitud **Mitte kunagi**. See nõue aitab vältida kaupade kaks korda laost mahaarvamist.
- **Mitte kunagi** – kui teete etapi puhul selle valiku, ei toimu selles etapis koosluse tarbimist. Näiteks kui valite kõigil kolmel vahekaardil (**Käivita**, **Toimingud** ja **Kinnita lõpetamine**) **Mitte kunagi**, tuleb materjalid varudest käsitsi maha arvata.

> [!IMPORTANT]
> Mõelge oma tootmisparameetrite seadistus hoolega läbi ja veenduge, et lehe **Tootmise parameetrid** mitmesugustel vahekaartidel valitud parameetrid ei oleks üksteisega vastuolus.

Järgmistes näidetes on illustreeritud parameetrisätteid, mis toetavad mitmesuguseid koosluse tarbimise põhimõtteid. Parameetrid on seadistatud mooduli Tootmise käivitamine lehel **Tootmise parameetrid**.

### <a name="example-1-backflushing-on-operations"></a>Näide 1: operatsioonide tagasiarvestus

Kasutage järgmiseid sätteid, kui komplekteerimistöölehed ja koosluse kauba tarbimine tuleks luua siis, kui kaubad on märgitud toimingus lõpetatuks.

| Vahekaart                | Väli                          | Sätted                             |
|--------------------|--------------------------------|-------------------------------------|
| Käivita              | Uuenda algust võrgus           | **Olek** või **Olek + kogus** |
| Käivita              | Automaatne koosluse tarbimine      | **Mitte kunagi**                           |
| Operations         | Automaatne koosluse tarbimine      | **Alati**                          |
| Teata lõpetamisest | Automaatne koosluse tarbimine      | **Mitte kunagi**                           |
| Teata lõpetamisest | Uuenda lõpetatud aruannet võrgus | **Olek + kogus**               |

### <a name="example-2-backflushing-on-production"></a>Näide 2: tootmise tagasiarvestus

Kasutage järgmiseid sätteid, kui komplekteerimistöölehed ja koosluse kauba tarbimine tuleks luua siis, kui kaubad on märgitud tootmistellimuses lõpetatuks.

| Vahekaart                | Väli                          | Sätted                             |
|--------------------|--------------------------------|-------------------------------------|
| Käivita              | Uuenda algust võrgus           | **Olek** või **Olek + kogus** |
| Käivita              | Automaatne koosluse tarbimine      | **Mitte kunagi**                           |
| Operations         | Automaatne koosluse tarbimine      | **Mitte kunagi**                           |
| Teata lõpetamisest | Automaatne koosluse tarbimine      | **Alati**                          |
| Teata lõpetamisest | Uuenda lõpetatud aruannet võrgus | **Olek + kogus**               |

### <a name="example-3-flushing-principle"></a>Näide 3: automaatse tarbimise põhimõte

Kasutage järgmiseid sätteid, kui komplekteerimistöölehed ja koosluse kauba tarbimine tuleks luua vastavalt koosluse kaubale määratud tagasiarvestuse põhimõttele.

| Vahekaart                | Väli                          | Sätted                |
|--------------------|--------------------------------|------------------------|
| Käivita              | Uuenda algust võrgus           | **Olek + kogus**  |
| Käivita              | Automaatne koosluse tarbimine      | **Automaatse tarbimise põhimõte** |
| Operations         | Automaatne koosluse tarbimine      | **Automaatse tarbimise põhimõte** |
| Teata lõpetamisest | Automaatne koosluse tarbimine      | **Mitte kunagi**              |
| Teata lõpetamisest | Uuenda lõpetatud aruannet võrgus | **Olek + kogus**  |

### <a name="example-4-deduction-of-materials-during-startup-of-a-production-order"></a>Näide 4: materjalide mahaarvamine tootmistellimuse käivitamisel

Kasutage järgmiseid sätteid, kui komplekteerimistöölehed ja koosluse kauba tarbimine tuleks luua siis, kui tootmine käivitatakse.

| Vahekaart                | Väli                          | Sätted                             |
|--------------------|--------------------------------|-------------------------------------|
| Käivita              | Uuenda algust võrgus           | **Olek + kogus**               |
| Käivita              | Automaatne koosluse tarbimine      | **Alati**                          |
| Operations         | Automaatne koosluse tarbimine      | **Mitte kunagi**                           |
| Teata lõpetamisest | Automaatne koosluse tarbimine      | **Mitte kunagi**                           |
| Teata lõpetamisest | Uuenda lõpetatud aruannet võrgus | **Olek** või **Olek + kogus** |

Selles jaotises eespool kirjeldatud valikute põhjal sisestatakse komplekteerimislehe töölehed mitmesugustes tootmistellimuse protsessi etappides.

- Kui toiming käivitatakse
- Kui koguse tagasiside toimingusse märgitakse
- Kui kaubad tootmistellimuses lõpetatuks märgitakse

### <a name="example-5-manual-bom-consumption"></a>Näide 5: käsitsi koosluse tarbimine

Kui materjal tuleks varudest käsitsi maha arvestada, võite kasutada järgmisi sätteid. Sellisel juhul komplekteerimislehe töölehti ei sisestata.


|        Vahekaart         |             Väli              |         Sätted         |
|--------------------|--------------------------------|-------------------------|
|       Käivita        |      Uuenda algust võrgus      | <strong>Olek</strong> |
|       Käivita        |   Automaatne koosluse tarbimine    | <strong>Mitte kunagi</strong>  |
|     Operations     |   Automaatne koosluse tarbimine    | <strong>Mitte kunagi</strong>  |
| Teata lõpetamisest |   Automaatne koosluse tarbimine    | <strong>Mitte kunagi</strong>  |
| Teata lõpetamisest | Uuenda lõpetatud aruannet võrgus | <strong>Olek</strong> |

