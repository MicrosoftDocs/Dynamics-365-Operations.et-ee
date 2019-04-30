---
title: Talentit ei kuvata Microsoft Dynamics 365 rakenduste hulgas (Common Data Service 1.0)
description: Selles teemas selgitatakse, mida teha, kui klient ei näe Microsoft Microsoft Dynamics 365 rakenduste hulgas valikut Microsoft Dynamics 365 for Talent.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: ad5add2b572ccb6bff175806b965f63b53986152
ms.sourcegitcommit: 45b79d1e587e03f5cde2766cdec4eaa7a2a897a3
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2019
ms.locfileid: "949778"
---
# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-common-data-service-10"></a>Talentit ei kuvata Microsoft Dynamics 365 rakenduste hulgas (Common Data Service 1.0)

[!include [banner](includes/banner.md)]

**Väljastamine**

Klient ei näe Microsoft Dynamics365 rakenduste hulgas valikut Microsoft Dynamics 365 for Talent.

**Eraldusvõime**

Kasutajale peab Microsoft PowerAppsis olema keskkonna jaoks lisatud roll Keskkonna looja.

1. PowerAppsi plaani 2 litsentsi omav administraatorkasutaja peab avama lehe [PowerAppsi administraatori portaal](https://preview.admin.powerapps.com/).
2. Valige **Keskkonnad** ja seejärel õige keskkond rakendusele Talent.
3. Tehke vahekaardi **Turve** vahekaardil **Keskkonnarollid** valik **Keskkonna looja**.

    ![Vahekaart Keskkonnarollid](media/environment-roles.png)

4. Lisage vahekaardil **Kasutajad** kasutaja või organisatsioon.

    ![Vahekaart Kasutajad](media/environment-maker.png)

5. Valige käsk **Salvesta**.
6. Kasutaja peab kohe sisse logima lehele [Microsoft Dynamics 365](https://home.dynamics.com/).
7. Valige kasutajarakenduste uuendamiseks **Sünkrooni**.

    ![Nupp Sünkrooni](media/get-more.png)

    Pärast sünkroonimise lõpuleviimist ilmub rakendus Talent avalehel.
