---
title: Kinni jäänud pakett-tööde lähtestamine
description: See artikkel selgitab, kuidas lahendada probleemid kinni jäänud pakett-töödega.
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
ms.openlocfilehash: b56a16257a45dd093d10b7550b13d6a4a1ceb1f7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896014"
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
