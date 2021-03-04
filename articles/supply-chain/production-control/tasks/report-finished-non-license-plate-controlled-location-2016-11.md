---
title: Lõpetatuna kinnitamine asukohta, mida ei juhi litsentsiplaat (avaldus, mai 2016)
description: Selles ülesande juhendis esitatakse näide lõpetatuks kuulutamisest mittelitsentsiplaadiga juhitava asukoha jaoks.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdParmCostEstimation, ProdParmStartUp, ProdParmReportFinished, WHSWorkTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a9010b95cfd0528cd3b532627d19a3b340bdca4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425952"
---
# <a name="report-as-finished-to-a-non-license-plate-controlled-location--application-may-2016"></a>Lõpetatuna kinnitamine asukohta, mida ei juhi litsentsiplaat (avaldus, mai 2016)

[!include [banner](../../includes/banner.md)]

Selles ülesande juhendis esitatakse näide lõpetatuks kuulutamisest mittelitsentsiplaadiga juhitava asukoha jaoks. Selle ülesande eeltingimus on kehtiv tööpoliitika. Eelmises ülesande juhendis selgitati tööpoliitika seadistamist. Selle tegevusjuhise jaoks on nõutav rakenduse Dynamics AX-i versioon 7.0.1 või uuem.




## <a name="set-up-an-output-location"></a>Väljundi asukoha seadistamine
1. Avage Organisatsiooni haldus > Ressursid > Ressursigrupid.
2. Valige loendist ressursigrupp 5102.
3. Klõpsake nuppu Redigeeri.
4. Sisestage väljale Väljastusladu väärtus 51.
5. Sisestage väljale Väljundi asukoht väärtus 001.
    * Asukoht 001 pole litsentsiplaadiga juhitav asukoht. Saate seadistada mittelitsentsiplaadi väljundi asukoha ainult siis, kui asukohale on olemas vastav tööpoliitika.  

## <a name="create-a-production-order-and-report-it-as-finished"></a>Tootmistellimuse loomine ja selle lõpetatuna kinnitamine
1. Sulgege leht.
2. Avage Tootmise juhtimine > Tootmistellimused > Kõik tootmistellimused.
3. Klõpsake valikut Uus tootmistellimus.
4. Sisestage väljale Kauba kood väärtus L0101.
5. Klõpsake käsku Loo.
6. Klõpsake toimingupaanil valikut Tootmistellimus.
7. Klõpsake suvandit Hinnang.
8. Klõpsake nuppu OK.
9. Klõpsake käsku Käivita.
10. Klõpsake vahekaarti Üldine.
11. Tehke väljal Automaatne koosluse tarbimine valik Mitte kunagi.
12. Klõpsake nuppu OK.
13. Klõpsake valikut Kinnita lõpetamine.
14. Klõpsake vahekaarti Üldine.
15. Tehke väljal Aktsepteeri viga valik Jah.
16. Klõpsake nuppu OK.
17. Klõpsake toimingupaanil valikut Ladu.
18. Klõpsake suvandit Töö üksikasjad.
    * Kui tootmistellimus on lõpetatuks kuulutatud, pole ladustamiseks tööd loodud. See ilmneb, kuna määratletud on tööpoliitika, mis takistab töö loomist, kui toode L0101 kuulutatakse lõpetatuks asukohale 001.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]