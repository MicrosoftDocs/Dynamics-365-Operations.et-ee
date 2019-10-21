---
title: Põhivara kulumi arvutamine juriidiliste isikute lõikes
description: Mitme juriidilise isiku põhivara kulumit saab käitada ühe etapina.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, AssetProposalDepreciation, DefaultDashboard, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 500aa71e57f9c1ac8d1a2a080468381bc248741c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187011"
---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a>Põhivara kulumi arvutamine juriidiliste isikute lõikes

[!include [task guide banner](../../includes/task-guide-banner.md)]

Mitme juriidilise isiku põhivara kulumit saab käitada ühe etapina. See protseduur näitab, kuidas seadistada ja käitada protsessi mitme juriidilise isiku jaoks. See kasutab USMF-i juriidilise isiku puhul raamatupidaja rolli ja demoandmeid.


## <a name="set-up-cross-company-depreciation-run-journals"></a>Kontsernisiseste kulumikäituste töölehtede seadistamine
1. Avage Põhivarad > Seadistus > Põhivarade parameetrid.
2. Laiendage jaotist Põhivara ettepanekud.
3. Klõpsake vahekaarti Lisa.
4. Valige või sisestage väärtus väljal Sisestamiskiht.
5. Valige või sisestage väärtus väljal Töölehe nimi.
    * Korrake töölehe seadistust iga juriidilise isiku lehel Põhivara parameetrid.  

## <a name="depreciation-run"></a>Amortiseerimine
1. Avage Põhivarad > Töölehe kirjed > Kulumisoovituse koostamine.
2. Valige või sisestage väärtus väljal Sisestamiskiht.
    * Töölehe nimi põhineb põhivara parameetrites määratud vaikesättel. Seda saab praeguse juriidilise isiku jaoks siin muuta.  
3. Sisestage kuupäev väljale Lõpukuupäev.
    * Valige kulumikäitusesse kaasatavad juriidilised isikud.  
    * Loendis kuvatakse ainult juriidilised isikud, kelle töölehed on põhivara parameetrite lehel põhivara ettepanekute jaoks häälestatud.  
4. Valige väljal Sisesta töölehed väärtus Jah.
    * Filtreerimisväljad hõlmavad kõiki selle kulumikäituse jaoks valitud juriidiliste isikute põhivarasid, gruppe ja raamatuid.  
    * Suvand Pakktöötlus on vaikimisi lubatud. Kui suvand on lubatud, toimub kulumitöölehe loomine ja sisestamine taustal.  
5. Klõpsake suvandit Loo tööleht.
6. Avage Põhivarad > Töölehe sisestused > Põhivarade tööleht.

