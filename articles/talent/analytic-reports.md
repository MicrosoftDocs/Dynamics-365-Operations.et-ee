---
title: Analüüsiaruannete kasutamine rakenduses Microsoft Dynamics 365 Talent – Attract
description: Selles teemas kirjeldatakse analüüsiaruandeid värbamisprotsessi ülevaate saamiseks rakenduses Microsoft Dynamics 365 Talent – Attract
author: fewatson
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: fewatson
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent April 2019 update
ms.openlocfilehash: be62fe9a5021cfa83a465d316b182c0a154c0c50
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/23/2019
ms.locfileid: "2010003"
---
# <a name="use-analytic-reports"></a>Analüütiliste aruannete kasutamine

Microsoft Dynamics 365 Talent: Attracti analüütiliste aruannetega pakutakse valmislahendusi (OOTB) värbamisprotsessi ülevaadete jaoks. Saadaval funktsioonid on:

- **Töö analüüs** – klõpsake **Analüüsi** vahekaardil tööle, et näha ttöökoha kandidaatide mõõdikuid.
- **Analüüsi keskus** – klõpsake **Analüüs** vasakul navigeerimispaanil tööde kohta koondmõõdikute nägemiseks.
- **Kasutajapõhine turvalisus** – Attract haldab aruannetele juurdepääsu [rolli](security-attract.md) ja töö osaleja rolli.
- **Ristfiltreerimine** – klõpsake aruande visuaale, et vaadata valitud andmete alusel filtreeritud muid mõõdikuid.

>[!NOTE] 
>- See funktsioon on praegu [eelvaateversioonis](access-preview-feature.md). Selle proovimiseks peab teil olema [**tervikliku värbamise lisandmoodul.**](attract-comprehensive-hiring.md).
>- Kõik avalikud eelvaate aruanded kuvatakse inglise keeles.
>- Aruandeid värskendatakse iga kolme tunni järel. Viimane värskendamisaeg (kohalikus ajavööndis) asub aruande ülaosas. Värskendamise ajad on ligikaudsed ja varieeruvad vastavalt teie regiooni andmemahu ja ressursi koormusele.

## <a name="job-analytics"></a>Tööanalüüs

Töö analüüsi aruanne on ülevaade värbamisprotsessist.  Põhimõõdikud on järgmised.

- Aktiivsed kandidaadid etapi kaupa
- Kandidaadi allikas
- Kandidaadi tüüp (sisemine või väline)

## <a name="analytics-hub"></a>Analüüsi keskus

Analüüsi keskuse aruanded koondavad tööandmeid kõigi tööde kohta, et välja tuua värbamisprotsessi suundumused. Attract sisaldab kahte OOTB-aruannet: müügivõimaluste kokkuvõte ja lehtri analüüs.

### <a name="pipeline-summary"></a>Müügivõimaluste kokkuvõte

Müügivõimaluste kokkuvõtte aruanne koondab avatud tööde andmeid. Põhimõõdikud on järgmised.

- Kõikide tööde kandidaadid etapi järgi
- Kandidaadi allikas
- Avatud tööd staažitaseme järgi

### <a name="funnel-analysis"></a>Lehteranalüüs

Lehteranalüüsi aruanne koondab andmed tööde kohta, mis on suletud ametikoha täitmise pärast. Põhimõõdikud on järgmised.

- Värbamisaeg
- Mõõdikute teisendus (üle liikumisel)
- Pakkumise vastuvõtmismäär

Märkus. Ajaliselt kõige täpsemaks värbamisaruandluseks on soovitatav kasutada [pakkumise halduse](offer-setup.md), funktsiooni, mis on saadaval tervikliku värbamise lisandmooduli osana.

>[!TIP] 
>Lisateabe saamiseks liigutage kursorit visuaalide kohal. Näiteks, liikudes üle visuaali **Aktiivses kandidaadid**, kuvatakse keskmine päevade arv etapis. Selle teabe analüüsimine võib anda kriitilise tähtsusega ülevaate värbamisaja vähendamiseks ja lubab värbajatel keskenduda meetoditele, milllega vähendada igale etapile kulutatud aega.

## <a name="user-specific-security"></a>Kasutajapõhine turve

Attracti aruanded on saadaval administraatori, loe kõike, värbaja ja personalijuhi [rollidele](security-attract.md)- Määramata kasutajatel ei ole juurdepääsu kummalegi analüüsiaruannete lehtele, (Töö analüüs või Analüüsi keskus).

Töö analüüsi aruanded kuvavad andmeid valitud töö kohta. Analüüsi keskuse aruanded koondavad andmed kõigi tööde kohta, mida kasutaja saab vaadata. Kasutajatele, kes saavad vaadata nii Minu töid kui ka Kõiki töid Tööde lehel, on samad vaated saadaval ka Analüüsi keskuses.

## <a name="cross-filter"></a>Ristifilter

Üks Power BI suurepärastest funktsioonidest on see, kuidas kõik aruande lehe visuaalid on omavahel ühendatud. Kui valite andmepunkti ühe visuaali alusel, siis kõik teised lehel olevad visuaalid, mis sisaldavad samu andmeid, muutuvad tehtud valiku põhjal. Vaadake lisateavet ja näidet, [Kuidas visuaalid ristfiltreerivad üksteist Power BI aruandes](https://docs.microsoft.com/power-bi/consumer/end-user-interactions).

## <a name="export-to-excel"></a>Excelisse eksportimine

Aruande andmete Excelis vaatamiseks klõpsake menüüs Suvandid (kolm punkti) visuaalil ja valige **Alusandmete eksportimine.** Eksporditud andmed eksporditakse filtreeritud kujul, austades kasutaja õigusi Attractis. Lisateavet vt teemast [Andmete eksportimine visualiseeringutest](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data).
