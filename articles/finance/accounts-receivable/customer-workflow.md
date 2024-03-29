---
title: Kliendi töövoog
description: Selles artiklis kirjeldatakse kliendi töövoogu. Saate muuta kliendi teatud välju ja saata need muudatused töövoo abil kinnitamiseks, enne kui need lisatakse kliendile.
author: abruer
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 883e77b5480a52201673e58a641c7180009a129c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864421"
---
# <a name="customer-workflow"></a>Kliendi töövoog

[!include [banner](../includes/banner.md)]

Kliendi töövoog lisati versiooni 8.0.4. Saate muuta kliendi teatud välju ja saata need muudatused töövoo abil kinnitamiseks, enne kui need lisatakse kliendile.

## <a name="set-up-the-customer-workflow"></a>Kliendi töövoo häälestamine

Enne kliendi töövoo funktsiooni kasutamist peate selle lubama.

1. Minge jaotisse **Müügireskontro \> Seadistus \> Müügireskontro parameetrid**.
2. Funktsiooni lubamiseks määrake vahekaardi **Üldine** kiirkaardil **Kliendi kinnitus** suvandi **Luba kliendi kinnitused** väärtuseks **Jah**.
3. Väljal **Andmeüksuse käitumine** valige käitumine, mida andmeüksused peaksid kasutama andmete importimisel:

    - **Luba muudatused ilma kinnitamata** – üksus saab värskendada kliendikirjet ilma selle töötlemiseta läbi töövoo.
    - **Hülga muudatused** – kliendikirjele ei saa muudatusi teha. Väljadel, mis on töövoo jaoks lubatud, importimine nurjub.
    - **Loo muudatusettepanekud** – muudetakse kõiki välju peale väljade, mis on töövoo jaoks lubatud. Nende väljade uued väärtused lisatakse kliendile pakutud muudatustena ja töövoog käivitatakse automaatselt.

4. Valige kliendiväljade loendis märkeruut **Luba** iga välja jaoks, mis tuleb enne muudatuste tegemist kinnitada.
5. Minge jaotisse **Müügireskontro \> Seadistus \> Müügireskontro töövood**.
6. Valige **Uus**.
7. Valige **Pakutud kliendimuudatuse töövoog**. 
8. Häälestage töövoog nii, et see ühtiks teie heakskiidu protsessiga. Töövoo kinnitamise element **Töövoo kinnitus pakutud kliendimuudatuse jaoks** rakendab muudatused kliendile.

## <a name="change-customer-information-and-submit-the-changes-to-the-workflow"></a>Klienditeabe muutmine ja muudatuste esitamine töövoole

Kui muudate välja, mis on töövoo jaoks lubatud, kuvatakse leht **Pakutud muudatused**. Sellel lehel kuvatakse välja algväärtus ning uus väärtus, mille sisestasite. Teie muudetud välja väärtus taastatakse algväärtusele. Lehe olekuteade teavitab teid, et muudatusi pole edastatud.

Iga kord, kui muudate välja, mis on töövoo jaoks lubatud, lisatakse see väli pakutud muudatuste loendisse. Välja pakutud väärtuse tühistamiseks kasutage loendis välja kõrval olevat nuppu **Tühista**. Kõigi muudatuste tühistamiseks kasutage lehe allosas olevat nuppu **Tühista kõik muudatused**. Valige lehe sulgemiseks **OK**.

Kui teil on vähemalt üks pakutud muudatus, kuvatakse toimingupaanil kaks uut menüüd: **Pakutud muudatused** ja **Töövoog**.

1. Valige **Pakutud muudatused**, et avada leht **Pakutud muudatused** ja vaadata oma muudatused üle.
2. Valige **Töövoog \> Edasta**, et edastada muudatused töövoogu.

    Lehel on olekuks nüüd **Kinnitamise ootel muudatused**.

Töövoog järgib rakenduses standardset töövooprotsessi. Kinnitaja suunatakse lehele **Klient**, kus ta saab lehel **Pakutud muudatused** tehtud muudatused üle vaadata ja seejärel valida töövoo kinnitamiseks **Töövoog \> Kinnita**. Kui kõik kinnitamised on lõpule viidud, värskendatakse väljasid teie pakutud muudatustega.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
