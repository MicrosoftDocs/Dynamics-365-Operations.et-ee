---
title: "Tootmise seadistusnõuded"
description: "Selles artiklis on teave seadistusnõuete kohta, mida peate teadma enne tootmise juhtimisega töötamist."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdParameters, RouteOpr, RouteOprTable, WorkCalendarTable, WorkTimeTable, WrkCtrTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 55561
ms.assetid: 1953059f-478d-4706-b461-25b89ace5fc3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 47fe11168ad2ddea2a7033eda8d8bd8220efea32
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="production-setup-requirements"></a>Tootmise seadistusnõuded

[!include [banner](../includes/banner.md)]

Selles artiklis on teave seadistusnõuete kohta, mida peate teadma enne tootmise juhtimisega töötamist. 

Tootmise juhtimine on integreeritud teiste moodulite funktsioonidega. See vastastikune ühenduvus võimaldab teil muuta tootmistellimusi ja tagada, et need uueneksid automaatselt kõikides muudes süsteemi seotud protsessides ja arvutustes. Järgmised seadistusprotsessid on loetletud nende tegemise järjekorras.

## <a name="required-baseline-setup-in-other-modules"></a>Nõutav alusjoone seadistus muudes moodulites
Muudes moodulites olev teave tuleb seadistada enne, kui saate tootmise juhtimisega töötada. Seadistus hõlmab järgmisi ülesandeid.

-   ettevõtte üldteabe seadistamist;
-   Pearaamatu seadistamist;
-   kaubagruppide määramist;
-   pearaamatukontode seadistamist kaubagruppidele;
-   laokauba tabeli seadistamist laohalduses;
-   materjalikoosluste ja koosluseversioonide loomist laohalduses.

## <a name="required-calendar-and-resource-setup"></a>Vajalik kalendri ja ressursi seadistus
Enne tootmise juhtimise kasutamist avage organisatsiooni haldus ning looge ja määratlege kalender ja operatsiooniressursid järgmises järjekorras.

1.  **Tööajamallid** – seadistage tööajamallid, et määrata kellaajad, mis on saadaval tootmise planeerimisel.
2.  **Kalendrid** – seadistage tööajakalendrid, et määratleda aastas tootmise plaanimiseks saadaval olevad päevad.
3.  **Ressursigrupid** – seadistage ressursigrupid operatsiooniressursside grupeerimiseks, nii et saaksite ajastamise käivitamisel vabast mahust ülevaate. Enne operatsiooniressursside seadistamist pole vaja ressursigruppe seadistada. Kuid soovitame tootmise juhtimise seadistamisel ressursside grupeerimisest aru saada.
4.  **Ressursid** – seadistage operatsiooniressursid, et määrata mitmesugused ressursid, mida kasutatakse tootmisprotsessi lõpetamiseks ja võimsuse planeerimiseks.

## <a name="required-production-parameters-setup"></a>Nõutav tootmise parameetrite seadistus
**Tootmise juhtimise parameetrid** – seadistage põhilised tootmise parameetrid määratlemiseks, kuidas süsteem tootmistellimusi käsitleb ja töötleb. Määratlege, kuidas tootmistellimusi luuakse, hinnatakse, plaanitakse ja tarbitakse. Samuti saate valida, millist tagasisidet soovite ja kuidas kuluarvestust tehakse.

## <a name="required-journal-name-identification"></a>Töölehe nime nõutav identifitseerimine
**Tootmistöölehtede nimed** – määrake tootmistöölehtede nimed, mida kasutatakse kannete kirjendamiseks ja sisestamiseks.

## <a name="setup-if-you-use-operations"></a>Seadistus toimingute kasutamisel
Toimingud kajastavad konkreetseid tegevusi, mida valmis toote tootmiseks tehakse. **Märkus.** Peate teadma kauba tootmiseks vajalikke tegevuste tüüpe ning nende tegevuste järjekorda ja prioriteete. Samuti peate teadma, millised ressursid ja kui palju ressursse on asjaga seotud.

1.  **Toimingud** – seadistage toimingud, mis kajastavad valmis kauba tootmiseks täidetavaid ülesandeid.
2.  **Seosed** – seadistage toimingute seosed üksikasjalike atribuutide kehtestamiseks. Toimingute seoste määratlemiseks klõpsake valikut **Seosed** lehel **Toimingud**.

## <a name="setup-if-you-use-routes"></a>Seadistus protsesside kasutamisel
Kui töötate protsessidega, tuleb määratleda iga tootmisprotsessi jaoks seadistatud toimingud. Protsess kujutab endast teed, mille kaup ühest toimingust teise liikudes läbib, tootmisprotsessi algusest lõpuni.

1.  **Kulukategooriad** – seadistage kulukategooriad määratletud protsesside tunnihinna ja seadistusaegade määratlemiseks.
2.  **Kulugrupid** – seadistage kulugrupid, et luua ja hallata kulude eri tüüpe.
3.  **Protsessigrupid** – seadistage protsessigrupid protsessigruppidega seotud parameetrite määratlemiseks. Enne tootmisprotsesside loomist peate seadistama protsessigrupid.
4.  **Protsessid** – seadistage tootmisprotsessid ja määrake vaikesätted protsessitoimingute plaanimise, kuluarvutuse ja hinnakujunduse ning edenemisaruandluse juhtimiseks.
5.  **Protsessid** – seadistage protsessiversioonid tootmises kaubavariatsioonide lubamiseks.

## <a name="optional-advanced-settings"></a>Valikulised täpsemad sätted
1.  **Tootmisgrupid** – seadistage tootmisgrupid seoste loomiseks tootmistellimuse ja pearaamatukonto vahel. Pearaamatukontosid kasutatakse tellimuste sisestamiseks või grupeerimiseks aruandluse jaoks.
2.  **Tootmiskaustad** – looge tootmiskaustad tootmistellimuste grupeerimiseks, et saaksite töödelda kiireid tootmistellimusi või kustutada ja sisestada tellimuste gruppe.
3.  **Atribuudid** – määratlege atribuudid eriatribuutide loomiseks, mille saate määrata oma ressurssidele tootmiste järjekorra juhtimiseks. Need atribuudid ühendatakse tööajamalliga.





