---
title: Failidest allettevõtte andmete importimine
description: Selles teemas kirjeldatakse, kuidas ette valmistada andmeid välissüsteemidest, nii et neid saab importida rakendusse Microsoft Dynamics 365 Finance.
author: jinniew
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 4be1e748724331c4e2089da8a08a9ac7e5cf88a2ac6d3d89b37b9fcd4480f516
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6727296"
---
# <a name="import-subsidiary-data-from-files"></a>Failidest allettevõtte andmete importimine

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas ette valmistada andmeid välissüsteemidest, nii et neid saab importida rakendusse Microsoft Dynamics 365 Finance. Kasutate lehte **Konsolideeri impordiga** (**Konsolideerimised \> Konsolideeri impordiga**), et valmistada ette allettevõtte andmete edastamiseks välissüsteemidest.

1. Allettevõtte juriidilise isiku loomine konsolideerimiseks. Lisateavet juriidiliste isikute loomise kohta leiate jaotisest [Juriidilise isiku loomine](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md). Lisateavet leiate jaotisest [Juriidilise isiku ettevalmistamine konsolideerimisprotsessis kasutamiseks](prepare-company-for-consolidation.md) ja [Allettevõtte juriidilise isiku seadistamine konsolideerimiseks](set-up-subsidiary-company-for-consolidation.md).

2. Valmistage ette fail, mis sisaldab imporditud andmeid. Lisateavet importimise protsessi kohta leiate jaotisest [Andmete importimis- ja eksportimistööde ülevaade](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).
3. Eksportige andmed faili, järgides protseduuri "Andmete importimise/eksportimise protsess" jaotises [Andmete importimis- ja eksportimistööde ülevaade](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md). Seda protseduuri saate kasutada andmete konsolideerimiseks kas teisest rakenduse Dynamics 365 Finance eksemplarist või rakendusest Dynamics 365 Business Central. Kui impordite andmeid välissüsteemidest, peavad andmed olema vormingus, mis on kirjeldatud jaotises [Allandmete eksportimine failidesse](export-subsidiary-data-to-file.md).
4. Avage **Konsolideerimised \> Konsolideeri impordiga**. Määratlege lehe **Konsolideeri impordiga** vahekaardil **Kriteeriumid** aruande ja/või impordi üksikasjad, seadistades järgmised väljad.

    | Field                                 | Aruande väärtus | Impordi väärtus |
    |---------------------------------------|----------------------|----------------------|
    | Kirjeldus                           | Pole kohaldatav | Sisestage kirjeldus impordi tuvastamiseks. |
    | Põhikonto                          | Määratlege kontode vahemik, mida aruanne peaks hõlmama. Kui te vahemikku ei määratle, kaasatakse kõik kontod. | Määratlege kontode vahemik, mida import peaks hõlmama. Kui te vahemikku ei määratle, kaasatakse kõik kontod. |
    | Konsolideerimisperiood                  | Määratlege konsolideerimiseks kuupäevavahemik. | Määratlege konsolideerimiseks kuupäevavahemik. |
    | Tegelike summade kaasamine                | Tegelike summade kaasamiseks seadistage see suvand väärtusele **Jah**. | Tegelike summade kaasamiseks seadistage see suvand väärtusele **Jah**. |
    | Eelarvesummade kaasamine                | Eelarvesummade konsolideerimisse kaasamiseks seadistage see suvand väärtusele **Jah**. | Eelarvesummade konsolideerimisse kaasamiseks seadistage see suvand väärtusele **Jah**. |
    | Saldode uuestiloomine konsolideerimise käigus | Seadistage see suvand olekusse **Jah**, kui uuestiloomise protsess peaks täielikult tühjendama saldo ja uued kirjed ning looma saldo uuesti algusest peale. | Seadistage see suvand olekusse **Jah**, kui uuestiloomise protsess peaks täielikult tühjendama saldo ja uued kirjed ning looma saldo uuesti algusest peale. |
    | Eelarvemudelid                         | Pole kohaldatav | Kui valisite eelarvesummade importimise, sisestage konsolideerimiseks eelarvemudelid. |
    | Eelarvekursi tüüp                      | Pole kohaldatav | Sisestage eelarve vahetuskursi tüüp. |

6. Kui teil on erinevad arvestusvaluutad, kasutage välju vahekaardil **Valuuta teisendus**, et konfigureerida konsolideerimise ajal tehtav teisendus.

    | Field                      | Kirjeldus |
    |----------------------------|-------------|
    | Algne juriidiline isik        | Valige juriidiline isik, millest impordite. |
    | Algne arvestusvaluuta | Vaikevaluuta on valuuta, mis on seotud väljal **Algne juriidiline isik** valitud algse juriidilise isikuga. |
    | Lähte- ja sihtkontod       | Määrake kontode vahemik, mida algsest juriidilisest isikust importida. |
    | Vahetuskursi tüüp         | Valige vahetuskursi tüüp. Vahetuskursi tüübid määratakse põhikonto loomisel. Lisateabe jaoks vt [Põhikonto loomine](tasks/create-main-account.md). |
    | Rakenda vahetuskurss alates   | Sisestage kuupäev, et rakendada vahetuskurss, mis kehtis sel kuupäeval. Teise võimalusena sisestage väärtus, mida tuleks kasutada vahetuskursina. |
    | Valuutakurss              | Vaikeväärtus sõltub vahetuskursi tüübist, mille valisite väljal **Vahetuskursi tüüp**. Kui sisestasite kasutaja määratud vahetuskursi, saate määratleda kursi. |

7. Seadistage suvad **Taustal käivitamine** olekusse **Jah**, et võimaldada importimisprotsessi käivitamine taustal.
8. Seadistage suvand **Pakett-töötlus** valikule **Jah**, et käivitada konsolideerimine pakett-tööna määratud ajal. Konsolideerimise koheseks käivitamiseks valige **OK**. 

Kanded ja saldod, mis olid tütarettevõtetes konsolideerimiseks määratud, lisatakse vastavatele konsolideeritud juriidilise isiku kontodele.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]