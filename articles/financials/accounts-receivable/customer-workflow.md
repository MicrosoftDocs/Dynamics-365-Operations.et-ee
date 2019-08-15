---
title: Kliendi töövoog
description: Selles teemas kirjeldatakse kliendi töövoogu. Saate muuta kliendi teatud välju ja saata need muudatused töövoo abil kinnitamiseks, enne kui need lisatakse kliendile.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 10149351d548ab63b9d765ce34afd5908e43e12f
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835066"
---
# <a name="customer-workflow"></a>Kliendi töövoog

[!include [banner](../includes/banner.md)]

Kliendi töövoog lisati teenuse Microsoft Dynamics 365 for Finance and Operations versiooni 8.0.4. Saate muuta kliendi teatud välju ja saata need muudatused töövoo abil kinnitamiseks, enne kui need lisatakse kliendile.

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

Töövoog järgib rakenduses Finance and Operations standardset töövooprotsessi. Kinnitaja suunatakse lehele **Klient**, kus ta saab lehel **Pakutud muudatused** tehtud muudatused üle vaadata ja seejärel valida **Töövoog \> Kinnita**, et kinnitada töövoog. Kui kõik kinnitamised on lõpule viidud, värskendatakse väljasid teie pakutud muudatustega.
