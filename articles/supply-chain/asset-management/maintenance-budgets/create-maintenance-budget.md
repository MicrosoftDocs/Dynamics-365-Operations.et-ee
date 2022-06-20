---
title: Hoolduseelarvete loomine
description: See artikkel selgitab, kuidas luua varahalduses hoolduseelarvet.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetBudgetLineAdjust, EntAssetBudget, EntAssetBudgetRecalc, EntAssetBudgetCopy, EntAssetBudgetLine, EntAssetBudgetCreate, EntAssetBudgetApprove, EntAssetBudgetCalculateActualCost
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1fa5e4c76621634930206c1d89fd8e8f4f541fd5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858036"
---
# <a name="create-maintenance-budgets"></a>Hoolduseelarvete loomine

[!include [banner](../../includes/banner.md)]

 



Hoolduseelarveid kasutatakse, et tagada ülevaade ennetava hoolduse eeldatavatest kuludest. Eelarveread arvutatakse nende hooldusgraafiku ridade põhjal, mille eeldatav alguskuupäev on eelarveperioodi jooksul.

Hoolduseelarved põhinevad kulutüüpidel, mida kasutatakse varahalduses: **Ennetav**, **Parandav** ja **Investeering**. Eelarvekulud investeeringu hoolduseks on kaasatud aktiivsete varade jaoks, millel on asenduskuupäev eelarveperioodi jooksul ja seotud asendusväärtus. Eelarvekulud parandava hoolduse jaoks on kaasatud, kui eelarve arvutusse on kaasatud varasem parandav kuupäev. Sellisel juhul arvutatakse varasema perioodi parandavad kulud sama tulevase perioodi kohta, mille kohta hoolduseelarvet arvutate.

## <a name="create-a-maintenance-budget"></a>Hoolduseelarve loomine

1. Valige **Varahaldus** \> **Päringud** \> **Hoolduseelarve** \> **Eelarve**.
2. Valige käsk **Loo eelarve**.
3. Väljale **Hoolduseelarve** sisestage eelarve ID.
4. Väljale **Kirjeldus** sisestage kirjeldus.
4. Vahekaardi **Periood** väljadele **Kuupäevast** ja **Kuupäevani** sisestage eelarveperioodi algus- ja lõppkuupäev.
5. Parandavate eelarvekulude kaasamiseks, mis arvutatakse varasema perioodi tegelike kulude põhjal, sisestage väljale **Parandav kuupäevast** perioodi alguskuupäev, mille kohta need kulud peaksid olema kaasatud.
6. Sõltuvalt eelarves nõutavast üksikasjade tasemest seadistage asjakohased suvandid viiel kiirkaardil **Rühmitusalus**.
7. Valige nupp **OK**.
8. Valige **Eelarveread**, et avada leht **Hoolduseelarveread**, kus saate vaadata kõiki eelarveridu, mis on selle perioodi kohta loodud.
9. Eelarve kinnitamiseks valige see lehel **Hoolduseelarved** ja seejärel valige **Kinnita**. Seejärel valige **OK** dialoogiboksis **Kinnita eelarve**. Teie nimi sisestatakse lehe **Hoolduseelarved** väljale **Kinnitaja**.

    > [!NOTE]
    > Pärast hoolduseelarve kinnitamist ei saa te enam uuesti arvutada ega kohandada seotud ridu lehel **Hoolduseelarveread**, ilma kinnitust eemaldamata. Hoolduseelarve kinnituse eemaldamiseks valige see lehel **Hoolduseelarved** ja seejärel valige **Kinnita**. Seejärel valige **OK** dialoogiboksis **Kinnita eelarve**.

![Hoolduse eelarved.](media/01-maintenance-budgets.png)

Samuti saate luua uue hoolduseelarve olemasoleva eelarve kopeerimisega. Lehel **Hoolduseelarved** ja valige eelarve, mida soovite kopeerida, ja seejärel valige **Kopeeri**. See lähenemine on kasulik, kui olete näiteks loonud eelarve ühe kuu kohta ja soovite seda kopeerida teistesse kuudesse.

> [!NOTE]
> Hoolduseelarve arvutab ainult hooldusgraafiku ridadel põhinevad eelarvekulud. Sama perioodi tegelike kulude arvutamiseks saate teha arvutuse lehel **Vara kulu juhtimine**. 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]