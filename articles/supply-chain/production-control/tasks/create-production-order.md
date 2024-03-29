---
title: Tootmistellimuse loomine
description: Selles protseduuris näitlikustatakse, kuidas luua tootmistellimust.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdTable, ProdBOM, ProdRoute, ProdJournalCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cb7eb237758acb6f27c636050fa5a74d1fd758f1
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580692"
---
# <a name="create-a-production-order"></a>Tootmistellimuse loomine

[!include [banner](../../includes/banner.md)]

Selles protseduuris näitlikustatakse, kuidas luua tootmistellimust. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid. See on esimene protseduur seitsmest, mis selgitab tootmistellimuse elutsüklit.


## <a name="create-a-production-order"></a>Tootmistellimuse loomine
1. Avage Tootmise juhtimine > Tootmistellimused > Kõik tootmistellimused.
2. Klõpsake valikut Uus tootmistellimus.
3. Sisestage väljale Kaubakood tüüp D0001.
4. Sisestage tarnekuupäev väljale Tarne.
    * Tarnekuupäev näitab, millal peab tootmistellimus lõppema, et tarne toimuks tähtaegselt. Seda kuupäeva saab planeerimisprotsessis kasutada. Näiteks saate tellimuse planeerida tellimuse jaoks määratud tarnekuupäevast tagasi.  
5. Määrake koguse väärtuseks 20.
    * Märkus: koosluse numbri väljal kuvatakse automaatselt praeguse kauba aktiivse koosluse number, kuid saate tootmistellimuse kooslust muuta, valides aktiivse koosluse kinnitatud koosluse versioonide loendist.    Märkus: protsessi numbri väljal kuvatakse automaatselt praeguse kauba aktiivse protsessi number, kuid saate tootmistellimuse protsessi muuta, valides aktiivse protsessi kinnitatud protsessi versioonide loendist.  
6. Klõpsake käsku Loo.

## <a name="validate-the-production-order"></a>Tootmistellimuse kinnitamine
1. Klõpsake loendis valitud real olevat linki.
    * Klõpsake loodud tootmistellimuse numbri linki. Avaneb leht tellimuse üksikasjade kohta.  
2. Klõpsake nuppu Redigeeri.
3. Sisestage tarnekuupäev väljale Tarne.
    * Näiteks saate muuta tootmistellimuse tarnekuupäeva.  
4. Klõpsake nuppu Salvesta.
5. Sulgege leht.

## <a name="update-the-bom"></a>Koosluse värskendus
1. Klõpsake toimingupaanil valikut Tootmistellimus.
2. Klõpsake valikut Kooslus.
    * Tootmistellimuse loomisel kopeeritud koosluse vaikeandmete kinnitamiseks avage leht Kooslus. Selles protseduuris peate koosluse kogust uuendama.  
3. Klõpsake nuppu Redigeeri.
4. Sisestage arv väljale Kogus.
    * Koguse muutmine koosluse real mõjutab tootmistellimuse materjalitarbimise kuluhinnangut.  
5. Klõpsake nuppu Salvesta.
6. Sulgege leht.

## <a name="update-the-production-route"></a>Tootmisprotsessi värskendus
1. Klõpsake toimingupaanil valikut Tootmistellimus.
2. Klõpsake valikut Protsess.
    * Tellimuse loomisel kopeeritud tootmisprotsessi vaikeandmete kinnitamiseks avage leht Protsess. Selles protseduuris peaksite uuendama ühe tootmisprotsessi operatsioonide kogust.  
3. Otsige loendist ja valige soovitud kirje.
4. Klõpsake nuppu Redigeeri.
5. Sisestage arv väljale Protsessi kogus.
    * Töötlusaja muutmine mõjutab hinnangulist protsessi tarbimist ja tootmistellimuse kulu.  
6. Klõpsake nuppu Salvesta.
7. Sulgege leht.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]