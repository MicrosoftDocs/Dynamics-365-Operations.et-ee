--- 
title: "Partii tellimuse elutsükkel loomisest käivitamiseni"
description: "See protseduur juhib teid läbi partiitellimuse elutsükli esimese osa."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdTableListPage, ProdTableCreate, ProdBOM, PmfProdCoBy, ProdParmCostEstimation, ProdCalcTrans, ProdParmRelease, ProdSchedule, ProdRouteJob, ProdParmStartUp, ProdJournalTransBOM, ProdJournalTransRoute
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 94f706241545282fd2744c3be4edc253f2998aff
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="batch-order-lifecycle-from-create-to-start"></a>Partii tellimuse elutsükkel loomisest käivitamiseni

[!include [task guide banner](../../includes/task-guide-banner.md)]

See protseduur juhib teid läbi partiitellimuse elutsükli esimese osa.

Alates loomisest, kulude prognoosimisest ja tootmistöö plaanimisest kuni partiitellimuse tegeliku alguseni.



Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid. 



Protseduuri teise andmekogumiga käitamise eeltingimus on aktiivse valemi ja protsessiversiooniga väljastatud toode.


## <a name="create-a-batch-order"></a>Partiitellimuse koostamine
1. Minge jaotisse Kõik tootmistellimused.
2. Klõpsake valikut Uus partiitellimus.
3. Sisestage või valige väärtus väljal Kaubakood.
4. Klõpsake käsku Loo.
5. Kasutage kiirfiltrit, et filtreerida välja Tootmine väärtuse b järgi.

## <a name="view-production-formula-and-expected-co-products"></a>Tootmisvalemi ja eeldatavate kaastoodete kuvamine
1. Klõpsake toimingupaanil valikut Tootmistellimus.
2. Klõpsake valikut Valem.
3. Sulgege leht.
4. Klõpsake valikut Kaastooted.
5. Sulgege leht.

## <a name="estimate-the-batch-order"></a>Partiitellimuse hindamine
1. Klõpsake suvandit Hinnang.
2. Klõpsake nuppu OK.
3. Klõpsake toimingupaanil valikut Kulude haldamine.
4. Klõpsake suvandit Kuva arvutamise üksikasjad.
5. Sulgege leht.

## <a name="release-the-batch-order"></a>Partiitellimuse väljastamine
1. Klõpsake toimingupaanil valikut Tootmistellimus.
2. Klõpsake valikut Vabasta.
3. Klõpsake nuppu OK.

## <a name="schedule-production-jobs"></a>Tootmistööde plaanimine
1. Klõpsake tegumiribal valikut Graafik.
2. Klõpsake valikut Tööde planeerimine.
3. Tehke väljal Piiratud võimsus valik Ei.
4. Tehke väljal Piiratud materjal valik Ei.
5. Klõpsake nuppu OK.
6. Klõpsake toimingupaanil valikut Tootmistellimus.
7. Klõpsake valikut Kõik tööd.
8. Sulgege leht.

## <a name="start-the-batch-order"></a>Partiitellimuse alustamine
1. Klõpsake nuppu Käivita.
2. Klõpsake vahekaarti Üldine.
3. Tehke väljal Sisesta komplekteerimisleht kohe valik Ei.
4. Klõpsake nuppu OK.
5. Klõpsake toimingupaanil valikut Kuva.
6. Klõpsake suvandit Komplekteerimisleht.
7. Klõpsake loendis valitud real olevat linki.
8. Sulgege leht.
9. Sulgege leht.
10. Klõpsake suvandit Protsessikaart.
11. Klõpsake loendis valitud real olevat linki.
12. Sulgege leht.
13. Sulgege leht.


