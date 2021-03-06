---
title: Turbediagnostika ülesande salvestiste jaoks
description: Selles teemas jagatakse teavet selle kohta, kuidas analüüsida ja hallata tegevuse salvestise põhjal turvaõiguste nõudeid.
author: Peakerbl
ms.date: 05/05/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: ''
ms.dyn365.ops.version: Version 10.0.9
ms.openlocfilehash: cb4d544d8d74ad10432901381253f84ec9331ae7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745761"
---
# <a name="security-diagnostics-for-task-recordings"></a>Turbediagnostika ülesande salvestiste jaoks

[!include [banner](../../includes/banner.md)]

## <a name="before-you-begin"></a>Enne alustamist

Selles teemas jagatakse teavet selle kohta, kuidas analüüsida ja hallata tegevuse salvestise põhjal turvaõiguste nõudeid. Enne teemas toodud etappide täitmist peab teil olema selle äriprotsessi tegevuse salvestis, mida soovite analüüsida. Äriprotsessi salvestamiseks vt teemat [Tegevuse salvestaja vahendid](../../user-interface/task-recorder.md). 

## <a name="manage-security-for-a-task-recording"></a>Tegevuse salvestise turvalisuse haldamine

1. Avage **Süsteemihaldus** > **Turve** > **Tegevuse salvestise turbediagnostika**.
2. Avage tegevuse salvestis selle asukohas. Valige **Ava sellest arvutist** või **Ava rakendusest Lifecycle Services** ja seejärel valige **Sulge**.
3. See avab lehe **Turbemenüü käsu üksikasjad**, kus on loetletud protsessi jaoks nõutud turbeobjektid.

 > [!NOTE]
 > Loetelu ei hõlma menüükäske **Tegevus** ja **Väljund**.

4. Valige kasutaja väljal **Kasutaja ID**. Kui kasutajal puudub mõne menüükäsu kohta luba, siis uuendatakse välja **Puuduvad load** väärtuseks **Jah**.
  
  ![Turbemenüü käsu üksikasjade leht](../media/Security-Menu-Item-Details.png)

5. Valige suvand **Lisa viide**, et näha turbeobjektide loetelu, sealhulgas rollid, kohustused ja privileegid, mis tagavad puuduva loa.
6. Valige loendist turbeobjekt.

    - Kui **Roll** on valitud, siis valige **Lisa kasutajale roll**. See avab lehe **Määra rollidele kasutajaid**. Lisainfo saamiseks vt lehte [Kasutajatele turberollide määramine](assign-users-security-roles.md).
    - Kui **Kohustus** on valitud, siis valige **Lisa rollile kohustus**, valige rollid, millele tuleks kohustus lisada ning seejärel valige **OK**.
    - Kui **Privileeg** on valitud, siis valige **Lisa kohustustele privileeg**, valige rollid, millele tuleks kohustus lisada ning seejärel valige **OK**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]