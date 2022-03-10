---
title: Kinni jäänud pakett-tööde lähtestamine
description: See teema kirjeldab, kuidas lahendada probleemid pakett-töödega, mis on kinni jäänud.
author: andreabichsel
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: 859f039a928cdc57c9f227885d0f00ef79980f28
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070396"
---
# <a name="reset-stuck-batch-jobs"></a>Kinni jäänud pakett-tööde lähtestamine


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a>Väljasta

Microsoft Dynamics 365 Human Resources -il võib tekkida probleeme pakett-töödega, mis on jäänud kinni kas **Teostamise** või **Tühistamise** olekusee ja mida ei saa lõpule viia.

## <a name="resolution"></a>Eraldusvõime

Kui pakett-töö on jäänud kinni **Teostamise** või **Tühistamise** olekusse, saate oleku lähtestada, käivitades töö tühistamise. Pärast selle tühistamine saate lähtestada pakett-töö, seadistades selle olekusse **Ootel**. Seejärel korjatakse see jälle üles, et läbiviia järjekordne planeeritud pakett-töö käivitus.

1. **Süsteemihalduse** tööruumis valige leht **Lingid** ja valige **Pakett-tööd**.

2. **Pakett-töö** loendilehel valige töö, mida on vaja lähtestada.

3. Toiminguribal valige **Sundtühista** ja kinnita tühistamine.

   > [!NOTE]
   > **Sundtühista** käsk on kättesaadav kui valitud pakett-töö staatus on kas **Käivitamine** või **Tühistamine** ja ühtki paketi käivitamise või tühistamise protsessi ei käitata töö jaoks.

4. Tegevusribal vali **Muuda olekut**.

5. Lehel **Vali uus olek** valige **Ootamine** ja seejärel valige **OK**.

   ![Valige uus pakett-töö olek.](./media/hr-admin-reset-batch-job-status.png)

## <a name="see-also"></a>Vt ka

[Jõudluse optimeerimine pakett-tööde planeerimisel pärast tööaega](hr-admin-troubleshooting-batch-jobs.md)<br>
[Jõudluse optimeerimine automaatsete puhastamisülesannetega](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
