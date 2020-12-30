---
title: Määrade koondandmete seadistamine
description: See protseduur näitab, kuidas seadistada koondmäära.
author: ShylaThompson
manager: tfehr
ms.date: 10/16/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSBreakMaster,TMSRateMaster,TMSRateMasterBase,TMSRateBaseType, TMSRouteWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b4cca9fd47a5d8c81d7b8a913d0a467bc113b584
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/29/2020
ms.locfileid: "4426720"
---
# <a name="set-up-rate-masters"></a>Määrade koondandmete seadistamine

[!include [banner](../../includes/banner.md)]

See protseduur näitab, kuidas seadistada koondmäära. Koondmäärad seadistab üldjuhul logistikahaldur vedajatega allkirjastatud lepingutest olenevalt. Sel juhul saate seadistada koondmäära lennukompanii puhul. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.

## <a name="set-up-break-master"></a>Katkestuse koondandmete seadistamine

1. Avage **Transpordihaldus > Seadistus > Hinnang > Katkestuste koondandmed**. Katkestuse koondandmeid kasutatakse hinnakujunduse struktuuri ja selle katkestuspunktide määratlemiseks. Hinnakujunduse struktuur kasutab mitmetasandilist hinnakujundust, mis põhineb füüsilistel dimensioonidel.  
1. Valige suvand **Uus**.
1. Sisestage väärtus väljal **Katkestuse koondandmed**.
1. Sisestage väärtus väljale **Nimi**.
1. Valige **Andmetüüp** väljal andmetüüp.
1. Sisestage väljale **Võrdlus** taotletud võrdluse tüüp (kasutades tehtemärke).
1. Sisestage **Katkestuse ühik** väljale katkestuse ühiku väärtused.
1. Looge **Üksikasjad** jaotises nii palju katkestusi, kui on vaja hinnakujunduse struktuuri jaoks.
1. Valige käsk **Salvesta**.

## <a name="set-up-rate-master"></a>Koondmäära seadistamine

1. Avage **Transpordihaldus > Seadistus > Hinnang > Hinnangu koondandmed**.
1. Valige suvand **Uus**.
1. Sisestage väärtus väljale **Hinnangu koondandmed**.
1. Sisestage väärtus väljale **Nimi**.
1. Valige **Meta-andmete ID hindamine** väljal otsingu avamiseks ripploendi nuppu. Hinnangu meta-andmete ID määratleb koondmäära puhul vajalikud andmed, nagu see määratleb transpordihalduse mootori eeldatavad metaandmed seda koondmäära kasutades.  
1. Selle näite puhul valige suvand P2P. See on juba demo andmetega määratletud.
1. Valige loendis link valitud reas.
1. Valige käsk **Salvesta**.

## <a name="set-up-rate-base"></a>Alusmäära seadistamine

1. Valige **Hinnangu alus**.
    * Alusmäär määratleb vedaja määra ja seda saab kasutada tariifi struktuuri seadistamiseks, nagu see struktuurib määrasid katkestuse koondandmete määratletud katkestuspunktides.  
2. Valige suvand **Uus**.
3. Sisestage **Hinnangu alus** väljale väärtus.
4. Sisestage väärtus väljale **Nimi**.
5. Valige **Katkestuse koondandmed** väljal otsingu avamiseks ripploendi nuppu.
    * Katkestuse koondandmeid kasutatakse hinnakujunduse struktuuri ja selle katkestuspunktide määratlemiseks. Hinnakujunduse struktuur kasutab mitmetasandilist hinnakujundust, mis põhineb füüsilistel dimensioonidel.  
6. Selle näite puhul kasutage kaalu. See on juba demo andmetega määratletud.
7. Valige loendis link esiletõstetud reas.
8. Laiendage jaotist **Üksikasjad**.
9. Valige suvand **Uus**.
10. Sisestage **Kohaletoimetamise lähtekoha sihtnumber** väljale väärtus 30301.
11. Sisestage **Kohaletoimetamise sihtkoha sihtnumber** väljale "30318".
12. Sisestage **Kohaletoimetamise riik/regioon** väljale "USA".
13. Sisestage **<1,00 naela** väljale "100".
    * Sisestage määr naela kohta, kui koorma kogukaal on vähem kui 1 nael.  
14. Sisestage **<5,00 naela** väljale "300".
    * Sisestage määr naela kohta, kui koorma kogukaal on kuni 5 naela.  
15. Sisestage **<20,00 naela** väljale "500".
    * Sisestage määr naela kohta, kui koorma kogukaal on kuni 20 naela.  
16. Sisestage **<100,00 naela** väljale "1000".
    * Sisestage määr naela kohta, kui koorma kogukaal on kuni 100 naela.  
17. Sisestage **<1000,00 naela** väljale "3000".
    * Sisestage määr naela kohta, kui koorma kogukaal on kuni 1000 naela.  
18. Valige käsk **Salvesta**.
19. Sulgege leht.

## <a name="assign-rate-base"></a>Alusmäära määramine

1. Laiendage **Alusmäära määramised** jaotist.
2. Valige suvand **Uus**.
    * Teil võib iga määra koondandme puhul olla mitu alusmäära määramist. See võimaldab luua mitu erinevat hinnaühtlustuspunkti iga vedaja puhul olenevalt sihtkohtadest, teenustest või erinevatest alusmääradest. Selles protseduuris loote ainult ühe alusmäära määramise.  
3. Sisestage väärtus väljale **Nimi**.
4. Klõpsake **Alusmäär** väljal otsingu avamiseks ripploendi nuppu.
5. Valige loendis link esiletõstetud reas.
6. Klõpsake väljal **Teenus** otsingu avamiseks ripploendi nuppu.
7. Otsige loendist ja valige soovitud kirje.
8. Valige loendis link esiletõstetud reas.
9. Sisestage väljale **Peale võtmise postiindeks** väärtus "98052".
    * Määrake, milline sihtnumber peaks selle alusmäära määramise puhul kehtima.
10. Sisestage väljale **Peale võtmise riik/regioon** "USA".
11. Valige käsk **Salvesta**.
