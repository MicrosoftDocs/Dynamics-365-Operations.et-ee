---
title: Ettevõtte teabe konfigureerimine rakenduses Microsoft Dynamics 365 Talent – Attract
description: Selles teemas selgitatakse, kuidas konfigureerida ettevõtte teavet ja brändingut rakenduse Microsoft Dynamics 365 Talent – Attract jaoks.
author: andreabichsel
manager: AnnBe
ms.date: 12/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 7013065a9494cb407020de2ebcad4058dd57c6c4
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551589"
---
# <a name="configure-company-information-in-microsoft-dynamics-365-talent---attract"></a>Ettevõtte teabe konfigureerimine rakenduses Microsoft Dynamics 365 Talent – Attract
[!include[banner](../includes/banner.md)]

Rakenduse Microsoft Dynamics 365 Talent: Attract halduskeskuses on konfiguratsioonisätted, integratsiooni- ja häälestussuvandid rakenduse Attract jaoks.

## <a name="company-information"></a>Ettevõtte andmed

Sisestage kuvatav ettevõtte nimi ja lisage ettevõtte logo. Kuvatavat nime ja logo saab siis kasutada töökuulutustel ning sisseelamisperioodil.

## <a name="linkedin-integration"></a>LinkedIni integreerimine

Seadistage integreerimine lahendusega LinkedIn Recruiter System Connect(RSC). Pärast ühenduse loomist LinkedIniga LinkedIni sisselogimisteabe abil, saate sünkroonida kandidaadi LinkedIni profiili, avaldusi, töövestluste tagasisidet ja värbamistöörühma märkmeid. Vajalik on LinkedIni värbaja täislitsents. Platvormi LinkedIn Recruiter kohta leiate lisateavet spikriartiklist [Recruiter System Connect (RSC) – FAQ](https://www.linkedin.com/help/recruiter/answer/90483).

## <a name="user-permissions"></a>Kasutajaõigused

Määrake oma organisatsioonis olevatele kasutajatele rolle. Kasutada on järgmised rollid: **Administraator**, **Värbaja**, **Personalijuht** ja **Kirjutuskaitstud**. Kasutajaõiguste kohta leiate lisateavet artiklist [Turvalisus ja rollihaldus Attractis](./security-attract.md).

## <a name="feature-management"></a>Funktsioonide haldus

Uute funktsioonide lisamisel võidakse need avaldada avalikus eelversioonis. Avaliku eelversiooni funktsioonid ei vasta kõigile teenusenõuetele. Neid vastu võttes nõustute oma andmeid jagama välissüsteemidega. Võite avastada, et teie organisatsioon ei vaja kõiki avaldatud uusi funktsioone. Te saate avaliku eelversiooni funktsioone välja ja sisse lülitada olenevalt oma organisatsiooni vajadustest.

## <a name="template-management"></a>Mallihaldus

Protsessimall sisaldab kõiki tegevusi, mis peaksid olema tööle värbamise protsessi osad. Teie organisatsioon võib lubada värbamisprotsessi malle luua kõigil töörühma liikmetel või ainult administraatoritel. Töörühma liikmetele värbamisprotsessi mallide loomise lubamiseks lülitage sisse mallihalduse funktsioon. Protsessimallide kohta leiate lisateavet artiklist [Protsessimallid Attractis](./process-templates-attract.md).

## <a name="email-template-settings"></a>E-kirja malli sätted.

Organisatsioonid saavad luua meilimalle mitmesuguste olukordade jaoks. Võimalik on valida meilimallidele lisatav päisepilt. Valitud päis lisatakse seejärel kõigile meilimallidele. Malli jalusesse saate lisada oma organisatsiooni privaatsusavalduse ja teadetega seotud kasutustingimuste lingi. Lisateavet leiate artiklist [Meilimallid Attractis](./email-templates.md).

## <a name="offer-process"></a>Pakkumise protsess

Te saate konfigureerida tööpakkumiste kinnitamisprotsessi. Näiteks saate määrata, kas pakkumine peab olema kinnitatud enne selle saatmist kandidaadile. Samuti võite teha kohustuseks, et kinnitajad peavad jätma pakkumisega seotud otsuse kohta kommentaari.

Kasutada on kaks kinnitamise töövoogu: **Paralleelne** ja **Järjestikune**.

- **Paralleelne** – kinnitatavad pakkumised saadetakse kinnitajatele üheaegselt.
- **Järjestikune** – kinnitatavad pakkumised saadetakse kinnitajatele kindlas järjekorras.

Samuti saate konfigureerida kandidaadi kogemusega seotud suvandeid. Näiteks üks suvand võimaldab määrata, kas kandidaadid saavad pakkumise tagasi lükata ilma järgneva aruteluta. Kui määrate suvandi **Luba kandidaatidel pakkumine tagasi lükata ilma järgneva aruteluta** olekuks **Ei**, siis on kandidaaditele olemas nupp **Lükka pakkumine tagasi**. Kui määrate suvandi olekuks **Jah**, saavad kandidaadid pakkumise tagasi lükkamiseks valida põhjuse ja seejärel nupu **Lükka pakkumine tagasi**.

Samuti saate määrata pakkumistele aegumiskuupäeva ja seda jõustada. Kui määrate suvandi **Nõutud aegumiskuupäev kõigi pakkumiste puhul** olekuks **Jah**, aeguvad pakkumised määratud tundide või päevadega.

Pakkumiste haldamise kohta leiate lisateavet artiklist [Pakkumiste halduse seadistamine](./offer-setup.md).
