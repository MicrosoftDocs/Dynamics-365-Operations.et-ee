---
title: Tööta töötajad
description: Töötajad, kellel puudub tulevane, aktiivne või ajalooline töösuhe teie organisatsioonis, ilmuvad vormile Töötajad ilma töösuheteta.
author: andreabichsel
ms.date: 04/06/2021
ms.topic: ''
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorkerV2, HRMMassHireProject, HRMMassHireLine, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-04-06
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f6fbada6feb55b8627b1aa1ddfe367177edb7a0a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051709"
---
# <a name="workers-without-employment"></a>Tööta töötajad

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Töötajad, kellel puudub tulevane, aktiivne või ajalooline töösuhe teie organisatsioonis, ilmuvad vormile **Töötajad ilma töösuheteta**. Selle olekuga töötajad võivad ilmuda siis, kui impordite ilma töökirjeta töötajaid või kui kustutate töötaja tööhõive jaotises **Töötajad > Tööhõive ajalugu**.

Vaikimisi on vorm **Tööhõiveta töötajad** saadaval järgmistele rollidele.

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

   [![Filtreerige privileegide loendit](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)

3. Valige veerus **Viited** suvand **Kuvamenüü üksused**.

4. Valige veerus **Kuvamenüü üksused** suvand **HcmWorkersWithoutEmployment**.

   [![Vali vorm](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)

5. Määrake õigus **Kustuta** olekusse **Luba**.

6. Valige vahekaart **Avaldamata objektid**.

7. Valige **Avalda kõik**.

   [![Avalda muudatused](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]