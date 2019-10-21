---
title: Talentit ei kuvata Microsoft Dynamics 365 rakenduste hulgas (Common Data Service 1.0)
description: Selles teemas selgitatakse, mida teha, kui klient ei näe Microsoft Microsoft Dynamics 365 rakenduste hulgas valikut Microsoft Dynamics 365 Talent.
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
ms.openlocfilehash: 956af80a8ab2f454d9f523d3c74dda754ef0f793
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009372"
---
# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-common-data-service-10"></a>Talentit ei kuvata Microsoft Dynamics 365 rakenduste hulgas (Common Data Service 1.0)

[!include [banner](includes/banner.md)]

**Väljastamine**

Klient ei näe Microsoft Dynamics365 rakenduste hulgas valikut Microsoft Dynamics 365 Talent.

**Eraldusvõime**

Kasutajale peab Microsoft PowerAppsis olema keskkonna jaoks lisatud roll Keskkonna looja.

1. PowerAppsi plaani 2 litsentsi omav administraatorkasutaja peab avama lehe [PowerAppsi Haldusportaal](https://preview.admin.powerapps.com/).
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
