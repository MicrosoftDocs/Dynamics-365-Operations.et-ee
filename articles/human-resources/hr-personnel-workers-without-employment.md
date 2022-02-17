---
title: Tööta töötajad
description: Töötajad, kellel ei ole teie organisatsiooniga tulevast, aktiivset ega ajaloolist tööd, kuvatakse lehel Töötajad ilma tööta.
author: twheeloc
ms.date: 11/03/2021
ms.topic: ''
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorkerV2, HRMMassHireProject, HRMMassHireLine, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-04-06
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d0b8fe7dd0818fa1c3cc4224e73035849f9dadfe
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070547"
---
# <a name="workers-without-employment"></a>Tööta töötajad


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Töötajad, kellel ei ole teie organisatsiooniga tulevast, aktiivset ega ajaloolist **tööd, kuvatakse lehel Tööta** töötajad. Seda tüüpi töötajad võivad ilmuda siis, kui impordite töötajaid, kellel pole töökirjet, või kui kustutate töötaja töö töötajate **tööhõive ajaloo kaudu \>**.

Vaikimisi **on leht Tööta töötajad** saadaval järgmistele rollidele.

- Inimressursside assistent
- Inimressursside haldur
- Värbaja
- Hüvitise ja eeliste haldur
- Palgaarvestuse administraator
- Palgaarvestuse haldur
- Koolitusjuht

Loendis **Töötajad ilma töösuheteta** saate loetletud isikud kustutada. Vaikimisi on see privileeg antud Inimressursside abilise rollile. Saate selle privileegi järgmiste sammudega anda teistele rollidele.

1. Valige suvand **Süsteemihaldus** ja seejärel valige suvand **Turbekonfiguratsioon**.

2. Vahekaardil **Privileegid** filtreerige loendit **Privileegid** suvandi **Töötajate haldamine** alusel.

   [![Filtreerige privileegide loendit.](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)

3. Valige veerus **Viited** suvand **Kuvamenüü üksused**.

4. Valige veerus **Kuvamenüü üksused** suvand **HcmWorkersWithoutEmployment**.

   [![Vali vorm.](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)

5. Määrake õigus **Kustuta** olekusse **Luba**.

6. Valige vahekaart **Avaldamata objektid**.

7. Valige **Avalda kõik**.

   [![Avalda muudatused.](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
