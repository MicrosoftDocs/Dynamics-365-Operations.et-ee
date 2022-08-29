---
title: Turbediagnostika ülesande salvestiste jaoks
description: See artikkel annab teavet, kuidas analüüsida ja hallata ülesannete salvestamisel põhinevaid turbeõiguse nõudeid.
author: Peakerbl
ms.date: 05/05/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: ''
ms.dyn365.ops.version: Version 10.0.9
ms.search.form: ''
ms.openlocfilehash: e564a0499cb1a5dc00fc027c20a027f9b454600c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272516"
---
# <a name="security-diagnostics-for-task-recordings"></a>Turbediagnostika ülesande salvestiste jaoks

[!include [banner](../../includes/banner.md)]

## <a name="before-you-begin"></a>Enne alustamist

See artikkel annab teavet, kuidas analüüsida ja hallata ülesannete salvestamisel põhinevaid turbeõiguse nõudeid. Enne selle artikli sammude lõpule viimist peab teil olema ülesande salvestamine äriprotsessile, mida soovite analüüsida. Äriprotsessi salvestamiseks vt teemat [Tegevuse salvestaja vahendid](../../user-interface/task-recorder.md). 

## <a name="manage-security-for-a-task-recording"></a>Tegevuse salvestise turvalisuse haldamine

1. Avage **Süsteemihaldus** > **Turve** > **Tegevuse salvestise turbediagnostika**.
2. Avage tegevuse salvestis selle asukohas. Valige **Ava sellest arvutist** või **Ava rakendusest Lifecycle Services** ja seejärel valige **Sulge**.
3. See avab lehe **Turbemenüü käsu üksikasjad**, kus on loetletud protsessi jaoks nõutud turbeobjektid.

 > [!NOTE]
 > Loetelu ei hõlma menüükäske **Tegevus** ja **Väljund**.

4. Valige kasutaja väljal **Kasutaja ID**. Kui kasutajal puudub mõne menüükäsu kohta luba, siis uuendatakse välja **Puuduvad load** väärtuseks **Jah**.
  
  ![Turbemenüü käsu üksikasjade leht.](../media/Security-Menu-Item-Details.png)

5. Valige suvand **Lisa viide**, et näha turbeobjektide loetelu, sealhulgas rollid, kohustused ja privileegid, mis tagavad puuduva loa.
6. Valige loendist turbeobjekt.

    - Kui **Roll** on valitud, siis valige **Lisa kasutajale roll**. See avab lehe **Määra rollidele kasutajaid**. Lisainfo saamiseks vt lehte [Kasutajatele turberollide määramine](assign-users-security-roles.md).
    - Kui **Kohustus** on valitud, siis valige **Lisa rollile kohustus**, valige rollid, millele tuleks kohustus lisada ning seejärel valige **OK**.
    - Kui **Privileeg** on valitud, siis valige **Lisa kohustustele privileeg**, valige rollid, millele tuleks kohustus lisada ning seejärel valige **OK**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
