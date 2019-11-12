---
title: Hoolduseelarvete loomine
description: Selles teemas tutvustatakse, kuidas luua hoolduseelarvet varahalduses.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 99f76c684150f154404cbb241daacb7a8d05f7f9
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571756"
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

![Hoolduseelarved](media/01-maintenance-budgets.png)

Samuti saate luua uue hoolduseelarve olemasoleva eelarve kopeerimisega. Lehel **Hoolduseelarved** ja valige eelarve, mida soovite kopeerida, ja seejärel valige **Kopeeri**. See lähenemine on kasulik, kui olete näiteks loonud eelarve ühe kuu kohta ja soovite seda kopeerida teistesse kuudesse.

> [!NOTE]
> Hoolduseelarve arvutab ainult hooldusgraafiku ridadel põhinevad eelarvekulud. Sama perioodi tegelike kulude arvutamiseks saate teha arvutuse lehel **Vara kulu juhtimine**. 
