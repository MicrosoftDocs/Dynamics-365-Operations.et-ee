---
title: Sissetulevad ja väljaminevad varad
description: See artikkel selgitab, kuidas registreerida varahalduses sissetulevaid ja väljaminevaid varasid.
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
ms.openlocfilehash: fd7482cfe943347840e9fb070151d66fbe5ef9ca
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016532"
---
# <a name="inbound-and-outbound-assets"></a>Sissetulevad ja väljaminevad varad

[!include [banner](../../includes/banner.md)]

 

Kui teie ettevõte teeb parandustöid või hooldustöid teistest asukohtadest või klientidelt saadud varadele, saab varahaldus jälgida nii sissetulevaid varasid, mis on teel teie ettevõttesse kui ka tagastatavaid väljaminevaid varasid.

> [!NOTE]
> Kui soovite kasutada sissetulevaid ja väljaminevaid elutsükli olekuid, et hallata varasid, mis tulevad sisse ja mis tagastatakse, peate seadistama hoolduse taotluse elutsükli olekud ja elutsükli mudelid nende toimingute toetamiseks. Lisateavet uute tarnijate nõuete kohta vt [Hooldusnõuded](/d365F-O/supply-chain/asset-management/manage-maintenance-requests/../manage-maintenance-requests/maintenance-request-overview).

’Varahalduse häälestus määratleb, kas saate töötada sissetulevate ja väljaminevate põhivaradega.

## <a name="register-assets-as-inbound"></a>Registreeri varad sissetulevatena

1. Valige **varahalduse hooldustaotlused** \> **aktiivse** \> **hoolduse taotlused**.
2. Valige hooldustaotlus.
3. Valige **Uuenda hooldustaotluse olekut**.
4. Valige **Sissetulev** (või mõni muu elutsükli olek, mille olete sissetulevate varade jaoks loonud) ja seejärel valige **OK**.

![Registreeri varad sissetulevatena.](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a>Registreeri varad vastuvõetuna

1. Valige **Varahalduse** \> **sissetulevad/väljaminevad** \> **sissetulevad varad**.
2. Saate valida vara või hooldustaotluse.
3. Valige **Varade vastuvõtmine**.
4. Väljale **Vastuvõetud** sisestage kuupäev ja kellaaeg. Seejärel valige **OK**. Kirje eemaldatakse loendilehelt **Sissetulevad varad**.

![Registreeri varad vastuvõetuna.](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a>Registreeri varad sissetulekuna

Hoolduse või parandustöö lõpule viimise korral saate vara registreerida kui tagastatud.

1. Valige **varahalduse hooldustaotlused** \> **aktiivse** \> **hoolduse taotlused**.
2. Valige hooldustaotlus.
3. Valige **Uuenda hooldustaotluse olekut**.
4. Valige **Väljaminev** (või mõni muu elutsükli olek, mille olete väljaminevate varade jaoks loonud) ja seejärel valige **OK**.

## <a name="register-outbound-assets-as-delivered"></a>Registreeri varad kui tarnitud.

1. Valige **varahalduse** \> **sissetulevad/väljaminevad väljaminevad** \> **varad.**
2. Saate valida vara või hooldustaotluse.
3. Valige **Varade kohaletoimetus**.
4. Väljale **Kohale toimetatud** sisestage kuupäev ja kellaaeg. Seejärel valige **OK**. Kirje eemaldatakse loendilehelt **Väljaminev varad**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]