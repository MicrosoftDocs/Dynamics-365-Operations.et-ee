---
title: Ülesannete haldamine
description: See artikkel selgitab, kuidas microsofti ülesannete halduses ülesandeid häälestada Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2022-06-09
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6a38cc2e36c24ddbfe0d8b2886301c108599ab25
ms.sourcegitcommit: 55e440e30490b2d36d86b22aa1263d5da97633aa
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/04/2022
ms.locfileid: "9745419"
---
# <a name="set-up-tasks-in-task-management"></a>Ülesannete haldamine

[!INCLUDE [PEAP](../includes/peap-1.md)]

Microsoft versioonides enne Dynamics 365 Human Resources versiooni 10.0.30 pidi kasutaja, kes soovis ülesannet redigeerida, seda ülesannet iga kontroll-loendi kohta eraldi redigeerima. Kuid vastavalt inimressursside versioonile 10.0.30 saavad kasutajad valida, kuidas redigeeritud ülesandeid käsitsetakse. Kui redigeeriv ülesanne **on** **kontroll**-loendis, **peab** redigeeritud ülesande kasutamiseks kontroll-loendi lubamiseks olema valitud inimressursside jagatud parameetrite lehe vahekaardil Ülesandehaldus suvand Luba ülesannete halduse täiendamine.

[![Lubab ülesandehalduse täienduse suvandi inimressursside ühiskasutusega parameetrite lehel.](./media/task-update.png)](./media/task-update.png)

Kui ülesannete redigeerimisi tuleb rakendada kõikidele seostatud kontroll-loendi ülesannetele, peab seos ülesandeteegis oleva ülesande ja kontroll-loendi ülesande vahel juba olemas olema. Valik lisati teegi ülesande ja kontroll-loendi ülesande vahelise seose loomiseks.

Saate ülesandeid luua ükshaaval ja seejärel taaskasutada neid mitmes kontroll-loendis. Ülesande loomiseks tehke lehel Põhiseadistus vahekaardil Ülesanded valik **Uus**.**·** **·**

## <a name="set-up-tasks"></a>Saate häälestada ülesandeid.

Loodud ülesande määramiseks mitmele kontroll-loendile valige ülesanne ja seejärel valige menüü **kontroll-loenditele** rakendamine.

Võite ülesandeid lisada ka otse kontroll-loendisse. Ülesande lisamiseks kontroll-loendile, **·** **on sisseostmise seadistuse lehel vahekaardil Kontroll-loend** looge uus kontroll-loend ülesande lisamiseks või lisage ülesanne olemasolevasse kontroll-loendisse.

Teegi ülesande redigeerimiseks valige ülesandeteegi **menüüst** käsk Redigeeri. Kui ülesanne on seotud mis tahes kontroll-loendiga, kuvatakse need kontroll-loendid lehel Ülesande **redigeerimine**. Kui soovite kontroll-loendite ülesandeid uuendada redigeerimistega, **valige need kontroll-loendid jaotises Rakenda kontroll-loenditele**.

Ülesannete kustutamiseks ülesandeteegist valige **kustuta**. Kui ülesanne on seotud kontroll-loendiga, ei kustutata seda toimingut kontroll-loendist. Ülesande eemaldamiseks kontroll-loendist on vaja eraldi toimingut.

### <a name="set-up-checklists"></a>Saate häälestada kontroll-loendeid.

Kontroll-loend on ülesannete grupp. Saate luua nii palju kontroll-loendeid, kui vaja ja saate määrata samad ülesanded mitmele kontroll-loendile. Kontroll-loendi loomisel määrate omaniku ja kalendri.

Uue ülesande loomiseks kontroll-loendis valige ülesande **menüüribalt** uus. Uue ülesande loomisel saate valikuliselt lisada ülesande ülesandeteeki, nii et seda saab jagada mitme kontroll-loendi vahel. Ülesande lisamiseks ülesandeteeki peate häälestama **suvandi Rakenda ülesanne teegile väärtusele** **Jah**. Kui valite ülesande lisamise ülesandeteeki, saate ülesande lisada samal ajal ka teistele kontroll-loenditele, **valides need kontroll-loendid jaotises Rakenda kontroll-loenditele**. Kui otsustate, et ei soovi ülesannet ülesandeteeki lisada, on see ülesanne olemas ainult selle loomisel kontroll-loendis.

Tööülesande redigeerimiseks kontroll-loendis valige menüü **Ülesanne** käsk Redigeeri. Kui ülesanne on seotud mis tahes kontroll-loendiga, kuvatakse need kontroll-loendid lehel Ülesande **redigeerimine**. Kui soovite kontroll-loendite ülesandeid uuendada redigeerimistega, **valige need kontroll-loendid jaotises Rakenda kontroll-loenditele**.

Ülesannete eemaldamiseks kontroll-loendist valige käsk **Eemalda**. See toiming eemaldab ülesanded kontroll-loendist. Kuid see ei kustuta tööülesandeid ülesandeteegist. Ülesannete kustutamiseks ülesandeteegist avage ülesandeteegi **leht ja** valige käsk **Kustuta**.
