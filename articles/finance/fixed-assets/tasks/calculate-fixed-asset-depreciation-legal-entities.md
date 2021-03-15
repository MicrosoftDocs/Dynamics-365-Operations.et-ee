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
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8b09bbe4d0143aa521ca0a4cf67e86b7165b0f4f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968950"
---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a>Põhivara kulumi arvutamine juriidiliste isikute lõikes

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]