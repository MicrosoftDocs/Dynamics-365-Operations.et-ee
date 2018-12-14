---
title: Rakendust Talent ei kuvata Microsoft Dynamics 365 rakenduste hulgas (CDS1.0)
description: "Selles teemas selgitatakse, mida teha, kui klient ei näe Microsoft Dynamics 365 rakenduste hulgas valikut Microsoft Dynamics 365 for Talent."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 32ae0ab807e953bd811a557e6878b9bee79d293c
ms.contentlocale: et-ee
ms.lasthandoff: 12/04/2018

---

# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-cds10"></a>Rakendust Talent ei kuvata Microsoft Dynamics 365 rakenduste hulgas (CDS1.0)

[!include [banner](includes/banner.md)]

**Probleem**

Klient ei näe Microsoft Dynamics 365 rakenduste hulgas valikut Microsoft Dynamics 365 for Talent.

**Eraldusvõime**

Kasutajale peab Microsoft PowerAppsis olema keskkonna jaoks lisatud roll Keskkonna looja.

1. PowerAppsi plaani 2 litsentsi omav administraatorkasutaja peab avama lehe [PowerAppsi administraatori portaal](https://preview.admin.powerapps.com/).
2. Valige **Keskkonnad** ja seejärel õige keskkond rakendusele Talent.
3. Tehke vahekaardi **Turve** vahekaardil **Keskkonnarollid** valik **Keskkonna looja**.

    ![Vahekaart Keskkonnarollid](media/environment-roles.png)

4. Lisage vahekaardil **Kasutajad** kasutaja või organisatsioon.

    ![Vahekaart Kasutajad](media/environment-maker.png)

5. Valige **Salvesta**.
6. Kasutaja peab kohe sisse logima lehele [Microsoft Dynamics 365](https://home.dynamics.com/).
7. Valige kasutajarakenduste uuendamiseks **Sünkrooni**.

    ![Nupp Sünkrooni](media/get-more.png)

    Pärast sünkroonimise lõpuleviimist ilmub rakendus Talent avalehel.

