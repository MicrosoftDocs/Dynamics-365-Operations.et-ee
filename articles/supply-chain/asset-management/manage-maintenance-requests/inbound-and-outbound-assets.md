---
title: Sissetulevad ja väljaminevad varad
description: Selles teemas kirjeldatakse, kuidas registreerida sissetulevad ja väljaminevad varad varahalduses.
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetOutboundObjectsListPage, EntAssetOutboundObjectsDeliver, EntAssetInboundObjectsListPage, EntAssetInboundObjectsRecieve
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 86d85d280b32834c36691535a019ef6d5141bf93
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6356017"
---
# <a name="inbound-and-outbound-assets"></a>Sissetulevad ja väljaminevad varad

[!include [banner](../../includes/banner.md)]

 

Kui teie ettevõte teeb parandustöid või hooldustöid teistest asukohtadest või klientidelt saadud varadele, saab varahaldus jälgida nii sissetulevaid varasid, mis on teel teie ettevõttesse kui ka tagastatavaid väljaminevaid varasid.

> [!NOTE]
> Kui soovite kasutada sissetulevaid ja väljaminevaid elutsükli olekuid, et hallata varasid, mis tulevad sisse ja mis tagastatakse, peate seadistama hoolduse taotluse elutsükli olekud ja elutsükli mudelid nende toimingute toetamiseks. Lisateavet uute tarnijate nõuete kohta vt [Hooldusnõuded](../setup-for-maintenance-requests/requests.md).

’Varahalduse häälestus määratleb, kas saate töötada sissetulevate ja väljaminevate põhivaradega.

## <a name="register-assets-as-inbound"></a>Registreeri varad sissetulevatena

1. Valige **Varahaldus**\>**Ühised**\>**Hooldustaotlused**\>**Aktiivsed hooldustaotlused**.
2. Valige hooldustaotlus.
3. Valige **Uuenda hooldustaotluse olekut**.
4. Valige **Sissetulev** (või mõni muu elutsükli olek, mille olete sissetulevate varade jaoks loonud) ja seejärel valige **OK**.

![Registreeri varad sissetulevatena.](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a>Registreeri varad vastuvõetuna

1. Valige **Varahaldus**\>**Ühised**\>**Sissetulevad/väljaminevad**\>**Sissetulevad varad**.
2. Saate valida vara või hooldustaotluse.
3. Valige **Varade vastuvõtmine**.
4. Väljale **Vastuvõetud** sisestage kuupäev ja kellaaeg. Seejärel valige **OK**. Kirje eemaldatakse loendilehelt **Sissetulevad varad**.

![Registreeri varad vastuvõetuna.](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a>Registreeri varad sissetulekuna

Hoolduse või parandustöö lõpule viimise korral saate vara registreerida kui tagastatud.

1. Valige **Varahaldus**\>**Ühised**\>**Hooldustaotlused**\>**Aktiivsed hooldustaotlused**.
2. Valige hooldustaotlus.
3. Valige **Uuenda hooldustaotluse olekut**.
4. Valige **Väljaminev** (või mõni muu elutsükli olek, mille olete väljaminevate varade jaoks loonud) ja seejärel valige **OK**.

## <a name="register-outbound-assets-as-delivered"></a>Registreeri varad kui tarnitud.

1. Valige **Varahaldus**\>**Ühised**\>**Sissetulevad/väljaminevad**\>**Väljaminevad varad**.
2. Saate valida vara või hooldustaotluse.
3. Valige **Varade kohaletoimetus**.
4. Väljale **Kohale toimetatud** sisestage kuupäev ja kellaaeg. Seejärel valige **OK**. Kirje eemaldatakse loendilehelt **Väljaminev varad**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]