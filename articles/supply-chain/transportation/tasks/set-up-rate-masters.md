---
title: Määrade koondandmete seadistamine
description: See protseduur näitab, kuidas seadistada koondmäära.
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 462bfce89fa77c8830a93a22b0dd6c8c8fb2cde6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555302"
---
# <a name="set-up-rate-masters"></a>Määrade koondandmete seadistamine

[!include [task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab, kuidas seadistada koondmäära. Koondmäärad seadistab üldjuhul logistikahaldur vedajatega allkirjastatud lepingutest olenevalt. Sel juhul saate seadistada koondmäära lennukompanii puhul. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.


## <a name="set-up-rate-master"></a>Koondmäära seadistamine
1. Avage Transpordihaldus > Seadistus > Hinnang > Koondmäär.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Koondmäär.
4. Sisestage väärtus väljale Nimi.
5. Klõpsake väljal Hindamise metaandmete ID otsingu avamiseks ripploendi nuppu.
    * Hinnangu metaandmete ID määratleb koondmäära puhul vajalikud andmed, nagu see määratleb TMS-i mootori eeldatavad metaandmed seda koondmäära kasutades.  
6. Selle näite puhul valige suvand P2P
7. Klõpsake loendis valitud real olevat linki.
8. Klõpsake nuppu Salvesta.

## <a name="set-up-rate-base"></a>Alusmäära seadistamine
1. Klõpsake suvandit Alusmäär.
    * Alusmäär määratleb vedaja määra ja seda saab kasutada tariifi struktuuri seadistamiseks, nagu see struktuurib määrasid katkestuse koondandmete määratletud katkestuspunktides.  
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Alusmäär.
4. Sisestage väärtus väljale Nimi.
5. Klõpsake väljal Katkestuse koondandmed otsingu avamiseks ripploendi nuppu.
    * Katkestuse koondandmeid kasutatakse hinnakujunduse struktuuri ja selle katkestuspunktide määratlemiseks. Hinnakujunduse struktuur kasutab mitmetasandilist hinnakujundust, mis põhineb füüsilistel dimensioonidel.  
6. Selle näite puhul kasutage kaalu
7. Klõpsake loendis valitud real olevat linki.
8. Laiendage jaotist Üksikasjad.
9. Klõpsake Uus.
10. Sisestage väljale Kohaleviimise saatja sihtnumber väärtus 30301.
11. Sisestage väljale Kohaleviimise saaja sihtnumber väärtus 30318.
12. Sisestage väljale Kohaleviimise riik/regioon suvand USA.
13. Sisestage väljale <1,00 naela väärtus 100.
    * Sisestage määr naela kohta, kui koorma kogukaal on alla 1 naela.  
14. Sisestage väljale <5,00 naela väärtus 300.
    * Sisestage määr naela kohta, kui koorma kogukaal on alla 5 naela.  
15. Sisestage väljale <20,00 naela väärtus 500.
    * Sisestage määr naela kohta, kui koorma kogukaal on alla 20 naela.  
16. Sisestage väljale <100,00 naela väärtus 1000.
    * Sisestage määr naela kohta, kui koorma kogukaal on alla 100 naela.  
17. Sisestage väljale <1000,00 naela väärtus 3000.
    * Sisestage määr naela kohta, kui koorma kogukaal on alla 1000 naela.  
18. Klõpsake nuppu Salvesta.
19. Sulgege leht.

## <a name="assign-rate-base"></a>Alusmäära määramine
1. Laiendage jaotist Alusmäära määrangud.
2. Klõpsake valikut Uus.
    * Teil võib iga määra koondandme puhul olla mitu alusmäära määramist. See võimaldab luua mitu erinevat hinnaühtlustuspunkti iga vedaja puhul olenevalt sihtkohtadest, teenustest või erinevatest alusmääradest. Selles protseduuris loote ainult ühe alusmäära määramise.  
3. Sisestage väärtus väljale Nimi.
4. Klõpsake väljal Alusmäär otsingu avamiseks ripploendi nuppu.
5. Klõpsake loendis valitud real olevat linki.
6. Klõpsake väljal Teenus otsingu avamiseks ripploendi nuppu.
7. Otsige loendist ja valige soovitud kirje.
8. Klõpsake loendis valitud real olevat linki.
9. Sisestage väljale Pealevõtmise postiindeks väärtus 98052.
    * Määrake, milline sihtnumber peaks selle alusmäära määramise puhul kehtima.    
10. Sisestage väljale Pealevõtmise riik/regioon suvand USA.
11. Klõpsake nuppu Salvesta.

