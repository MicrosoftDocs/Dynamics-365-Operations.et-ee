---
title: Avatud lõpuga puhkuse loomine
description: See artikkel selgitab, kuidas Luua Microsoftis avatud lõpuga puhkuse Dynamics 365 Human Resources.
author: twheeloc
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 08231d4139209387c3c76923fafdd2061fceb280
ms.sourcegitcommit: e88ecaccd82afa3a915e41df1d4287d99da6a48a
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/29/2022
ms.locfileid: "9805422"
---
# <a name="create-an-open-ended-leave-of-absence"></a>Avatud lõpuga puhkuse loomine

> [!IMPORTANT]
> Selles artiklis kirjeldatud funktsioon on Microsoft Dynamics saadaval finantside infrastruktuuris osana tulevasest väljalaskest pärast 365 Finantsite väljalaset 10.0.31.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Saate esitada puhkusetaotlused, mis on avatud lõpuga ja vaadata oma puhkusetaotluste olekut Dynamics 365 Human Resources.

## <a name="prerequisites"></a>Eeltingimused

1. Funktsioonihalduse **all** veenduge, et funktsioon **Avatud lõpetatud puhkused** on sisse lülitatud.

    > [!IMPORTANT]
    > Seda funktsiooni ei saa välja lülitada, kui see on sisse lülitatud.

2. Saate luua puhkuse puhkuse tüübi.
3. Sisestage sellised üksikasjad nagu puhkuse tüüp, kirjeldus ja töövoo ID.
4.  **Väljal Taotluse tüüp** valige **puhkus**.
5. Üksikasjade jaotises seadke avatud lõpuga lehtede suvandi Avatud **lõpetatud väärtuseks**  **Jah**.
6. Seadke suvandi **Tööteatise tagastamine** väärtusele **Jah** või **Ei**.
7. Töölt tagasipöördumise teatist saab valikuliselt nõuda avatud lõpuga puudumistaotluste puhul.

> [!NOTE]
> Kui see funktsioon on lubatud, lubatakse **manusele** vajalik funktsioon.

## <a name="request-an-open-ended-leave-of-absence"></a>Avatud lõpuga puhkuse taotlemine

1. Töötaja iseteeninduse **tööruumis** valige paanil **Aja off saldod** suvand **Veel (...).**
2. Puhkusetaotluse esitamiseks valige suvand **Taotle puhkusepuhkust**.
3. Sisestage puhkuse tüüp **ja alguskuupäeva**  **väljadele** teave.  **Väljale Lõppkuupäev** sisestage esialgse lõppkuupäev.
4. Kui peate esitama toetavad dokumendid, valige jaotises **Manused** suvand Laadi **üles**.
5. Kui olete valmis oma taotlust esitama, valige **edastamine**. Muidu valige suvand **Salvesta mustand**.
6. Avatud lõpuga puhkuse taotluse värskendamiseks valige taotlus, **sisestage** lõppkuupäev väljale Lõppkuupäev, **·**  **seadke suvandi Kinnita lõppkuupäev väärtuseks Jah** ja laadige dokumentatsioon üles.
7. Kui suvandi **Töösse tagastamise teatis** väärtuseks **on** seatud Jah, **valige** Üleslaadimine ja märkige seejärel ruut kehtiva töösse tagastamise teate üleslaadimise kinnitamiseks.
8. Kui kõik üksikasjad on sisestatud, valige **Edasta**.
