---
title: Tootmise seadistusnõuded
description: Selles artiklis on teave seadistusnõuete kohta, mida peate teadma enne tootmise juhtimisega töötamist.
author: johanhoffmann
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProdParameters, RouteOpr, RouteOprTable, WorkCalendarTable, WorkTimeTable, WrkCtrTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 55561
ms.assetid: 1953059f-478d-4706-b461-25b89ace5fc3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bfde8b40927ceaa216878d58ef72c5d91e9ebe01
ms.sourcegitcommit: 133aa728b8a795eaeaef22544f76478da2bd1df9
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/13/2022
ms.locfileid: "7968792"
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
-   Saate tooteteabe halduses luua koosluse versioone.

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
5.  **Protsessiversioon** – seadistage protsessiversioonid tootmises kaubavariatsioonide lubamiseks.

## <a name="optional-advanced-settings"></a>Valikulised täpsemad sätted
1.  **Tootmisgrupid** – seadistage tootmisgrupid seoste loomiseks tootmistellimuse ja pearaamatukonto vahel. Pearaamatukontosid kasutatakse tellimuste sisestamiseks või grupeerimiseks aruandluse jaoks.
2.  **Tootmiskaustad** – looge tootmiskaustad tootmistellimuste grupeerimiseks, et saaksite töödelda kiireid tootmistellimusi või kustutada ja sisestada tellimuste gruppe.
3.  **Atribuudid** – määratlege atribuudid eriatribuutide loomiseks, mille saate määrata oma ressurssidele tootmiste järjekorra juhtimiseks. Need atribuudid ühendatakse tööajamalliga.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
