---
title: Attracti kasutajad ei saa karjääriportaalis töökohtadele kandideerida
description: Selles teemas selgitatakse probleemi tõrkeotsingut, kus Attracti kasutajad ei saa karjääriportaalis töödele kandideerida.
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: e1d72bef6d8bbe15e27326f66341915ba44a09b4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460890"
---
# <a name="attract-users-cant-apply-for-jobs-from-career-portal"></a>Attracti kasutajad ei saa karjääriportaalis töökohtadele kandideerida

[!include [banner](includes/banner.md)]

## <a name="issue"></a>Väljasta

Attracti kasutajad ei saa karjääriportaalis töökohtadele kandideerida. Kui nad proovivad Dynamics 365 Talent: Attractis loodud töökohale kandideerida, siis brauser laadib pidevalt lehte ega vii tegevust lõpule.

## <a name="cause"></a>Põhjus

See probleem ilmneb siis, kui talendisuhete meeskonnal ei ole talendi kasutajarolli.

## <a name="resolution"></a>Eraldusvõime

Määrake talendi kasutajaroll talendisuhete meeskonnale.

1. Logige sisse [Power Platform i halduskeskusse](https://admin.powerplatform.microsoft.com) mis tahes järgmise administraatori identimisteabega.

   - Dynamics 365 administraator
   - Globaalne administraator
   - Power Platformi administraator

2. Navigeerimispaanil valige **Keskkond** ja seejärel valige keskkond, milles määrata talendi kasutajaroll talendisuhete meeskonnale.

   ![Keskkonna valimine](./media/attract-troubleshoot-career-portal-select-environment.png)

3. Valige paanil **Keskkonnad** **Keskkonna URL** ja logige sisse keskkonna haldusportaali (nt https:<orgname>.crm.dynamics.com).

4. Valige **Sätted**, valige **Süsteem** ja seejärel valige **Turve**.

   ![Turbe juurde liikumine](./media/attract-troubleshoot-career-portal-security.png)

5. Valige **Meeskonnad**.

   ![Meeskondade valimine](./media/attract-troubleshoot-career-portal-security-teams.png)

6. Sisestage otsinguväljale **Talendisuhete meeskond** ja valige seejärel otsingutulemustest meeskond.

7. Valige lindilt **ROLLIDE HALDAMINE**.

8. Valige dialoogis **Meeskonnarollide haldamine** saadaolevate rollide loendist **Talendi kasutaja** ja seejärel valige rolli rakendamiseks **OK**.

   ![Rolli rakendamine](./media/attract-troubleshoot-career-portal-apply-role.png)

9. Testige muudatusi.

   1. Logige karjääriportaali sisse uues brauseriaknas.
   2. Kandideerige karjääriportaalis tööle. 