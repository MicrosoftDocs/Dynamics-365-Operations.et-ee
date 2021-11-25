---
title: Tööta töötajad
description: Töötajad, kellel puudub tulevane, aktiivne või ajalooline töösuhetes teie organisatsioonis, ilmuvad tööhõiveta töötajate lehel.
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
ms.openlocfilehash: d282c0fac00d6bc410717dd156aef9ffce352c6d
ms.sourcegitcommit: 7e0e2a266d9a9473df72e207554d9bd150e17ce3
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/05/2021
ms.locfileid: "7771286"
---
# <a name="workers-without-employment"></a>Tööta töötajad

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Töötajad, kellel puudub tulevane, aktiivne või ajalooline töö teie organisatsioonis, ilmuvad **tööhõiveta töötajate** lehel. Seda tüüpi töötajad võivad ilmuda siis, kui impordite töötajaid, kellel pole tööhõivekirjet või kui kustutate töötaja töösuhte Töötajate **\> tööhõive ajaloo kaudu**.

Vaikimisi on lehte **·** Töötajad(ad) võimalik kasutada järgmistele rollidele:

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

   [![ Filtreerige privileegide loendit.](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)

3. Valige veerus **Viited** suvand **Kuvamenüü üksused**.

4. Valige veerus **Kuvamenüü üksused** suvand **HcmWorkersWithoutEmployment**.

   [![ Vali vorm.](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)

5. Määrake õigus **Kustuta** olekusse **Luba**.

6. Valige vahekaart **Avaldamata objektid**.

7. Valige **Avalda kõik**.

   [![ Avalda muudatused.](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
