---
title: Kinni jäänud pakett-tööde lähtestamine
description: See teema kirjeldab, kuidas lahendada probleemid pakett-töödega, mis on kinni jäänud.
author: twheeloc
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: 2602bd954daac563cbc50810c6fe0d79dc71a62b
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8694987"
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
