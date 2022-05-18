---
title: Hankija töövoog
description: Muutke hankija teavet ja kasutage töövoogu selle kinnitamiseks.
author: sunfzam
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Vendor
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 1801e3d90bbf80c59bb62329acc593d2c66a179c
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735663"
---
# <a name="vendor-workflow"></a>Hankija töövoog

[!include [banner](../includes/banner.md)]

Hankija töövoogu kasutades saadetakse konkreetsetes väljades tehtud muudatused enne hankijale lisamist kinnitamiseks töövoogu.

## <a name="set-up-the-vendor-workflow"></a>Hankija töövoo seadistamine

Enne kui saate töövoo funktsiooni kasutada, peate selle lubama.

1. Avage **Ostureskontro \> Seadistus \> Ostureskontro parameetrid**.
2. Määrake vahekaardil **Üldine** kiirkaardil **Hankija kinnitus** suvandi **Hankija kinnituste lubamine** väärtuseks **Jah**.
3. Valige väljast **Andmeüksuse käitumine** käitumine, mida tuleks andmete importimisel kasutada.

    - **Luba muudatused ilma kinnitamata** – andmeüksus saab hankijakirjet uuendada ilma seda läbi töövoo töötlemata.
    - **Hülga muudatused** – hankijakirjet ei saa muuta. Import nurjub väljade puhul, mis on töövoos lubatud.
    - **Loo muudatusettepanekud** – muudetakse kõiki välju peale töövoos lubatud väljade. Nende väljade uued väärtused lisatakse hankijale pakutud muudatustena ja töövoog käivitatakse automaatselt.

4. Valige hankija väljade loendist märkeruut **Luba** iga välja kohta, mis tuleb enne muudatuste tegemist kinnitada.
5. Avage **Ostureskontro \> Seadistus \> Ostureskontro töövood**.
6. Valige **Uus**.
7. Valige **Pakutud hankijamuudatuste töövoog**. 
8. Seadistage töövoog nii, et see ühtiks teie kinnitusprotsessiga. Töövoo kinnitamise element **Töövoo kinnitus pakutud hankijamuudatuse jaoks** rakendab muudatused hankijale.

## <a name="change-vendor-information-and-submit-the-changes-to-the-workflow"></a>Hankijateabe muutmine ja muudatuste kinnitamine töövoogu

Kui muudate välja, mis on töövoo jaoks lubatud, ilmub leht **Pakutud muudatused**. Sellel lehel kuvatakse välja algväärtus ning uus väärtus, mille sisestasite. Muudetud väljal taastatakse algne väärtus. Olekuteade teavitab teid, et teie muudatusi ei kinnitatud. 

Iga kord kui muudate välja, mis on töövoos lubatud, lisatakse see väli loendisse lehel **Pakutud muudatused**. Välja pakutud muudatuse tühistamiseks kasutage nuppu **Hülga** välja kõrval loendis. Kõikide muudatuste hülgamiseks kasutage nuppu **Hülga kõik muudatused** lehe allosas. Lehe sulgemiseks valige **OK**.

Kui teil on vähemalt üks pakutud muudatus, ilmuvad tegumiribale kaks täiendavat vahekaarti: **Pakutud muudatused** ja **Töövoog**.

1. Valige vahekaart **Pakutud muudatused**, et avada leht **Pakutud muudatused** ja muudatused üle vaadata.
2. Valige suvandid **Töövoog \> Edasta, et edastada muudatused töövoogu**.

    Lehel on olekuks nüüd **Kinnitamise ootel muudatused**.

Töövoog järgib standardset töövooprotsessi. Kinnitaja suunatakse lehele **Hankija**, kus ta saab üle vaadata muudatused lehel **Pakutud muudatused** ja seejärel valida töövoo kinnitamiseks suvandid **Töövoog \> Kinnita**. Kui kõik kinnitamised on lõpule viidud, värskendatakse väljasid teie pakutud muudatustega.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
